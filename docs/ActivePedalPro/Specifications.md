# ActivePedal Pro specifications

## Physical

| Property          | Value                                                                                                      |
| ----------------- | ---------------------------------------------------------------------------------------------------------- |
| Dimensions        | 100 x 255 x 418 mm (4 x 10 x 16.5 in)                                                                      |
| Weight            | 6 kg (13.2 lb)                                                                                                      |
| Connectors        | Simucube Link, two external passive pedal ports, power in			                                         |
| Force range       | Up to 110 kg (242.5 lb)																									 |
| Travel range      | 5 - 74 mm (2.9 in)																								     |
| Power consumption | 10 - 100 W in average use, 280 W peak                                                                      |


## Game support

### As standard pedal

ActivePedal Pro appears to computer as a standard USB game controller and therefore it works with any racing game that supports such device (basically all racing games). In these games device acts as USB pedal without game telemetry data based effects.

- Also in this mode, pedal profile and feel is fully configurable by force-travel curve, friction, damping and game output mapping curve. 
- Device may be software configured to act as a brake, throttle or clutch.

### With telemetry data effects

Active effects like RPM and ABS are only supported by games that can produce required telemetry data and are supported
by the Tuner software. See [game support list](../Tuner/games/index.md) for list of these games and required steps to enable
telemetry data if game doesn't provide it automatically.



Support for more games are being developed and are released in future Tuner software updates.

## ActivePedal & Tuner compatible passive pedals

Together with the ActivePedal you may also purchase a passive throttle pedal, the [Simucube Throttle](../Simucube Throttle/index.md). In addition specific passive pedals have been verified by Simucube to be connectable to ActivePedal system. "Connectable" in here means that the pedal may be wired to one of ActivePedal external pedal ports and get the benefits of configuring them through Tuner. 

### Connectable passive pedals

Supported with separately sold link cable:

* Heusinkveld Sim Pedals Sprint
* Heusinkveld Sim Pedals Ultimate
* Heusinkveld Sim Pedals Ultimate+

### Other passive pedals

Generally any USB connected pedal should work with ActivePedals as long as they are physically fittable in the same rig. Using direct USB connection on passive pedals will rely on their respective software thus are not confugrable through Tuner.

Additional to USB connection, most of load cell sensor based passive pedals could work via ActivePedal external pedal input and with Tuner regardless of not being listed in this page. Fitting them in ActivePedal system may require third party or DIY adapter.

## Mechanical dimensions, electrical pinouts, API

For Mounting hole footprint images and 3D models, see [drawings section](Drawings.md). For Electrical pinouts etc. see Developer section [Electrical pinouts](../Developers/ActivePedal/Pinouts.md)

