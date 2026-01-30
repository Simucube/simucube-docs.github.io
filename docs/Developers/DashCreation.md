# Creating SC Link Wheel dashes

Dashes consist of a directory containing a JSON configuration file, lua scripts, images and font files. The directory
needs to be located in Documents/SimucubeTuner/dashes/ in the user's home directory. The JSON configuration file needs
to be located in the root of this directory, and all other files used by the dash should be in this directory or in
subdirectories.

## JSON configuration file

The JSON file needs to be named *dash.json* so that the dash appears in Tuner in the list of available dashboards. All
files mentioned in the configuration file should have a path relative to the directory where the configuration file is
located. The file should have contents like in the following example:

```json
{
    "version": "1.0.0",
    "name": "Example Dash",
    "author": "Simucube",
    "preview_image": "preview.png",
    "fonts": {
        "moongloss_16": {
            "path": "fonts/MoonGlossDisplayThick.otf",
            "size": 16,
            "additional_chars": "abcdefgABCDEFG0123456789"
        },
        "Bold_30": {
            "path": "fonts/TTSupermolot_Bold.ttf",
            "size": 30,
            "usage": "NAMES",
            "additional_chars": "km/h"
        }
    },
    "scripts": {
        "main": "script/main.lua",
        "widgets": "script/widgets.lua"
    },
    "images": {
        "background": "images/sc_dash.png",
        "popup_mask": {
            "path": "images/popup_mask.png",
            "format": "alpha_only"
        }
    }
}
```

#### version (required)
The *version* string must be 1.0.0, other values are not supported.

#### name (optional)
The *name* value is displayed in Tuner where the dashboard is selected along with the preview image.

#### author (optional)
The *author* value is displayed in Tuner where the dashboard is selected along with the preview image.

#### preview_image (required)
*preview_image* is the image displayed in Tuner where the dashboard is selected.

### fonts (optional)
The *fonts* section is not mandatory if the dash doesn’t use any text or it only uses built-in fonts. The built-in fonts
are  montserrat_12, montserrat_14, montserrat_16, montserrat_32, montserrat_48, roboto_56 and roboto_bold_144. They
contain all ASCII characters.  
When using additional fonts, only the characters explicitly added using "usage" and "additional_characters" will be
available as characters in the dash labels. This is done to save memory, as all used characters are converted to a
bitmap format and added to the dash data used by the SC Link Wheel.

The built-in fonts as well as the fonts added in the JSON configuration are added to the dash.font table in Lua, and can
be used by using the built-in name or object name in the configuration file, e.g.
```
font1 = dash.font.moongloss_16
font2 = dash.font.Bold_30
font3 = dash.font.montserrat_32
```
The font objects have the following fields:
#### path (required)
The *path* value is the relative path to the font file in TTF, OTF or WOFF format.

#### size (required)
*size* is the font size.

#### usage (optional)
Groups of characters which are made available to the dash. The possible values and the characters they will add to the
dash are:

| Group  | Added characters                                                                            |
|--------|---------------------------------------------------------------------------------------------|
| names  | "0123456789abcdefghijklmnopqrstuvwxyzåäö'/ àâèéêïûüç"                                       |
| Names  | "0123456789abcdefghijklmnopqrstuvwxyzåäöABCDEFGHIJKLMNOPQRSTUVWXYZÅÄÖ'/ àâèéêïûüçÀÂÈÉÊÏÛÜÇ" |
| NAMES  | "0123456789ABCDEFGHIJKLMNOPQRSTUVWXYZÅÄÖ'/ ÀÂÈÉÊÏÛÜÇ"                                       |
| values | "0123456789.,;:!?/RN+-°% abhimkprs"                                                         |

#### additional_chars (optional)
*additional_chars* is a string containing characters added to the dash.

### scripts (required)
The *scripts* object contains all lua scripts used in the dash. The keys in the configuration are the module names used
by Lua. The main module needs to be called “main”. This module is run when the dash is loaded.  
For example, the “widgets” Lua script can be used in the main Lua script using
```
local widgets = require("widgets")
```

### images (optional)
*images* contains all images used by the dash. Images can be in any format supported by the Qt QImage class.
The images can be added by only using a key-value pair like “background” in the example, or by using an object like
“popup_mask”.  
The key or the object name are added to the Lua dash.image table so they can be used in Lua scripts, e.g.
```
local page = dash.create_page(dash.image.background)
```
When using an object, the following fields are used:
#### path (required)
The path to the image file.

#### width (optional)
The width, if not using the width of the image.

#### height (optional)
The height, if not using the height of the image.

#### format (optional)
Values “alpha_only” and “a8” are supported. Both values mean that the image contains an alpha channel, and only the
transparency information in this channel is used. The color of the image is set separately using the "set_recolor"
function of the image dash object, e.g.
```
# Show red popup
local popup = dash.create_image(page, {x=5, y=5, image=dash.image.popup_mask})
popup:set_recolor(0xFF0000)
dash.update()
```

## Lua scripting
The dash scripts are written in Lua 5.4 (https://www.lua.org/manual/5.4/).
The Lua standard libraries built into the Lua engine running on the module are baselib, strlib, tablib and mathlib.
Additionally SC Link Wheel specific libraries (dash, dash.wheel, dash.telemetry etc.) are available which have ldoc
generated API documentation.

When creating new dashes, starting *sc-tuner.exe* from the command line and selecting the new dash for upload will show
any errors during script compilation to bytecode, e.g.
```
[2026-01-28 13:45:19.504] [control] [error] Dash "C:/Users/User1/Documents/SimucubeTuner/dashes/sc_dash_advanced/dash.json": Lua error 3: ...ts/SimucubeTuner/dashes/sc_dash_advanced/script/main.lua:6: syntax error near 'local'
```
If an error occurs when running a dash script on the wheel module, the screen will show an error message.

## Dash Viewer
Dash Viewer is a separate application which can be used to test dashes without uploading them to the wheel. 
Use File->Open to open the dash.json configuration file. The configuration file will be read and the scripts compiled
to bytecode, and any errors will be printed. If reading the configuration file succeeds, the dash will be displayed.
Dash Viewer uses Tuner through SC-API for telemetry. Tuner must be running so that the viewer receives telemetry values
from a game. Debug prints from the lua scripts will also be visible.
Dash Viewer can also be used to create a preview image for Tuner by using File->Save screen capture …
