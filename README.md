A comprehensive IoT project using ESP32 to monitor environmental sensors and control LEDs remotely via MQTT protocol. 
🎯 OVERVIEW
This project demonstrates a complete IoT solution where an ESP32 microcontroller:
->Reads data from ultrasonic distance sensor (HC-SR04)
->Monitors ambient light levels using an LDR sensor
->Publishes sensor data to MQTT broker every 5 seconds
->Controls two LEDs (Red & Green) based on MQTT commands
->Enables remote monitoring and control via Python script

🔧 HARDWARE COMPONENTS
(1)ESP32 DevKit C V4 (x1)
→ Acts as the main microcontroller responsible for reading sensor data, controlling LEDs, and communicating with the MQTT broker.

(2)HC-SR04 Ultrasonic Sensor (x1)
→ Connected to TRIG pin 25 and ECHO pin 26.
→ Used to measure distance in the range of 2 cm to 400 cm.

(3)LDR (Photoresistor) Sensor (x1)
→ Connected to analog pin 34 (ADC input).
→ Detects the surrounding light intensity and provides an analog voltage output.

(4)Red LED (x1)
→ Connected to Anode pin 23, Cathode to GND.
→ Used as Status Indicator 1 (e.g., shows system alerts or threshold triggers).

(5)Green LED (x1)
→ Connected to Anode pin 22, Cathode to GND.
→ Used as Status Indicator 2 (e.g., shows successful connection or operation status).

🌳 MQTT TOPIC TREE
All topics are organized under the main topic prefix: mqtt-demo/

(a)mqtt-demo/ultrasonic — (Publish)
Used by ESP32 to send distance sensor data from the Ultrasonic sensor.

(b)mqtt-demo/light — (Publish)
Used by ESP32 to send light intensity data from the LDR sensor.

(c)mqtt-demo/led1 — (Subscribe)
Used by the ESP32 to receive control commands for the Red LED.
Accepts commands like "on" or "off".

(d)mqtt-demo/led2 — (Subscribe)
Used by the ESP32 to receive control commands for the Green LED.
Accepts commands like "on" or "off".
