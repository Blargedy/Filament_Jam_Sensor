# Tasty-Sensor
A sensor that detects jams made of organic home-grown filament, and also runout.

![20230521_024540](https://github.com/Blargedy/Tasty_Sensor-A_Filament_Jam_and_Runout_Sensor/assets/25805271/ec5eebe4-cf4f-431b-842a-fcc315797377)

![20230521_025040](https://github.com/Blargedy/Tasty_Sensor-A_Filament_Jam_and_Runout_Sensor/assets/25805271/eb0f8fcc-b289-4426-813b-3d47cd0f4420)

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


![image](https://user-images.githubusercontent.com/25805271/221359839-47dba987-1dad-490d-907d-3c242c5a4b7b.png)

![image](https://user-images.githubusercontent.com/25805271/221359857-2f93749e-09b7-4e1e-baa9-52b849552389.png)

![image](https://user-images.githubusercontent.com/25805271/221359872-6cf89379-db94-4af9-949a-0afbb010349a.png)

## BoM
* 2pcs M3x8 BHCS
* 5pcs M3x10 SHCS
* 2pcs M3x12 SHCS
* 2pcs M3x25 SHCS
* 6pcs M3 hex nuts
* 2pcs M3 5mmWx4mmH threaded heat inserts
* 2pcs PC4-M6 pneumatic fittings
* 1pcs Optical Sensor
* 6pcs 623zz bearings
* 6pcs 5mmOD 3mmID 0.5mmH Shims

## Printing Recommendations

* Print the filament guides in 0.1mm layer height.
* Print everything else in 0.2mm layer height.
* Clearances were calibrated for eSun ABS+ and Polymaker ASA. Polymaker ABS could be used but it shrinks slightly more so fitment is tighter. Other filaments are untested.
* Clearances are sensitive to EM innacuracies and elephants foot so make sure you've tuned those properly.

## Instructions
1. Melt on the heat inserts
![image](https://user-images.githubusercontent.com/25805271/227226282-ca1c7612-1707-4485-ae4c-b6217fee5a94.png)
![image](https://user-images.githubusercontent.com/25805271/227226679-b782c6dd-3696-4428-abd4-2838868713f8.png)
![image](https://user-images.githubusercontent.com/25805271/227227142-206d96e0-df5e-4d57-8bf8-d581aa96f97b.png)

2. Insert hex nuts, pulling them tight with an M3 bolt
![image](https://user-images.githubusercontent.com/25805271/227229248-a977f2aa-76f8-42d4-b6d6-e1c509bfa20f.png)
![image](https://user-images.githubusercontent.com/25805271/227229905-35c2ffd6-263c-4eec-b9c2-0cc05db02c49.png)

3. Press fit the filament guides onto three bearings
![image](https://user-images.githubusercontent.com/25805271/227231143-e344410b-fe81-48f1-b42c-3b74f1d7c1e0.png)

4. Attach the bearing to the tensioner with an M3x8 BHCS
![image](https://user-images.githubusercontent.com/25805271/227232908-8bb72c05-f6c6-4784-a370-9b2db857d11e.png)

5. Insert the tensioner into the tensioner pocket
![image](https://user-images.githubusercontent.com/25805271/227233828-1a1c9a54-965d-4ab9-83c1-5ae4f3944cb9.png)

6. Attach the bearing with the middle filament guide onto plunger with an M3x8 BHCS
![image](https://user-images.githubusercontent.com/25805271/227234943-1ed15942-49e8-4245-a044-24d5fd354872.png)

7. Place the plunger onto the vertical channel, then move the tensioner loosely into position
![image](https://user-images.githubusercontent.com/25805271/227237973-252d94e8-9dff-4a71-a963-ab2dda0b817c.png)

8. Attach the rest of the bearings with M3x10 SHCS
![image](https://user-images.githubusercontent.com/25805271/227240238-e0293772-fd40-426c-9c33-316e592dc87b.png)

9. Gently push the tensioner into the plunger with your finger, then loosely tighten the set screw so that the tensioner won't back off but not so much that the plunger binds. You must maintain smooth movement. 
![image](https://user-images.githubusercontent.com/25805271/227241263-07cb394c-fcef-43c9-a0ff-5286db2052a2.png)

10. Insert the spring into the plunger cutout and test to see if you still have full range of motion on the plunger. It must be able to move the same amount with the spring in as without the spring. 
![image](https://user-images.githubusercontent.com/25805271/227242961-9e0a1054-dff8-4eae-a2ce-60890f22e1e8.png)

11. Install the optical sensor with M3x12 SHCS
![image](https://user-images.githubusercontent.com/25805271/227244091-b27a08ee-b6ed-40ff-bba2-302c54ab7add.png)

12. Screw on the Pneumatic tube fitments directly into the plastic 
![image](https://user-images.githubusercontent.com/25805271/227244727-8f25b7d4-f5c6-41a8-80da-b31b089c3977.png)

13. (Optional) Attach the tasty-sensor to your printer frame with the standoffs and M3x25 SHCS
![image](https://user-images.githubusercontent.com/25805271/227245259-b0b99817-debb-4764-b083-bdb4ab3c0e50.png)

14. Connect 5v, Signal, and Ground to the optical endstop

15. Add the following to your printer.cfg file:
```
[filament_switch_sensor filament_sensor]
switch_pin: !<your pin>
pause_on_runout: True
insert_gcode:
    M117 Insert Detected
runout_gcode:
    M117 Runout Detected
