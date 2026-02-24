# ENGR4321-ESP32-WiFi--Assignment
#ESP-32 Wifi Connection Assignment
Gabriella Luna
February 23, 2026

## Project Overview
This project demonstrates the use of an ESP32 microcontroller to connect to WiFi, communicate with a cloud-based MQTT broker, and exchange data using JSON formatting. The system simulates a basic IoT monitoring and control application in the Wokwi environment. The ESP32 reads temperature data from an analog sensor, publishes the data to a cloud topic, and subscribes to a separate topic to receive remote control commands. When a command is received from the cloud, the ESP32 toggles an LED output, demonstrating bidirectional communication between embedded hardware and a web-based service.

## Hardware Components
  -Microcontoller: ESP32 DevKit 
  -Input Devices:
    -Analog Temperature Sensor
    -Pushbutton
  -Output Devides:
    -LED with resistor
  -Simulation Platform: Wokwi
  
## System Connections
Temperature Sensor → ESP32 Analog Pin
Pushbutton → ESP32 Digital Input Pin
LED → ESP32 Digital Output Pin
ESP32 → WiFi (Wokwi-GUEST Network)
ESP32 → HiveMQ Cloud Broker

## How it Works
The ESP32 connects to the Wokwi-GUEST WiFi network.
It establishes a connection to the public MQTT broker (broker.hivemq.com).
The ESP32 publishes temperature readings in JSON format to the topic: SF/TEMP
The ESP32 subscribes to the topic: GMSimulation
When the message "on" is received, the LED turns ON.
When the message "off" is received, the LED turns OFF.
All system events (WiFi connection, MQTT connection, incoming messages, temperature data) are displayed in the Serial Monitor.

## Simulation Link
https://wokwi.com/projects/456710115743521793
