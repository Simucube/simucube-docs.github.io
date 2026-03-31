# Creating SC Link Wheel dashes

Dashes consist of a directory containing a JSON configuration file, Lua scripts, images and font files. The directory
needs to be located in Documents/SimucubeTuner/dashes/ in the user's home directory. The JSON configuration file needs
to be located in the root of this directory, and all other files used by the dash should be in this directory or in
subdirectories.

For a tutorial on creating dashes including JSON configuration, Lua scripting basics, and code examples, see the
[Getting Started guide](DashAPIDocs/getting-started.html). The full
[Lua API reference](DashAPIDocs/index.html) is also available.

The rest of this page covers details not included in the above documentation.

## JSON configuration details

The JSON file needs to be named *dash.json* so that the dash appears in Tuner in the list of available dashboards.

The top-level fields are:

| Field | Required | Description |
|-------|----------|-------------|
| version | yes | Must be "1.0.0", other values are not supported |
| name | no | Displayed in Tuner where the dashboard is selected |
| author | no | Displayed in Tuner where the dashboard is selected |
| preview_image | yes | Image displayed in Tuner where the dashboard is selected |
| fonts | no | Font definitions, see below |
| scripts | yes | Lua script files, see the [Getting Started guide](DashAPIDocs/getting-started.html) |
| images | no | Image definitions, see below |

### Font usage groups

When using custom fonts, only the characters explicitly added using "usage" and "additional_chars" will be
available as characters in the dash labels. This is done to save memory, as all used characters are converted to a
bitmap format and added to the dash data used by the SC Link Wheel.

The *usage* field allows adding predefined groups of characters:

| Group  | Added characters                                                                            |
|--------|---------------------------------------------------------------------------------------------|
| names  | "0123456789abcdefghijklmnopqrstuvwxyzåäö'/ àâèéêïûüç"                                       |
| Names  | "0123456789abcdefghijklmnopqrstuvwxyzåäöABCDEFGHIJKLMNOPQRSTUVWXYZÅÄÖ'/ àâèéêïûüçÀÂÈÉÊÏÛÜÇ" |
| NAMES  | "0123456789ABCDEFGHIJKLMNOPQRSTUVWXYZÅÄÖ'/ ÀÂÈÉÊÏÛÜÇ"                                       |
| values | "0123456789.,;:!?/RN+-°% abhimkprs"                                                         |

The *additional_chars* field is a string of individual characters to add to the dash.

Built-in fonts contain all ASCII characters and do not need usage or additional_chars configuration.

### Image configuration

Images can be in any format supported by the Qt QImage class.
When using an object instead of a plain path string, the following fields are available:

| Field | Required | Description |
|-------|----------|-------------|
| path | yes | Relative path to the image file |
| width | no | Override the width of the image |
| height | no | Override the height of the image |
| format | no | "alpha_only" or "a8" — use only the alpha channel, set color separately with set_recolor |

## Lua scripting

The dash scripts are written in Lua 5.5 (https://www.lua.org/manual/5.5/).
The Lua standard libraries built into the Lua engine running on the module are baselib, strlib, tablib and mathlib.

## Error checking

When creating new dashes, starting *sc-dash_viewer.exe* from the command line and opening the dash will show
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
