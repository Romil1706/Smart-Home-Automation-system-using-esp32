# Solar-Powered Smart Home Automation and Security System using ESP32 and MQTT

An IoT-based smart home automation and security system powered by solar energy, featuring remote appliance control, environmental monitoring, and MQTT-based communication.

## Overview

This project is a Solar-Powered IoT Smart Home Automation and Security System built using ESP32 and MQTT communication. The system allows users to remotely monitor environmental conditions and control home appliances through an MQTT dashboard.

The system is powered by a rechargeable battery charged using solar panels, making it an energy-efficient and sustainable solution for smart home applications.

The project combines home automation, environmental monitoring, and security features into a single platform.

## Features

* Remote control of three rooms/appliances using MQTT.
* Automatic lighting using LDR and PIR sensors.
* Temperature monitoring using DHT11 sensor.
* Humidity monitoring using DHT11 sensor.
* Gas level monitoring using MQ gas sensor.
* Motion detection using PIR sensor.
* Emergency alarm activation through MQTT.
* Real-time sensor data publishing.
* Wi-Fi connectivity using ESP32.
* Solar-powered operation.
* Battery-backed energy storage.
* Energy-efficient and sustainable design.

## Hardware Components

* ESP32 Development Board
* DHT11 Temperature and Humidity Sensor
* MQ Gas Sensor
* PIR Motion Sensor
* LDR Light Sensor Module
* Active Buzzer
* LEDs/Relays for Room Control
* Solar Panel
* Rechargeable Battery
* Jumper Wires
* Power Supply Components

## Working Principle

The ESP32 connects to a Wi-Fi network and communicates with an MQTT broker.

The system continuously:

* Reads temperature and humidity from the DHT11 sensor.
* Monitors gas levels using the MQ sensor.
* Detects motion using the PIR sensor.
* Detects ambient light using the LDR sensor.
* Publishes sensor readings to MQTT topics.

### Automatic Lighting

The LDR and PIR sensors work together to automate lighting.

* If the environment is dark and motion is detected, lights are turned ON automatically.
* If there is sufficient light or no motion is detected, lights remain OFF.

### Manual Room Control

Users can control Room 1, Room 2, and Room 3 through MQTT commands.

Each room supports:

* ON
* OFF
* AUTO

AUTO mode allows the room to follow the automatic lighting logic.

### Emergency Mode

An emergency command can be sent through MQTT to activate the buzzer remotely.

This can be used as a security alert or emergency warning system.

## Power System

The system is powered by a rechargeable battery that is charged using a solar panel.

* Solar energy is used to charge the battery.
* The battery powers the ESP32 and all connected sensors.
* The system can operate independently without direct dependence on grid electricity.

This makes the project suitable for sustainable and energy-efficient smart home applications.

## MQTT Topics

### Published Topics

| Topic        | Description            |
| ------------ | ---------------------- |
| esp32/temp   | Temperature data       |
| esp32/hum    | Humidity data          |
| esp32/gas    | Gas sensor readings    |
| esp32/motion | Motion status          |
| esp32/light  | Automatic light status |

### Subscribed Topics

| Topic           | Description              |
| --------------- | ------------------------ |
| esp32/room1     | Control Room 1           |
| esp32/room2     | Control Room 2           |
| esp32/room3     | Control Room 3           |
| esp32/emergency | Emergency buzzer control |

## Control Commands

### Room Control

| Command | Action                |
| ------- | --------------------- |
| ON      | Turn device ON        |
| OFF     | Turn device OFF       |
| AUTO    | Enable automatic mode |

### Emergency Control

| Command | Action            |
| ------- | ----------------- |
| ON      | Activate buzzer   |
| OFF     | Deactivate buzzer |

## Software and Technologies Used

* ESP32
* Arduino IDE
* MQTT Protocol
* MQTT Panel Application
* Wi-Fi Communication
* Embedded C/C++

## Author

Developed by **Romil Atmaramani** as an IoT-based Smart Home Automation and Security System using ESP32, MQTT communication, environmental monitoring, and solar-powered operation.
