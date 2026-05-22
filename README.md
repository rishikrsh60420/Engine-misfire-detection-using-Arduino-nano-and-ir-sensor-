This project simulates how a crankshaft misfire detection system works in an automobile engine using an Arduino Nano, IR speed sensor, encoder disc, OLED display, and DC motor. 
The IR sensor detects pulses from the rotating encoder disc attached to the motor shaft. Using these pulses, the Arduino calculates RPM in real time.
The system continuously monitors the rotational speed of the motor. 
After a fixed interval, a temporary RPM drop is introduced to simulate an engine misfire. When the RPM suddenly decreases, the Arduino detects the abnormal variation in pulse timing and triggers a warning indication using an LED and OLED display.

This project demonstrates:
RPM measurement
Pulse signal processing
Basic angular displacement estimation
Misfire simulation
Embedded system interfacing

Components Used
Component	Quantity
Arduino Nano	1
FC-03 IR Speed Sensor	1
SPI OLED Display (SSD1306)	1
DC Motor	1
Encoder Disc / Slotted Wheel	1
BC547 Transistor	1
1N4007 Diode	1
100uF Capacitor	1
Red LED	1
220Ω Resistor	1
1kΩ Resistor	1
9V Battery	1
Breadboard	1
Jumper Wires	Multiple


Working Principle (Step by Step)
1. Motor Rotation

The DC motor rotates continuously using a 9V power supply. An encoder disc is attached to the motor shaft.

2. Pulse Generation

As the encoder disc rotates, the slots pass through the FC-03 IR sensor. The sensor generates digital pulses based on the interruption/reflection of infrared light.

3. RPM Calculation

The Arduino Nano receives these pulses through interrupt pin D2. By measuring the time interval between pulses, the Arduino calculates the rotational speed (RPM).

4. RPM Monitoring

The system continuously checks whether the RPM remains stable during operation.

5. Misfire Simulation

After a fixed time interval, a temporary reduction in RPM is introduced to simulate an engine misfire condition.

6. Misfire Detection

When the RPM suddenly drops below the threshold value, the Arduino identifies it as a misfire event.

7. Alert Indication
The red LED turns ON during the misfire condition.
The OLED display shows the RPM value and misfire warning message.
Features
Real-time RPM monitoring
Misfire simulation
OLED display output
LED warning indication
IR sensor pulse detection
Embedded signal processing

Applications
Automotive electronics learning
Embedded systems projects
RPM monitoring systems
Engine diagnostics simulation
Sensor interfacing practice

Future Improvements
Real engine integration
Hall-effect crankshaft sensing
Wireless monitoring
Data logging
Multi-cylinder simulation
Graph plotting on OLED
