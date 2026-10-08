# 🚦 Four-Way Traffic Signal Using Arduino

## 📌 Project Overview

The **Four-Way Traffic Signal System using Arduino UNO** is a simple traffic management prototype designed to control traffic lights at a four-road intersection.

The system uses an **Arduino UNO** to control Red, Yellow, and Green LEDs for four different directions:

* North
* East
* South
* West

Each direction gets a predefined **Green → Yellow → Red** sequence, allowing traffic to move one direction at a time.

---

## 🎯 Objectives

* To design a simple four-way traffic signal system.
* To understand Arduino digital output control.
* To implement traffic light sequencing using Arduino.
* To demonstrate basic embedded-system programming.
* To create a low-cost traffic signal prototype.

---

## ⚙️ Components Required

| Component     |    Quantity |
| ------------- | ----------: |
| Arduino UNO   |           1 |
| Red LED       |           4 |
| Yellow LED    |           4 |
| Green LED     |           4 |
| 220Ω Resistor |          12 |
| Breadboard    |           1 |
| Jumper Wires  | As required |
| USB Cable     |           1 |

---

## 🔌 Pin Configuration

| Direction | Green | Yellow | Red |
| --------- | ----: | -----: | --: |
| North     |    D2 |     D3 |  D4 |
| East      |    D5 |     D6 |  D7 |
| South     |    D8 |     D9 | D10 |
| West      |   D11 |    D12 | D13 |

---

## 🔄 Working Principle

The Arduino controls the traffic signals in sequence.

### 1. North Direction

* North Green → 5 seconds
* North Yellow → 2 seconds
* North Red → ON

### 2. East Direction

* East Green → 5 seconds
* East Yellow → 2 seconds
* East Red → ON

### 3. South Direction

* South Green → 5 seconds
* South Yellow → 2 seconds
* South Red → ON

### 4. West Direction

* West Green → 5 seconds
* West Yellow → 2 seconds
* West Red → ON

After the West direction, the sequence starts again from North.

---

## 🧠 Program Flow

```text
          START
            ↓
       Initialize Pins
            ↓
       All Signals RED
            ↓
      NORTH → GREEN
            ↓
      NORTH → YELLOW
            ↓
      NORTH → RED
            ↓
       EAST → GREEN
            ↓
       EAST → YELLOW
            ↓
       EAST → RED
            ↓
      SOUTH → GREEN
            ↓
      SOUTH → YELLOW
            ↓
      SOUTH → RED
            ↓
       WEST → GREEN
            ↓
       WEST → YELLOW
            ↓
       WEST → RED
            ↓
        Repeat
```

---

## 💡 LED Connection

For each LED:

```text
Arduino Digital Pin
        │
        │
      220Ω
     Resistor
        │
       LED
        │
       GND
```

The **220Ω resistor** is used to limit current through the LED.

---

## 💻 Software

* **Arduino IDE**
* **Programming Language:** C/C++ (Arduino)
* **Board:** Arduino UNO

---

## 📂 Repository Structure

```text
Four-Way-Traffic-Signal/
│
├── Four_Way_Traffic_Signal.ino
├── README.md
└── images/
    └── circuit.jpg
```

---

## 🚀 How to Run

1. Install the **Arduino IDE**.
2. Connect the Arduino UNO to your computer.
3. Open `Four_Way_Traffic_Signal.ino`.
4. Select:

   * Board → Arduino UNO
   * Correct COM Port
5. Click **Verify**.
6. Upload the program.
7. Connect the LEDs according to the pin configuration.
8. Observe the four-way traffic signal sequence.

---

## 📊 Timing

| Signal |                    Duration |
| ------ | --------------------------: |
| Green  |                   5 seconds |
| Yellow |                   2 seconds |
| Red    | Depends on other directions |

---

## 🔮 Future Improvements

The project can be upgraded by adding:

* 🚗 IR sensors for vehicle detection
* ⏱️ 7-segment countdown display
* 🚶 Pedestrian crossing system
* 🔊 Buzzer for pedestrian alerts
* 📡 IoT monitoring
* 📱 Mobile application
* 🚑 Emergency vehicle priority
* 🌐 Web-based traffic monitoring
* 🤖 AI-based traffic density detection

---

## 🎓 Applications

This prototype can be used for:

* Embedded Systems projects
* Arduino demonstrations
* Traffic signal prototypes
* Engineering mini projects
* IoT and smart-city project development
* Educational demonstrations

---

## 👨‍💻 Author

**Roshan Kallis**

Electrical and Electronics Engineering

This project is created for **educational and academic purposes**. You are free to modify and improve the project for learning and non-commercial use.
