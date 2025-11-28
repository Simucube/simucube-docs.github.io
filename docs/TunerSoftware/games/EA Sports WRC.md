# EA Sports WRC

Tuner will configuring telemetry automatically, after the game is started and closed once, when
Tuner is also running. When updating Tuner or the game, it may be necessary to configure telemetry again.

Tuner will automatically patch "Documents/My Games/WRC/telemetry/config.json" and add custom telemetry packet type for itself. It uses port 27878 by default.

## Enabling Force Feedback for Simucube 3

Find your 
``SteamApps\common\EA SPORTS WRC\WRC\Content\input\Windows\devices\device_defines.xml`` file.

file. Add a new xml entry after 
``<device_list>`` as follows, on a single line:

``  <device id="{0D6616D0-0000-0000-0000-504944564944}" name="simucube link" priority="90" type="wheel" official="false" />``