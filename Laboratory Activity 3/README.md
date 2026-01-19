# Laboratory Activity #3: Working with Sensors (Fire Sensor Simulation)

## 📝 Description
This activity involves the creation of a **Fire Sensor Simulation** system. By integrating a thermistor and a photoresistor, the system monitors environmental conditions (heat and light) to detect potential fire hazards. This project demonstrates how to handle multiple sensor inputs and trigger urgent visual and audible alerts when specific thresholds are breached.

## 🎯 Objectives
* Familiarize with basic **sensor components** used in IoT ecosystems.
* Integrate analog sensors (Thermistor and Photoresistor) into a functional Arduino circuit.
* Implement a logic-based alarm system using threshold monitoring.

## 🛠️ Components Used
* **Microcontroller:** Arduino Uno
* **Temperature Sensor:** Thermistor (connected to A0)
* **Light Sensor:** Photoresistor (LDR) (connected to A2)
* **Visual Alert:** Red LED (Pin 12)
* **Audible Alert:** Buzzer/Speaker (Pin 12)
* **Resistors:** 10kΩ for sensor voltage dividers and 220Ω for the LED.



## 💡 Concepts Applied
* **Sensor Integration:** Interfacing analog sensors using a voltage divider circuit.
* **Signal Mapping:** Converting raw analog data into meaningful units (Celsius).
* **Modular Programming:** Separating sensor logic into distinct functions for readability and maintenance.
* **Pre-processor Directives:** Using `#define` for hardware pin management.
* **Constant Definitions:** Using `const` for immutable threshold values.

## ⚙️ System Behavior
The system acts as a safety monitor with the following logic:
1. **Data Acquisition:** The system continuously reads temperature (Celsius) and brightness levels.
2. **Threshold Monitoring:**
   * **Temperature Limit:** 50°C
   * **Brightness Limit:** 220 (Digital/Mapped value)
3. **Alarm Condition:** If **BOTH** the temperature exceeds 50°C **AND** the brightness exceeds 220, the alarm is triggered.
4. **Alert Execution:** A fast-blinking Red LED and a Buzzer (on Pin 12) activate to notify the user of a fire.

## 📂 Repository Content
* **Sketch File:** `fire_sensor_simulation.ino` (Includes modular functions for temperature and light readings).
* **Diagram:** A detailed Breadboard diagram showing the wiring of the thermistor, photoresistor, and the shared LED/Buzzer pin.

## 👥 Members
| De Asis, Johnny Jr. S. | Osit, Eduardo V. | Padilla, Allexzeus Marvel C. |
