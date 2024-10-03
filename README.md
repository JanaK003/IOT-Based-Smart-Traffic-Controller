# IOT-Based-Smart-Traffic-Controller


### Tagline
Automated traffic control system using ultrasonic sensors to detect vehicles and manage traffic lights.

---

## Introduction

### What is this project?
The **Smart Traffic Control System** is a real-time, automated traffic management solution built using a Raspberry Pi, ultrasonic sensors, and LEDs simulating traffic lights. The system measures the distance of vehicles approaching an intersection from four directions (north, east, south, and west) using ultrasonic sensors, and dynamically adjusts the traffic lights based on traffic density. The direction with the highest vehicle density gets priority with a green light, enhancing traffic flow and reducing congestion.

### Why was this project created?
This project was created to demonstrate the use of sensors and a Raspberry Pi to automate traffic management. It simulates a smarter, more efficient way of controlling traffic at intersections, responding to real-time vehicle data. This type of system could be implemented in smart cities to reduce traffic jams and improve road safety.

---

## Key Features
- **Real-Time Traffic Detection**: Uses four ultrasonic sensors (one for each direction) to detect the proximity of vehicles and estimate traffic density.
- **Dynamic Traffic Light Control**: Automatically switches traffic lights based on the sensor input, giving priority to directions with heavier traffic.
- **LED Simulation**: Simulates traffic lights using LEDs for red, yellow, and green signals.
- **Automatic Operation**: Continuously monitors traffic and adjusts lights every 5 seconds.
- **Easy to Expand**: The system can be scaled for more complex intersections by adding more sensors and logic.

---

## Screenshots
- **Circuit Diagram**
- **Real-Time Traffic Control Output**

---

## Getting Started

### Prerequisites
- Raspberry Pi (with GPIO access)
- HC-SR04 Ultrasonic Sensors (4)
- LEDs (Red, Yellow, Green for each direction)
- Breadboard and jumper wires for connections
- Resistors (for LEDs)

---

## Connections

### 1. Ultrasonic Sensors (HC-SR04) to Raspberry Pi:
| **Direction** | **TRIG Pin**  | **ECHO Pin**  |
|---------------|---------------|---------------|
| North         | GPIO 23       | GPIO 17       |
| East          | GPIO 24       | GPIO 27       |
| South         | GPIO 25       | GPIO 22       |
| West          | GPIO 26       | GPIO 5        |

### 2. Traffic Lights (LEDs) to Raspberry Pi:
| **Direction** | **Red Pin**   | **Yellow Pin**| **Green Pin** |
|---------------|---------------|---------------|---------------|
| North         | GPIO 18       | GPIO 19       | GPIO 20       |
| East          | GPIO 21       | GPIO 22       | GPIO 23       |
| South         | GPIO 24       | GPIO 25       | GPIO 26       |
| West          | GPIO 27       | GPIO 28       | GPIO 29       |

### 3. Breadboard and Jumper Wires:
- Use a breadboard and jumper wires to connect the sensors and LEDs to the appropriate GPIO pins on the Raspberry Pi. Ensure that resistors are used to protect the LEDs.

---

## Installation

1. Connect the ultrasonic sensors and LEDs to the Raspberry Pi according to the pin configuration described above.
2. Install the necessary libraries to control GPIO pins on the Raspberry Pi:
   ```bash
   sudo apt-get install python3-rpi.gpio
3. Upload the provided Python code to the Raspberry Pi.

---
## Usage
1. Run the Python script on the Raspberry Pi:
   ```bash
   python3 traffic_control.py
3. The system will start monitoring vehicle distances in all four directions and adjust the traffic lights accordingly.
4. The LED corresponding to the direction with the highest traffic (closest vehicle) will turn green, while all other directions will be red.
5. The system automatically updates every 5 seconds.

---

