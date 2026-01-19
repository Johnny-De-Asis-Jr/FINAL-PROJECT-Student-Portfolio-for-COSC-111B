# COSC 111B: Internet of Things - Course Portfolio

## 📝 Description
This repository serves as a comprehensive compilation of all laboratory activities and projects completed for the **COSC 111** course. The collection tracks the progression from basic Arduino hardware control to advanced IoT implementations involving Python, FastAPI, and bidirectional serial communication.

## 🎯 Course Objectives
* Review and implement **Arduino** as a core device for IoT systems.
* Master the transition between **Digital and Analog signals**.
* Integrate sensors (Thermistors, Photoresistors) into functional circuits.
* Develop **Full-Duplex communication** between microcontrollers and high-level Python applications.
* Implement **Web-based hardware control** using the FastAPI framework.

---

## 📂 Laboratory Activities Directory

### 📍 [Laboratory Activity 1: Working with Digital Signals](./Laboratory Activity 1)
* **Goal:** Create a running light circuit using pins 8 to 12.
* **Logic:** Sequential LED control from 12 to 8 with a 1-second delay using `digitalWrite()`.

### 📍 [Laboratory Activity 2: Working with Analog Signals](./Laboratory Activity 2)
* **Goal:** Implement the running light logic using `analogWrite()` for brightness control.
* **Logic:** Utilize a `while()` loop and an **array** to initialize pin modes and handle signal conversion.

### 📍 [Laboratory Activity 3: Working with Sensors](./Laboratory Activity 3)
* **Goal:** Simple fire sensor implementation using a thermistor (A0) and photoresistor (A2).
* **Logic:** Trigger a fast-blinking Red LED/Buzzer on Pin 12 if Temp > 50°C **and** Brightness > 220.

### 📍 [Laboratory Activity 4: Arduino Serial Connection](./Laboratory Activity 4)
* **Goal:** Familiarization with Serial connection functions.
* **Logic:** A photoresistor triggers a "sticky" blink on Pin 8 that only stops when the word "stop" (case-insensitive) is entered in the Serial Monitor.

### 📍 [Laboratory Activity 5: Python to Arduino Serial Connection](./Laboratory Activity 5)
* **Goal:** Control an Arduino circuit (RGB LEDs) using a Python-based interface.
* **Logic:** Python script sends toggling commands ('R', 'G', 'B', 'A', 'O') via `pyserial` to control pins 8, 9, and 10.

### 📍 [Laboratory Activity 6: Bidirectional Control](./Laboratory_Activity_6)
* **Goal:** Implement a loopback system between Arduino and Python.
* **Logic:** Buttons send 'R/G/B' to Python, which writes back '1/2/3' to Arduino to toggle the corresponding LEDs.

### 📍 [Laboratory Activity 7: Controlling Arduino using FastAPI](./Laboratory Activity 7)
* **Goal:** Implement an HTTP-based solution for hardware control.
* **Logic:** Using FastAPI endpoints like `/led/{color}` to send serial signals to the Arduino for remote LED management.

---

## 🏆 Laboratory Exams

### [Midterms Laboratory: Smart Outdoor Lighting System](./Midterms)
* **Description:** An intelligent LDR system featuring **Manual** and **Automatic** modes.
* **Key Feature:** Dynamic thresholding based on environmental simulations (Cloudy, Normal, Bright Sunlight).


### [Finals Laboratory: Arduino-to-Python Client System](./Finals)
* **Description:** A remote trigger system that uses a physical button to call a Python program, which then calls a web API.
* **Key Feature:** Software debouncing to ensure one button press equals exactly one API request.


---
*Submitted as a final requirement for COSC 111.*
