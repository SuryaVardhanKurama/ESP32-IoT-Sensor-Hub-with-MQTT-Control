🎯 OVERVIEW

A comprehensive IoT project using ESP32 to monitor environmental sensors and control LEDs remotely via the MQTT protocol.

This project demonstrates a complete IoT solution where an ESP32 microcontroller:

1.Reads data from an Ultrasonic Distance Sensor (HC-SR04)

2.Monitors ambient light levels using an LDR sensor

3.Publishes sensor data to an MQTT broker every 5 seconds

4.Controls two LEDs (Red & Green) based on MQTT commands

5.Enables remote monitoring and control via a Python script

🔧 HARDWARE COMPONENTS

1.ESP32 DevKit C V4 (x1) → Acts as the main microcontroller responsible for reading sensor data, controlling LEDs, and communicating with the MQTT broker.

2.HC-SR04 Ultrasonic Sensor (x1) → Connected to TRIG pin 25 and ECHO pin 26. Used to measure distance in the range of 2 cm to 400 cm.

3.LDR (Photoresistor) Sensor (x1) → Connected to analog pin 34 (ADC input). Detects surrounding light intensity and provides an analog voltage output.

4.Red LED (x1) → Connected to Anode pin 23, Cathode to GND. Used as Status Indicator 1 (e.g., system alerts or threshold triggers).

5.Green LED (x1) → Connected to Anode pin 22, Cathode to GND. Used as Status Indicator 2 (e.g., successful connection or operation status).

🌳 MQTT TOPIC TREE

All topics are organized under the main topic prefix: mqtt-demo/

1.mqtt-demo/ultrasonic — (Publish) Used by ESP32 to send distance data from the Ultrasonic sensor.

2.mqtt-demo/light — (Publish) Used by ESP32 to send light intensity data from the LDR sensor.

3.mqtt-demo/led1 — (Subscribe) Used by ESP32 to receive control commands for the Red LED. Accepts commands like "on" or "off".

4.mqtt-demo/led2 — (Subscribe) Used by ESP32 to receive control commands for the Green LED. Accepts commands like "on" or "off".
