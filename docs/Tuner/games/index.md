# Game setup

This section covers all supported simulator game titles. Overview of supported features and first time setup guides.

Brake threshold vibration and clutch bite point effects don't require telemetry data and are available in all games.

| Game                       | Setup <sup>2</sup>                     | ABS              | TC <sup>1</sup>  | RPM              | G-Force          | Treshold | Bite Point |     |     |     |     |     |     |
| -------------------------- | -------------------------------------- | ---------------- | ---------------- | ---------------- | ---------------- |----------|------------| --- | --- | --- | --- | --- | --- |
| Assetto Corsa              | Automatic                              | :material-check: | :material-check: | :material-check: | :material-check: |       :material-check:   |      :material-check:      |     |     |     |     |     |     |
| Assetto Corsa Competizione | Automatic                              | :material-check: | :material-check: | :material-check: | :material-check: |    :material-check:      |      :material-check:      |     |     |     |     |     |     |
| Automobilista 2            | [:material-wrench:](Automobilista2.md) | :material-check: | :material-check: | :material-check: | :material-check: |     :material-check:     |       :material-check:     |     |     |     |     |     |     |
| BeamNG.drive               | [:material-wrench:](BeamNG.md)         | :material-check: | :material-check: | :material-check: | :material-check: |    :material-check:      |      :material-check:      |     |     |     |     |     |     |
| Codemasters F1             | [:material-wrench:](F1.md)             |                  |                  | :material-check: | :material-check: |     :material-check:     |      :material-check:      |     |     |     |     |     |     |
| Dirt Rally 1 & 2           | [:material-wrench:](DirtRally.md)      |                  |                  | :material-check: | :material-check: |  :material-check:        |          :material-check:  |     |     |     |     |     |     |
| Live for Speed             | [:material-wrench:](LFS.md)            | :material-check: | :material-check: | :material-check: | :material-check: |      :material-check:    |      :material-check:      |     |     |     |     |     |     |
| iRacing                    | Automatic                              | :material-check: |                  | :material-check: |                  |      :material-check:    |      :material-check:      |     |     |     |     |     |     |
| Project CARS 1             | [:material-wrench:](pCARS.md)          | :material-check: |                  | :material-check: | :material-check: |     :material-check:     |      :material-check:      |     |     |     |     |     |     |
| Project CARS 2             | [:material-wrench:](pCARS2.md)         | :material-check: |                  | :material-check: | :material-check: |     :material-check:     |     :material-check:       |     |     |     |     |     |     |
| RaceRoom Racing Experience | Automatic                              | :material-check: | :material-check: | :material-check: | :material-check: |     :material-check:     |      :material-check:      |     |     |     |     |     |     |
| WRC Generations            | [:material-wrench:](WRC Generations.md)                              | :material-check: | :material-check: | :material-check: | :material-check: |     :material-check:     |      :material-check:      |     |     |     |     |     |     |


<sup>1</sup> TC stands for Traction Control effect. Some games do not provide telemetry data needed for this effect.

<sup>2</sup> Automatic in the table means that the game does not require game configuration. Just have the Tuner app running in background to use telemetry data.

## Checking game telemetry status

To check whether telemetry data is connected to Tuner, look at the left bottom edge telemetry status area of Tuner main window. When supported the simulator is detected as running, the status should say SIMULATOR CONNECTED and name of the simulator should be shown in the following line. 

If game is running but Tuner hasn't received telemetry data yet, "Waiting for telemetry data" status text is displayed. Most games provide provide telemetry data only while the race is running thus it is expected to see this text in the status area when game is in menus. 

If there are no telemetry effects and this text is still shown when the simulation is running, see game specific instructions and verify that telemetry is suitably configured.