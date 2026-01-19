# Laboratory Activity #2: Working with Analog Signals

## 📝 Description
This activity expands on the previous LED sequence logic by transitioning from binary digital signals to **Pulse Width Modulation (PWM)**. By using analog output commands, the system controls not just the state of the LEDs, but their intensity, demonstrating how microcontrollers simulate analog behavior through digital pins.

## 🎯 Objectives
* Discuss **analog signals** and their implementation within an Arduino circuit.
* Understand **Analog-to-Digital Conversion (ADC)** and signal scaling.
* Master the use of the `map()` function to translate input ranges.
* Optimize code structure using **Arrays** and **While Loops**.

## 🛠️ Components Used
* **Microcontroller:** Arduino Uno (or compatible board)
* **Output Devices:** 5x LEDs (connected to PWM-capable pins)
* **Current Limiting:** 5x 220Ω Resistors
* **Prototyping:** Breadboard and Jumper Wires



## 💡 Concepts Applied
* **PWM (Pulse Width Modulation):** Using `analogWrite()` to control the average voltage delivered to the LEDs.
* **Array Mapping:** Storing pin numbers in an array for efficient iteration.
* **Conditional Logic:** Utilizing `while()` loops for controlled execution flow instead of standard `for()` loops.
* **Range Mapping:** Using `map()` to convert values between different scales (e.g., 0-1023 to 0-255).

## ⚙️ System Behavior
The system maintains the "Running Light" logic from Activity #1 but with upgraded control:
1. **Initialization:** Pins 8 through 12 are initialized as outputs using an **Array** and a **While Loop**.
2. **Sequence:** The "running" effect flows from Pin 12 down to Pin 8.
3. **Signal Type:** Instead of simple ON/OFF states, `analogWrite()` is used to drive the LEDs.
4. **Timing:** A strict 1-second (1000ms) delay is maintained between each state change in the sequence.

## 📂 Repository Content
* **Sketch File:** `activity_2.ino` containing the optimized array and while-loop logic.
* **Diagram:** A Breadboard diagram illustrating the connection of LEDs to the specific Arduino pins.

## 👥 Members
| [Name 1] 
| [Name 2] 
| [Name 3] | | |
