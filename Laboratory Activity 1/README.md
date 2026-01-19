# Laboratory Activity #1: Working with Digital Signals

## 📝 Description
This project demonstrates the implementation of a **LED Running Light** sequence using an Arduino microcontroller. The activity serves as a practical application of digital output control, requiring precise timing and sequential logic to manipulate hardware components.

## 🎯 Objectives
* Review **Arduino** as a primary device for IoT systems implementation.
* Discuss and implement **digital signals** within an Arduino circuit.
* Develop a functional understanding of pin manipulation and timing delays.

## 🛠️ Components Used
* **Microcontroller:** Arduino Uno (or compatible board)
* **Output Devices:** 5x LEDs
* **Current Limiting:** 5x 220Ω - 330Ω Resistors
* **Prototyping:** Breadboard and Jumper Wires



## 💡 Concepts Applied
* **Digital Output:** Utilizing `digitalWrite()` to send `HIGH` (5V) and `LOW` (0V) signals.
* **Pin Initialization:** Configuring GPIO pins using `pinMode()`.
* **Timing Logic:** Implementing synchronous delays using the `delay()` function.
* **Sequential Control:** Using loops or ordered statements to create a "running" visual effect.

## ⚙️ System Behavior
The system follows a specific 12-to-8 sequence:
1. **Power On:** All LEDs start in the `LOW` state.
2. **Phase 1 (Loading):** Starting from Pin 12, LEDs turn **ON** one by one with a 1-second interval until all 5 are lit.
3. **Phase 2 (Clearing):** Starting from Pin 12, LEDs turn **OFF** one by one with a 1-second interval until all are dark.
4. **Loop:** The sequence repeats indefinitely.

## 📂 Repository Content
* **Sketch File:** `*.ino` file containing the source code.
* **Diagram:** Breadboard layout (TinkerCad/Fritzing) showing the wiring of pins 8-12.
* **Documentation:** Individual grades and contributions of the members.

## 👥 Members
| De Asis, Johnny Jr. S. |
| Osit, Eduardo V. |
| Padilla, Allexzeus Marvel C. |

---
*Created for Laboratory Activity #1 - Digital Signals Review.*
