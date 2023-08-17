## Setup

Telemetry for both **Dirt Rally** and **Dirt Rally 2.0** games needs to be enabled from a games config file.

1. Navigate to **Documents\\My Games\\WRCG\\**  folder.
2. Open file **"UserSettings.cfg"** in a text editor.
3. Change line **WRC.Telemetry.EnableTelemetry = false;** to **WRC.Telemetry.EnableTelemetry = true;**
## FAQ

### Tuner detects the game running but says "Waiting for telemetry data from the game" even when simulation is already running

This indicates that Tuner does not receive telemetry data from the game. This can be due to configuration not matching
the above default configuration.

This game uses UDP technology to deliver telemetry data. Only one application can listen to a single UDP port at once.
That primary telemetry receiver must then forward the telemetry data for other application that require data.
So if any other app is using this game's telemetry data (i.e. Simhub), then Tuner connection to data may be blocked.

You can instead follow SimHub's instructions for telemetry configuration and then forward the telemetry data to Tuner and port 20777 following [these instructions](https://github.com/SHWotever/SimHub/wiki/Sharing-UDP-data-with-other-applications). 