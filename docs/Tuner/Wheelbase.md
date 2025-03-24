From version 2.5.0 onwards, the Tuner software supports Simucube 2 wheelbases.

Wheelbase view gives an option to change how Simucube 2 wheelbases (Ultimate, Pro, Sport) feel.

- In top left corner press "hamburger" menu to open the **Settings** or to reset the center of your steering wheel with **Reset Center** button.
- Below the "hamburger" menu is couple of icons:
    - <font color="orange">**Power icon**</font> = indicator if high torque mode is active.
    - <font color="orange">**Fault icon**</font> = indicates if there is an issue with the wheelbase.
    - <font color="orange">**Torque-off icon**</font> = indicates if the emergency button has been pressed.

![](assets/WheelbaseView.png)

### High Torque

- Clicking the **High Torque** toggle button, popup will appear descriping the dangers of this feature.
    - Scroll all the way down to unlock the **Activate high torque mode** button.

- You can avoid having to do this process each time you toggle the high torque mode:
    1. Scroll all the way down
    2. Tap the **Automatic activation on each start**
    3. Wait for 10 second counter that appears
    4. Tap the **Automatic activation on each start** button again to check the box
    5. Tap the **Activate high torque mode** button
    6. Follow popup message instructions to confirm the automatic high torque mode feature


![](assets/WheelbaseHighTorquePopup.png)

## Basic Settings
These settings control the general behavior of the wheel base.
### Max Strength
This controls the maximum torque output that can result from simulator generated FFB signals. Bumpstops are not affected.
### Steering Range
This sets the steering rotation range from maximum left to maximum right. 

## Mechanical Feel
These settings control how the wheel feels even when no force feedback is applied. The settings are typically used to set a natural realistic feeling to the wheel and are typically required to make the wheel stable (no oscillation) in simulators.
### Damping
Damping creates a resistive force that is proportional to the rotation speed of the wheel. More faster rotation, more force opposing that rotation is generated.
### Friction
Friction creates a resistive force that is constant regardless of wheel rotation speed.
### Inertia
Inertia effect gives weight feeling to the steering wheel. It resists the rate of change of the rotation speed. Larger inertia wheel is more difficult to get turning, and keeps on turning for longer when force that is applied to make it turn, is removed.

### Centering Force
This is a simple spring effect that adds force to get the wheel back to center regardless of any game generated FFB signals.

## Smoothness
These settings affect how the force feedback feels like. Simulator generated force feedback can be quite harsh due to physics modeling and grainy due to low FFB update rate from simulator to the wheel base. These filters can be used to control those sensations.

### Reconstruction Filter
This filter is a smoothing and extrapolation filter, that smooths out low update rate torque signal from simulator to the maximum possible rate inside the wheel base. Low values make the output force follow the simulator signal very closely especially in quick direction changes, where as high values give more emphasis on overall smoothness with some compromise on accuracy. For example, if a signal changes direction, high reconstruction filter might have slight delay on the change due to interpolation, which can result in very little lag to the overall torque feeling.

### Slew Rate Limit
This filter is a smoothing filter. Rate of change of the torque signal (Nm/ms) is always limited by motor characteristics. It can also be further limited by using this filter. The result is a smooth signal but any abrupt signal changes and details in the torque may have lag, or even disappear altogether, due to change rate being limited and the output signal never having time to reach the target. This filter is especially useful when wanting to get a rubbery or less active feeling to the wheel.

### Torque Bandwidth
This is a simple low-pass signal processing filter, that removes high frequencies (details) from the simulator signal. The lower the frequency limit is set, the more details is removed. Using this filter in combination with the reconstruction filter can be a good tool to remove excessive kerb vibrations. Compared to Reconstruction Filter and Slew Rate Limit, very limited torque bandwidth can cause the signal on the steering wheel have significant lag.

## Advanced
Advanced filters are for specific use cases where simulator's deficiensies must be compensated with wheel base side software algorithms.
### Static Force Reduction
This filter removes static torque after one second. Light amount of this filter can be useful to add some sensation of power steering to the wheel. Sharp details from road details are not affected by this filter. Using a higher value can result in the weigth transfer of the simulated car to be mixed up with this filter activating and removing of the static torque. This may case driving feel to be unintuitive.
### Ultra Low Latency
This feature is wheelbase internal signal processing adjustment filter that aims to reduce latencies in the torque control loop from simulator on the PC to the wheel. It does not affect FFB feeling. Adding some ultra low latency mode can make the wheel not oscillate with less damping/friction/inertia filters than what would be otherwise required. However, adding too much, can have unintended resonance consequenses in some simulators such as rFactor2 and Le Mans Ultimate.
### Torque Linearity
This is a gamma filter that can make the wheel react with more or less to small torque signals when there is no torque on the wheel. Typical use case is to make a lifeless wheel to feel more detailed when driving straight. The adjustment is very sensitive.

### Bumpstop Feel
This affects how the wheel rotation limits (bumpstops) feel. Bumpstop effect is software generated.
### Bumpstop Range
If the simulator generates bumpstops itself inside the wheel rotation range, but does so in such way that they are very harsh or even have kick-back from them, this adjustment can be used to move the device generated bumptops so that when wheel is rotated, these device generated bumpstops are hit instead. Using this filter, this can be done without actually recalibrating the wheel base rotation in the simulator.
### Combine accessory port with wireless wheel paddles toggle
Simucube 2 Accessory Port has two digital inputs for e.g. sequental shifter. Sometimes it can be useful to combine the button presses from those to the same buttons as the shifter paddles from a Simucube Wireless Wheel. However, sometimes it can also be useful to have extra buttons instead. This checkbox controls this setting.

## Notch Filter
Notch filter is a frequency domain filter that removes a frequency from the FFB signal. This can be useful to turn down kerb vibrations or wheel oscillation. This filter is difficult to tune without knowing the frequency that the unwanted vibration occurs on.
### Center Frequency
Frequency to remove the signal.
### Attenuation dB
How much the signal is removed at that frequency.
### Q Factor
How accurately the signal frequency is removed. Higher Q factor is more accurate at that frequency, where as lower Q factor removes FFB signals also from around this frequency.

## Ultimate Filters
These are filters that are only available on Simucube 2 Ultimate.
### Static Force Reduction Speed
This controls how fast the static force is removed, if the static force reduction is used.
### Center Damping
This adds additional damping around wheel center position. The additional damping is applied smoothly when wheel is turned to within certain limit of center position.
### Center Damping Angle Span
This controls how wide rotation range around the wheel center point the Center Damping filter is being applied to.

## Game Effects
These are separate adjustments for any DirectInput effects that the simulator may use to create additional, non physics based FFB effects. The adjustments here are best left at 100%. Any sliders do not have any effect unless the particular simulator uses these effects. Not many modern racing simulators use these effects. Earlier simulators such as GTR from 2005 is using these extensively.

### Damping
Damping creates a resistive force that is proportional to the speed of the wheel. More faster rotation, more force opposing that rotation is generated.
### Friction
Friction creates a resistive force that is constant regardless of wheel rotation speed.
### Spring
This is a centering spring effect. However via DirectInput, simulator can also make the center point of the spring to be something other than wheel center point.
### Sine Wave
This is sine wave vibration to the torque signal.
### Square Wave
This is a square wave vibration signal.
### Sawtooth Wave
This is a sawtooth wave vibration signal. The slider controls both the sawtooth up and sawtooth down effects.
### Triangle Wave
This is a triangle wave vibration signal.