# Live for Speed

## Setup

Live for Speed telemetry needs to be enabled from the config file of the game.

1. Navigate to Live for Speed installation folder. (e.g. C:\\LFS\\)
2. Open file **"cfg.txt"** in a text editor.

![](assets/lfs_telemetry_1.png)

3. Change **OutSim** and **OutGauge** settings near the end of the file to following:

```
OutSim Mode 1
OutSim Delay 1
OutSim IP 127.0.0.1
OutSim Port 4445
OutSim ID 0
OutSim Opts 1ff
OutGauge Mode 2
OutGauge Delay 1
OutGauge IP 127.0.0.1
OutGauge Port 4444
OutGauge ID 0
```

![](assets/lfs_telemetry_2.png)


## FAQ

### Tuner detects the game running but says "Waiting for telemetry data from the game" even when simulation is already running

This indicates that Tuner does not receive telemetry data from the game. This can be due to configuration not matching
the above default configuration.

This game uses UDP technology to deliver telemetry data. Only one application can listen to a single UDP port at once.
That primary telemetry receiver must then forward the telemetry data for other application that require data.
So if any other app is using this game's telemetry data (i.e. Simhub), then Tuner connection to data may be blocked.

You can instead follow SimHub's instructions for LFS telemetry configuration (which uses ports 63392 and 63393),
and then forward the telemetry data to Tuner and port 4444 following [these instructions](https://github.com/SHWotever/SimHub/wiki/Sharing-UDP-data-with-other-applications).

