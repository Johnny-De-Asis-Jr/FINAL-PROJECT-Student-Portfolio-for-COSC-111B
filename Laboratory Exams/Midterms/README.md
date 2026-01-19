# Midterms Laboratory Exam: Smart Outdoor Lighting System

## 📝 Description
This project involves designing and programming an intelligent lighting system for outdoor environments using an Arduino. The system monitors ambient light conditions through a photoresistor and adjusts LED indicators accordingly. It features two distinct operational states: a **Manual Mode** for user-defined sensitivity and an **Automatic Mode** that simulates responses to environmental changes like cloudy weather or bright sunlight.

## 🎯 Objectives
* Measure light intensity using a photoresistor and convert sensor readings from a 0–1023 range into a 0–100% scale.
* Implement conditional logic to control three different LEDs based on light thresholds.
* Create a robust Serial interface for real-time data monitoring and system interaction.
* Develop a dynamic threshold system that adjusts based on environmental simulations.

## 🛠️ Components Used
* **Microcontroller:** Arduino Uno.
* **Input Sensor:** Photoresistor (LDR) connected to Analog Pin A0.
* **Output Indicators:** * **Green LED:** Low light indicator.
    * **Yellow LED:** Medium light indicator.
    * **Red LED:** High light indicator.
* **Other:** Breadboard, jumper wires, and resistors.



## 💡 Concepts Applied
* **Analog-to-Digital Conversion:** Mapping 10-bit sensor data (0-1023) to a percentage (0-100%).
* **State Machine Logic:** Managing transitions between **Manual** and **Automatic** modes.
* **String Manipulation:** Using `startsWith()` and `substring()` methods to parse Serial commands.
* **Dynamic Thresholding:** Automatically reassigning trigger values based on current light intensity to simulate weather conditions.

## ⚙️ System Behavior
The system displays data every second including Light Intensity (%), Current Mode, Active LED, and Environment status.

### Threshold Rules
Only **one** LED is active at a time:
* **Green:** Active during LOW threshold.
* **Yellow:** Active during MED threshold.
* **Red:** Active during HIGH threshold.

### Operational Modes
* **Manual (Default):** Users can manually set thresholds using commands like `SET LOW xx` or `SET HIGH xx`.
* **Automatic:** Thresholds adjust dynamically based on the current environment:
    * **Cloudy:** Low = 0%, High = 40%.
    * **Normal:** Low = 41%, High = 70%.
    * **Bright Sunlight:** Low = 71%, High = 100%.

## 📂 Repository Content
* **Source Code:** The Arduino `.ino` sketch implementing the smart lighting logic.
* **Diagram:** Breadboard diagram illustrating the LDR and LED wiring.

## 👥 Members
| Ambong, Jemuel Chris N. | De Asis, Johnny Jr. S. | Dellosa, Keren G. | Magma, John Harold R. | Padilla, Allexzeus Marvel C. |
