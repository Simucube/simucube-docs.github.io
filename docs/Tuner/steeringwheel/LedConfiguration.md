## LED
### Open LED config tab
1. Select Steering Wheel from the device list in overview or in left side panel
2. In top left corner under the ”hamburger" menu is a tab called "**LED**". Select the tab.

![](assets/SteeringWheelValoViewLED.png)

### Adjust LED brightness
- Use the slider labeled **LED Brightness** to adjust the brightness of the LEDs

### Select LED Profile
- In top right corner of the LED tab view, you may select the desired LED profile from the drop-down menu.

### Test Telemetry effects
   - Press a **Test** button next to the effect you want to test
   - The effect will be displayed on the wheel LEDs

### Edit LED profile
- Pressing the "**Edit**" button above the Brightness slider will give you an option to edit the LED profile that you chose.

![](assets/SteeringWheelValoViewLEDEdit.png)

:bulb: <font color="orange">Template profiles cannot be saved over, but they can be saved as new.</font>

- In top right corner there is a button "Add Effect" which allows you to add new effect.
    - If there is already same type of effect, the other effects will be shown with dimmed down highlight color to help with visualization.

![](assets/SteeringWheelValoViewLEDEditAddEffectSameEffect.png)

- The right-side panel is effect list and is in hierarchical order starting from the top.
    - Click any of the effects to select it, it will become highlighted with orange color.
    - Click and hold three (3) lines to move the effect up or down.
    - X on the right-side area will delete the effect from the list.

- Icon with three (3) hollowed circles indicate a ramping effect
- Icon with circle and dot in middle indicates non-ramping effect

### Editing LED colors ###

1. Select the LED(s) you would like to change from the image, by clicking the LED location area. 
    - Selected LEDs will appear at the bottom panel.
2. In the bottom panel you can now click the square. The square is divided into two parts, top and bottom (depending on the effect) and you can select them. 
    - When you select, a white indicator will tell you that that part of the LED has been selected.
3. Choose a color picker and pick the color you like.
    - <font color="orange">Make sure you have color not selected as black, since darker color you choose, dimmer it appears. </font>
4. For visualization, press test button. 

![](assets/SteeringWheelValoViewLEDEditSelectColor.png)

- Drop down menu next to the slider will give you an option how would you like to animate your effect.
- Slider gives frequency and smoothness options for the animations based on the animation type.
- "**Clear selected**" button removes all the selected LEDs giving you a clean slate.
- "**Reset to default**" changes to default parameters that the effect has.

:bulb: <font color="orange">Non-ramping effects tend to have multi color option per led, unless led is chosen to be static.</font>

Each LED can be used in up to eight (8) different effects and you can see which effect the LED has by hovering over the LED.

![](assets/SteeringWheelValoViewLEDEditSelectLED.png)

---

## Car configuration menu
### Open Car configuration menu
- Select **SIMULATOR CONNECTED** from the bottom of the left side menu

![](assets/ConnectedSimulator.png)
![](assets/img_3.png)

### Select game
- The game that is currently running will be automatically selected, 
but you can also adjust settings for other games by selecting them from the **Select game** drop-down menu in the top right corner

### Selecting a car profile
- If the game you are playing offers the car name through the telemetry, the current car will be automatically added as a tab to the car configuration menu.
  - 5 previously used cars will be displayed.
  - Check the **Use car specific profile** checkbox to use a car specific profile
  - If the game does not offer the car name through the telemetry or **Use car specific profile** is not checked the **Default** car will be used.

### RPM range values
#### First shift light
RPM value for when the first shift light turns on.
#### Last shift light
RPM value for when the last shift light turns on.
#### Over rev blink
RPM value for when the blinking starts.
#### Engine rev limit RPM or Rev limit  
RPM value for the maximum RPM of the car.

### Adjusting RPM range values
- If the game you are playing offers the car rpm range through the telemetry, the RPM values are ignored and cannot be adjusted. 
  To adjust the RPM range, you need to unselect the **Use car specific profile** checkbox and adjust values in the Default car profile.
- The RPM range can be specified as **Relative** or **Absolute**.
  - **Relative** means that the RPM range values are relative to the **Engine rev limit RPM** and set as percentages between the different RPM values.
  - **Absolute** means that the RPM range values set as RPM values.
  - If desired, the RPM ranges can be adjusted separately for each gear using the table in section **Change shift lights by active transmission gear**.


