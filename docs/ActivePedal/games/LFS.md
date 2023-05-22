# Live for Speed

## Setup

Live for Speed telemetry needs to be enabled from the games config files.

1. Navigate to Live for Speed installation folder. (e.g. C:\\LFS\\)
2. Open file **"cfd.txt"** in a text editor.

![](assets/lfs_telemetry_1.png)

3. Change **OutSim** and **OutGauge** settings near the end of the file to following:

```
OutSim Mode 1
OutSim Delay 1
OutSim IP 127.0.0.1
OutSim Port 4445
OutSim ID 0
OutSim Opts 1ff
OutGauge Mode 1
OutGauge Delay 1
OutGauge IP 127.0.0.1
OutGauge Port 4444
OutGauge ID 0
```

![](assets/lfs_telemetry_2.png)

## Tips

(jos on jotain vinkkejä tai huomion arvoista niin se tieto tänne)

## FAQ

### Question "Game does not connect"
    This game uses UDP technology to deliver telemetry data. This limits number of telemetry clients to one application. So if any other app is using this game's telemetry data (i.e. Simhub), then Tuner connection to data may be blocked. To workaround this, take a look of [this article](https://github.com/SHWotever/SimHub/wiki/Sharing-UDP-data-with-other-applications).
