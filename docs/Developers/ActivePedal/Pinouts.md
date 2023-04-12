## Passive pedal port

The ports labeled as PEDAL 1 and PEDAL 2 support de-facto standard *load cell* pedals and *Hall effect sensor* based pedals. The port has been optimized for typical 1 kOhm load cells. Hall effect sensor output type has to be analog voltage and has to be rated to withstand supply voltage of 5 VDC.

### Pinout

The pinout of 6 pin *RJ12 6P6C* connector specified below.
Do not connect pin 6 (cable shield) to pin 5 (GND).

| Pin | Load cell wiring                        | Hall effect sensor wiring                            |
| --- | --------------------------------------- | ---------------------------------------------------- |
| 1   | (not connected)                         | Sensor output (0-5 VDC)                              |
| 2   | E+                                      | Sensor positive supply voltage (5 VDC, 30 mA max)    |
| 3   | S-                                      | Connect this pin through a 10 kOhm resistor to pin 2 |
| 4   | S+                                      | Connect this pin through a 10 kOhm resistor to pin 5 |
| 5   | E-                                      | Sensor negative supply voltage (GND)                 |
| 6   | Cable shield (not connected elsewhere) | Cable shield (not connected elsewhere)                |

