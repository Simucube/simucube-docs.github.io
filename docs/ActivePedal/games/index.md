# Game setup

This section covers all supported simulator game titles. Overview of supported features and first time setup guides.

| Game                       | ABS              | TC               | RPM              | Setup                                 |
| -------------------------- | ---------------- | ---------------- | ---------------- | ------------------------------------- |
| Assetto Corsa              | :material-check: | :material-check: | :material-check: | Automatic                             |
| Assetto Corsa Competizione | :material-check: | :material-check: | :material-check: | Automatic                             |
| Automobilista 2            | :material-check: | :material-check: | :material-check: | [:material-wrench:](Automobilista2.md) |
| BeamNG.drive               | :material-check: | :material-check: | :material-check: | [:material-wrench:](BeamNG.md)        |
| Live for Speed             | :material-check: | :material-check: | :material-check: | [:material-wrench:](LFS.md)           |
| iRacing                    | :material-check: |                  | :material-check: | Automatic                             |
| Project CARS 1             | :material-check: |                  | :material-check: | [:material-wrench:](pCARS.md)           |
| Project CARS 2             | :material-check: |                  | :material-check: | [:material-wrench:](pCARS2.md)           |

## Automatic setup

Games marked as "Automatic" in the table do not require configuration. Just have the game running with Tuner and telemetry data is obtained automatically.

## Check game telemetry status

To check whether telemetry data is connected to Tuner, look at the left bottom edge telemetry status area of Tuner main window.
When supported the simulator is detected as running, the status should be "SIMULATOR CONNECTED" and name of the simulator
should be shown in the following line. If game is running but Tuner hasn't received telemetry data yet,
"Waiting for telemetry data" status text is displayed. Most games only provide any kind of telemetry data, when the
simulation is running, so it is normal to see this in the main menu. If there is no telemetry effects and this text
is still shown when the simulation is running, see game specific instructions and verify that telemetry is suitably
configured.
