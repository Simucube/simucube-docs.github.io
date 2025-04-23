## Simucube 2 Accessory Port

The Accessory Port can be used to connect four analog inputs (0 to 5 V) and two digital button inputs (e.g. sequental shifter) to the wheelbase. Wiring pinouts and information is in a separate PDF guide:

[:material-download-circle: Simucube 2 Accessory Port Application Guide](https://granitedevices.com/w/images/c/c5/Simucube_2_Accessory_Port_Application_Guide.pdf)

Granite Devices does not recommend any new commercial products to be designed for this port as of 2025.


## Simucube 2 USB interface documentation

### Simucube product USB axis description and support requirements

- Wheel axis: X axis, Unsigned 16 bit field, 0-65535 value
- Y axis: Unsigned 16 bit field. 
    - This axis will idle at center position. However, users can map external pedal or handbrake to this axis.
    - Do not utilize product X and Y axises for in-game menu browsing!
- Pedal/handbrake axises: 6 additional axises, unsigned 16 bit values.
    - These can be set by users to inteface with Simucube-compatible pedals or handbrakes, or with (upcoming) analog axises (clutch paddles) from Simucube Wireless Wheels
- Buttons: There are 128 buttons.
    - All buttons can be used by Simucube 1 physical interface, and when combined with a Simucube wireless wheel, support for all 128 buttons is required for optimal user experience.

### Simucube product USB interface detection

USB Vendor ID: 0x16d0

USB Product IDs and Windows guidProduct ID list:

| Product name | USB Product ID | guiProduct ID | Visible name in Windows | Notes |
| ------------ | -------------- | ------------- | ----------------------- | ----- |
Simucube 1 | 0x0d5a | {0D5A16D0-0000-0000-0000-504944564944} | SimuCUBE |
Simucube 2 Sport | 0x0d61 | {0D6116D0-0000-0000-0000-504944564944} | Simucube 2 Sport |
Simucube 2 Pro | 0x0d60 | {0D6016D0-0000-0000-0000-504944564944} | Simucube 2 Pro |
Simucube 2 Ultimate | 0x0d5f | {0D5F16D0-0000-0000-0000-504944564944} | Simucube 2 Ultimate |
Simucube Link Hub | 0x0d66 | {0D6616D0-0000-0000-0000-504944564944} | SC-Link | Used by Simucube ActivePedal

