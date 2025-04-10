# Setting up FFB strength

FFB strength can be set up from many locations, including

 * The car in the simulator migth have separate control for it
 * The simulator can have a master setting for it
 * Device Driver software (Tuner FFB settings profile)

Setting up FFB in wrong way may result in inherently unsafe settings. It may also result in torque saturation (clipping), which in itself is not harmful to the device or to the driver. However if that happens in normal driving situations, FFB details are not felt on the wheel and vital information about tires and track are lost.

This document explains how FFB strength and some other settings should be set in optimal way.


## Step 1
Set the maximum strenght in the device driver software to the maximum that you would like to feel on your hands suddenly in crash situations. This is critical for safety.

Some simulators such as iRacing have a protection for crash forces - FFB is much reduced if car contacts e.g. wall. Some other simulators do not have any safety features, and (if High Torque Mode is activated) you are at risk of getting sudden full torque to your fingers when hitting walls, if you leave FFB strength at 100% in Tuner.

## Step 2
Go driving in the simulator. If the simulator has a FFB strength bar or indicator, observe it and tune the FFB strength in such way that the overall strength feeling is satisfactory and you are not hitting any constant maximum FFB periods in e.g. cornering. That would be clipping and details would be lost. If you hit some clipping on some particular kerbs, that is not something that has to be avoided and will actually work in your benefit.

!!! Tip
    Enable the torque saturation notification beeps in the wheel base configuration view to enable some indication when torque saturation is happening, in case the simulator does not have such indicator.


If the FFB feels still weak and you are experiencing torque saturation (clipping) , increase the overall FFB strength in Tuner (Step 1), and reduce it in the simulator to avoid clipping. Then continue tuning the in-simulator FFB strength to find suitable combination.

## Step 3: FFB feeling setup

Use mechanical feeling filters to set the overall wheel feeling - even when the sim is not running - to your liking. Some damping and friction are realistic to be used, and are also beneficial to reduce tendency for oscillation if you let go of the wheel while driving.

Then use the smoothness filters to set up how the FFB details feel.

## Simulation specific tips and tricks

### iRacing
iRacing defaults to showing arbitary units for the in-sim FFB strength.

Click on the strength label to set the slider to show Nm (Newton meter) based saturation point (Maximum Force) instead. Working with real units is preferred instead of the arbitary units.

This point controls the torque level, at which the full torque is (set from Tuner) is requested. Bigger Nm based number results in smaller overall torque level.

Wheel force controls the strength of the automatic FFB adjustment. iRacing measures how you drive and selects the maximum torque level you would experience based on that driving data. When clicking the automatic FFB checkbox, this data is used to set the Strength. However, if during the data gathering, you drove very carefully, it could be situation where the automatic FFB adjustment would select too strong FFB that would in fact cause clipping. Wheel force setting tries to prevent this from happening by setting a maximum level of torque that the wheel base is expected to be able to produce.

The intensity slider in iRacing does not affect FFB. It only controls how close to the limit set by Wheel Force the automatic FFB setting puts the FFB Strength. Therefore it only takes affect when you click the automatic FFB button.

Smoothness is an internal to iRacing filter that smooths the FFB. It is likely still better to leave this to 0% and to use wheel base internal smoothness filters in FFB settings profile instead to extract full potential of what the simulator is giving to the servo drive system.


### Assetto Corsa

This simulator has separate per-car HUD FFB level setting that can be adjusted when driving. Small caveat is that there would be no FFB when this is turned to 0, and some third party tools are known to cause this issue with Assetto Corsa.