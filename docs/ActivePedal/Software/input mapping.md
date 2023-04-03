Simulator input mapping means how the ActivePedal data is sent to the simulator. This means setting the dead zones and converting the force/position to simulator input by linear or custom curve method.

![](assets/inputmapping.png)

## Role effect on Simulator input mapping

If the ActivePedal role is configured as brake then the info on how hard the pedal has been pressed is sent to the simulator based on force.

If the ActivePedal role is configured as clutch or brake then the info on pedal press is sent to the simulator based on pedal position.

## Dead zones: Force/Position input range

Force/Position input range slider sets what is the 0% and 100% force/position sent to the Simulator. This can also be set from a curtain which is seen on force curve. This is done by dragging the top/bottom or left/right -side of the curtain. This allows setting deadzones before pedal press is activated in the simulator.

## Mapping 

The force/position data can be sent to the simulator directly by using linear mapping or it is also possible to customize how the force/position data is sent to the simulator by selecting "curve mapping". The custom mapping setup is done by dragging nodes on curve mapping graph.