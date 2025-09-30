# Game setup

This section covers all supported simulator game titles, mainly for Active Pedals. Overview of supported features and first time setup guides.

Brake threshold vibration and clutch bite point effects don't require telemetry data and are available in all games.

| Game                       | ABS              | TC <sup>1</sup>  | RPM              | G-Force          | Brake Lockup     | Setup <sup>2</sup>                         |
|----------------------------|------------------|------------------| ---------------- | ---------------- |------------------|--------------------------------------------|
| American Truck Simulator   |                  |                  | :material-check: | :material-check: |                  | Automatic                                  |
| Assetto Corsa              | :material-check: | :material-check: | :material-check: | :material-check: | :material-check: | Automatic                                  |
| Assetto Corsa Competizione | :material-check: | :material-check: | :material-check: | :material-check: | :material-check: | Automatic                                  |
| Automobilista              |                  |                  | :material-check: | :material-check: | :material-check: | [:material-wrench:](Automobilista.md)      |
| Automobilista 2            | :material-check: | :material-check: | :material-check: | :material-check: | :material-check: | [:material-wrench:](Automobilista2.md)     |
| BeamNG.drive               | :material-check: | :material-check: | :material-check: | :material-check: |                  | [:material-wrench:](BeamNG.md)             |
| Codemasters F1             |                  |                  | :material-check: | :material-check: | :material-check: | [:material-wrench:](F1.md)                 |
| Dirt Rally 1 & 2           |                  |                  | :material-check: | :material-check: | :material-check: | [:material-wrench:](DirtRally.md)          |
| EA Sports WRC              | :material-check: |                  | :material-check: | :material-check: | :material-check: | [Automatic*](EA Sports WRC.md)             |
| Euro Truck Simulator 2     |                  |                  | :material-check: | :material-check: |                  | Automatic                                  |
| Forza Motorsport 8         |                  |                  | :material-check: | :material-check: |                  | [:material-wrench:](Forza Motorsport 8.md) |
| GTR 2                      |                  |                  | :material-check: | :material-check: | :material-check: | [:material-wrench:](gtr2.md)               |
| Live for Speed             | :material-check: | :material-check: | :material-check: | :material-check: | :material-check: | [:material-wrench:](LFS.md)                |
| Le Mans Ultimate           | :material-check: | :material-check: | :material-check: | :material-check: | :material-check: | [:material-wrench:](LMU.md)                |
| iRacing                    | :material-check: |                  | :material-check: | :material-check: |                  | Automatic                                  |
| Project CARS 1             | :material-check: |                  | :material-check: | :material-check: | :material-check: | [:material-wrench:](pCARS.md)              |
| Project CARS 2             | :material-check: |                  | :material-check: | :material-check: | :material-check: | [:material-wrench:](pCARS2.md)             |
| rFactor                    |                  |                  | :material-check: | :material-check: | :material-check: | [:material-wrench:](rf.md)                 |
| rFactor 2                  | :material-check: | :material-check: | :material-check: | :material-check: | :material-check: | [:material-wrench:](rf2.md)                |
| RaceRoom Racing Experience | :material-check: | :material-check: | :material-check: | :material-check: | :material-check: | Automatic                                  |
| Richard Burns Rally        |                  |                  | :material-check: | :material-check: |                  | [:material-wrench:](RBR.md)                |
| WRC Generations            | :material-check: | :material-check: | :material-check: | :material-check: |                  | [:material-wrench:](WRC Generations.md)    |


<sup>1</sup> TC stands for Traction Control effect. Some games do not provide telemetry data needed for this effect.

<sup>2</sup> Automatic in the table means that the game does not require game configuration. Just have the Tuner app running in background to use telemetry data.

## Checking game telemetry status

To check whether telemetry data is connected to Tuner, look at the left bottom edge telemetry status area of Tuner main window. When supported the simulator is detected as running, the status should say SIMULATOR CONNECTED and name of the simulator should be shown in the following line. 

If game is running but Tuner hasn't received telemetry data yet, "Waiting for telemetry data" status text is displayed. Most games provide provide telemetry data only while the race is running thus it is expected to see this text in the status area when game is in menus. 

If there are no telemetry effects and this text is still shown when the simulation is running, see game specific instructions and verify that telemetry is suitably configured.