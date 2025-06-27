# 🚦 Railway Track Security and Signaling System

This project is a Final Year Engineering project aimed at improving railway safety and automation. It simulates a railway track system that includes smart signaling, track monitoring with sensors, and track switching using servo motors — all controlled via an Arduino-based setup.

## 📌 Features

- 🔴🟡🟢 **Automatic Signal Control** using 9 signal posts with Red, Yellow, and Green LEDs.
- 📡 **IR Sensor Detection**: 7 IR sensors to detect train position and manage block sections.
- ⚙️ **Track Switching Mechanism**: 4 servo motors dynamically change track routes based on real-time train location.
- 🔄 **Communication between two Arduino Uno boards** using SoftwareSerial protocol.
- 🧠 **Real-time Decision Making**: Ensures one train per block, avoids collisions, and provides proper signaling for merging/diverging tracks.
- 📊 **Efficient Resource Usage**:
  - 74HC595 shift registers for controlling 27 LEDs.
  - 74HC165 shift register for reading multiple IR sensors with minimal Arduino pins.

## 🛠️ Technologies Used

- **Arduino Uno (x2)**
- **IR Sensors (x7)**
- **Servo Motors (x4)**
- **74HC595 Shift Registers (for output LEDs)**
- **74HC165 Shift Register (for input sensors)**
- **C++ (Arduino Programming)**
- **SoftwareSerial Library**

## 🔌 Circuit Overview

- **LED Signals**: 9 posts × 3 LEDs (Green, Yellow, Red) = 27 LEDs controlled via 74HC595 shift registers.
- **Sensors**: 7 IR sensors connected through a 74HC165 input shift register.
- **Servos**: 4 Servo motors for dynamic track switching.
- **Dual Arduino Setup**:
  - Arduino 1: Handles sensors and LED signals.
  - Arduino 2: Controls servo motors based on commands via SoftwareSerial.

## 📈 Logic Flow

1. **IR sensor detects a train** at entry.
2. **Signal turns Red** for the current block; next block is checked.
3. If **next block is free**, signal turns Green and train proceeds.
4. If **track merging or diverging**, servo checks logic and switches track accordingly.
5. Arduino 1 sends serial command (`s1`, `s2`, `count20`, etc.) to Arduino 2 for servo control.

## 🧪 Testing & Simulation

- System tested in both hardware and software simulation (Wokwi).
- All scenarios like route merging, diverging, and block occupation are handled.
- Simulation matches real-world railway signal behavior.

## 🎯 Objective

To simulate a real-time railway track signaling and security system that enhances:
- Safety by preventing collisions
- Efficiency via automation
- Track utilization through servo-controlled routing

## 🧑‍💻 Team Contributions

- **Rakesh Naskar** – Software Developer, Arduino Programmer, Circuit Designer  
- **Sahin Dafader** – Software Developer  
- **Manoj Bhakta** – Hardware Integration  
- **Samir Sutradhar** – Hardware Integration

## 📷 Images / Videos

> Add circuit images or demo videos links/screenshots here for better presentation.

## 📁 Folder Structure

