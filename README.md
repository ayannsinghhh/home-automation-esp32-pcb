# home-automation-esp32-pcb
# 🏠 ESP32-Based Home Automation PCB

## 📌 Overview

This project is a custom-designed **home automation PCB** built using an ESP32, aimed at controlling multiple household appliances through relay switching.

Instead of using off-the-shelf relay modules, the system is designed from scratch at the circuit level — including relay driving, power conversion, and proper interfacing.

---

## ⚙️ System Architecture

The PCB integrates three main sections:

### 🔌 Power Supply

* AC input (Live & Neutral)
* Fuse protection (250mA)
* AC-DC conversion using HLK-PM01 module
* Regulated +5V output for the system

### 🧠 Controller Unit

* ESP32 DevKit (main controller)
* GPIO pins used to control relay drivers
* I2C interface for sensors (future expansion)

### ⚡ Relay Driver Section

Each appliance is controlled through an independent relay circuit:

* BC547 transistor used as a switch
* 1N4007 diode for flyback protection
* LED indicators for relay status
* 5V relay modules (G5LE-1 type)

This ensures:

* Safe switching of high-voltage loads
* Protection of ESP32 from back EMF

---

## 🔌 Output Connections

* Screw terminals provided for REL1 to REL5 (appliance outputs)
* Separate Live connections for each relay
* Designed for practical home wiring

---

## 📡 Expandability

* I2C header (SDA, SCL) for future sensors
* DHT sensor interface
* Modular approach for adding IoT features (Blynk/MQTT)

---

## 🧠 Design Understanding

This PCB was designed with a focus on:

* Proper separation of low voltage (ESP32) and high voltage (AC load)
* Reliable relay switching using transistor drivers
* Clean and scalable architecture for future upgrades

---

## ⚠️ Safety Considerations

* Fuse added for input protection
* Flyback diodes across relay coils
* Care required while handling AC mains

---

## 🛠️ Tools Used

* KiCad for schematic and PCB design
* ESP32 for control logic

---

