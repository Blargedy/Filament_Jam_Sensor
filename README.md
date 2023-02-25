# Tasty-Sensor
A sensor that detects jams made of organic home-grown filament, and also runout.

The Tasty-Sensor detects if the filament gets stuck on the way to the nozzle, or if the filament ran out but didn't get jammed like it usually does.

I needed a sensor that detects when the filament runs out, but I couldn't find one that worked for me, so I designed my own. A regular runout sensor sometimes worked if the hook at the end of a spool was gentle enough to slip through the sensor, but almost always the filament got stuck on the end of the sensor and the print failed silently. Sensors that check for filament movement (such as the BTT Smart Filament Sensor) gave me too many false positives even after the recommended tuning and adjustment. The sensor that got the closest to what I wanted is the SpEye by MirageC [thingiverse](https://www.thingiverse.com/thing:4299458) | [docs.hevort](http://docs.hevort.com/#/pages/Mods/spy-eye.md)

The SpEye introduced too much friction in the filament path to be feasible to me. The primary cause for this was the plunger binding and the filament sliding along the bearings instead of letting the bearings roll. The binding of the plunger comes from a direct plastic-to-plastic movement interface, and the spring tension acting offset from the center of rotation, causing a moment in the plunger. The SpEye needs two different stiffnesses of springs to function properly, and I didn't have two springs the right length and with different enough stiffness.

I sought to solve these issues in my design. The features of the Tasty-Sensor are as follows:

* Spring tension is aligned with the center of mass
* Only a single spring is needed 
* Plunger runs on bearings to reduce friction
* TPU tires on bearings let the bearings roll instead of having the filament slide over them

The primary drawbacks of this design are:

* Needs 6 bearings instead of 3
* Needs more parts printed
* Needs more fasteners
* Spring tension cannot be tuned and needs a spring swap for switching from ABS to flexible for example
* Loading filament is slightly harder


![image](https://user-images.githubusercontent.com/25805271/221357951-ac97b073-3dd4-4dad-a956-d6344baf1d16.png)

![image](https://user-images.githubusercontent.com/25805271/220586563-00bb3905-0ea4-483d-9f1a-a8820eaa070f.png)

![image](https://user-images.githubusercontent.com/25805271/221358006-48f0283d-2005-4272-8bc1-ce3248720c9b.png)


## Printing Recommendations

* Print the filament guides in 0.1mm layer height.
* Print everything else in 0.2mm layer height.
* Clearances were calibrated for eSun ABS+ and Polymaker ASA. Polymaker ABS could be used but it shrinks slightly more so fitment is tighter. Other filaments are untested.
* Clearances are sensitive to EM innacuracies and elephants foot so make sure you've tuned those properly.
