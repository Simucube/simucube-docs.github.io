# ActivePedal specifications

## Physical

| Property          | Value                                                                                                      |
| ----------------- | ---------------------------------------------------------------------------------------------------------- |
| Dimensions        | 100 x 250 x 402 mm                                                                                         |
| Weight            | 6 kg                                                                                                       |
| Connectors        | Simucube Link, two external passive pedal ports, power in, power out                                       |
| Force range       | 1-150 kg (default) or 1-120 kg ([user configurable](Mechanical adjustments.md#optimizing-force-vs-travel)) |
| Travel range      | 1-62 mm (default) or 1-79 mm ([user configurable](Mechanical adjustments.md#optimizing-force-vs-travel))   |
| Power consumption | 10 - 100 W in average use, 480 W peak                                                                      |


## Game support

### As standard pedal

ActivePedal appears to computer as a standard USB game controller and therefore it works with any racing game that supports such device (basically all racing games). In these games device acts as USB pedal without game telemetry data based effects.

- Also in this mode, pedal profile and feel is fully configurable by force-travel curve, friction, damping and game output mapping curve. 
- Device may be be software configured to act as a brake, throttle or clutch.

### With telemetry data effects

Selected games are supported with game telemetry data utilizing effects, such as motor RPM vibration, ABS effect and more. Titles supported at the moment are:

- Iracing
- Assetto Corsa
- Assetto Corsa Competizione

More titles are being developed and released with Tuner software udpates.

## ActivePedal & Tuner compatible passive pedals

Specific passive pedals have been verified by Simucube to be connectable to ActivePedal system. "Connectable" in here means that the pedal may be wired to one of ActivePedal external pedal ports and get the benefits of configuring them through Tuner. 

### Connectable passive pedals

Out-of-the box support:

* Simucube Throttle

Supported with separately sold link cable:

* Heusinkveld Sim Pedals Sprint
* Heusinkveld Sim Pedals Ultimate
* Heusinkveld Sim Pedals Ultimate+

### Other passive pedals

Generally any USB connected pedal should work with ActivePedals as long as they are physically fittable in the same rig. Using direct USB connection on passive pedals will rely on their respective software thus are not confugrable through Tuner.

Additional to USB connection, most of load cell sensor based passive pedals could work via ActivePedal external pedal input and with Tuner regardless of not being listed in this page. Fitting them in ActivePedal system may require third party or DIY adapter.

## Mechanical dimensions, electrical pinouts, API

See Developers section of this online guide for details and downloads.

