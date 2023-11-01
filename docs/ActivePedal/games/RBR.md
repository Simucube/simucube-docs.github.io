# Richard Burns Rally

### Setup

Telemetry needs to be enabled via RSF launcher program or by manually editing RichardBurnsRally.ini in the game folder. UDP Telemetry support requires NGP plugin to be installed (which is included with most RBR mods like RallySimFans)

In RSF Launcher enable "advanced options" and click on "Telemetry" options

1. Tick "UDP Telemetry" 
2. IP: 127.0.0.1
3. Port: 6776

![](assets/RBR_telemetry.png)

Alternatively in RBR root folder open RichardBurnsRally.ini file and find **[NGP]** section and put the following lines
```
[NGP]
udpTelemetry=1
udpTelemetryAddress=127.0.0.1
udpTelemetryPort=6776

```