
Passive pedals can be used with an ActivePedal. To use external pedals connected to ActivePedal they need to be added as a device to Tuner.

![](../../ActivePedal/Software/assets/passivepedalconfig.png)

## Adding passive pedal

To add passive pedal, press **Settings** -button found on bottom left of the Tuner. From the settings window, press **Add a passive pedal** -button found on 
SC-Link Devices part of the window. Each press adds one passive pedal, so press it twice if you want to add 2 passive pedals. Now you can close the window selecting either **Save** or **Cancel** found on bottom right of the window. New device(s) is seen on a device panel. To configure pedal, select pedal on the device panel or press **Go to configuration** from the notification.

## Initial configuration and calibration

On a passive pedal configure view select to which port the passive pedal is connected (1 or 2) and select pedal role: brake, throttle or clutch. 

To calibrate the passive pedal, press the calibrate button. Then fully press the passive pedal and release it a few times. This way the range of the pedal is recorded. After this is done, press ok. Invert axis if needed.

Then input range slider becomes visible, which allows finer adjustment of dead zones so that the pedal input stays 0% when the pedal isn't pressed and also always reaches full 100% input, when pressed. Monitor the indicator above the slider to see that the dead zones are suitable and then save the configuration.

## Passive pedal input mapping

The normal profile view of the passive pedal shows the current game input level as large slider.
By default the input from the pedal is linearly sent to the game so the sensor value maps 1:1 to the game input. Optionally curve mapping can be enable that will allow creating non-linear mapping to the game.

![](../../ActivePedal/Software/assets/passivepedalcurve.png)
Vertical axis is the input sent to the game and the horizontal axis the linear input from the sensor.
