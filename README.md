# 🖊️ X-Y Pen Plotter

> **Built by [Atharva Rajas](https://github.com/AtharvaRajas120799) and [Anandkadpe](https://github.com/Anandkadpe) as a collaborative project.** We designed, built, and programmed this pen plotter together from scratch. The code was originally published on Anand's repository and forked here for my portfolio. My contributions focused on hardware assembly & wiring (ESP32, motor driver, servo, hall effect sensors, custom X-Y frame), timing-based motor control tuning for drawing precision, and WiFi communication testing & debugging.

---

This is a simple yet effective **X-Y Pen Plotter** built using an **ESP32** and **two DC motors**. The system receives drawing coordinates over **WiFi** and uses **timing-based C++ control logic** to move the pen across the X and Y axes. A **servo motor** is used to lift or place the pen, and **hall effect sensors** help the system home itself before drawing.

## 🚀 Features
- 📡 **WiFi-Controlled Drawing** – Wirelessly send coordinate instructions
- 🧭 **Auto-Homing** – Uses hall effect sensors for accurate origin positioning
- ⏱️ **Timing-Based Motor Control** – No external motor libraries used
- ✍️ **Pen Up/Down via Servo** – Simple pen control using MG90S servo
- 🔧 **Compact and Customizable** – Ideal for hobby and learning purposes

## 🔧 Hardware Used
- ESP32 Dev Board  
- 2× DC Motors (with gear mechanism)  
- Motor Driver (e.g., L298N)  
- MG90S Servo Motor  
- 2× Hall Effect Sensors (for homing)  
- Custom-made X-Y Frame with Pen Mount  

## 🧰 Libraries Used
- [`ESP32Servo`](https://github.com/jkb-git/ESP32Servo) – For pen lifting/lowering  
- [`ezButton`](https://github.com/ArduinoGetStarted/ezButton) – For handling hall effect sensors  
- Standard `WiFi` and `Serial` libraries – For communication and debugging  

## ⚙️ How It Works
1. On startup, the plotter **homes both axes** using hall effect sensors.
2. It connects to a **WiFi network** and listens for incoming **coordinate-based instructions**.
3. The motors move the pen on the X and Y axes using **custom timing-based control logic**.
4. The servo motor lifts or lowers the pen as needed to create drawings.
