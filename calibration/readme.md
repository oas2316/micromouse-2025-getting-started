# IR Sensor Calibration 
- Move a maze wall on 3d printer in small increments while taking IR sensor readings to create a conversion table from sensor reading to distance
- Programmatically create a line of best fit to create an equation for sensor reading to distance

## Approach
1. Create a python script that uses serial to send gcode to move a printer bed with a maze wall attached
2. Open another serial port to communicate with the mouse to get IR sensor readings 
3. Store the current IR sensor reading and wall distance in a table
4. Move the wall and repeat step 3. Stop around 50 mm
5. Generate a line of best fit for the data in the table