# BeamNG.drive

## Setup

1. Navigate to **OPTIONS**
2. Select **OTHER**
3. Enable **OutGauge support**
4. Enable **MotionSim enabled**
5. Make sure IP and Port settings are set as in the picture below.

![](assets/beamng_drive_telemetry_1.png)

## FAQ

### Tuner detects the game running but says "Waiting for telemetry data from the game" even when simulation is already running

This indicates that Tuner does not receive telemetry data from the game. This can be due to configuration not matching
the above default configuration.

This game uses UDP technology to deliver telemetry data. Only one application can listen to a single UDP port at once.
That primary telemetry receiver must then forward the telemetry data for other application that require data.
So if any other app is using this game's telemetry data (i.e. Simhub), then Tuner connection to data may be blocked.

You can instead follow SimHub's instructions for BeamNG.drive telemetry configuration (which uses ports 63392),
and then forward the telemetry data to Tuner and port 4444 following [these instructions](https://github.com/SHWotever/SimHub/wiki/Sharing-UDP-data-with-other-applications).

