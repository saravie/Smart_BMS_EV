#  Smart Battery Management System (BMS) for EV Applications

![STM32](https://img.shields.io/badge/MCU-STM32F407VG-blue) ![ESP32](https://img.shields.io/badge/IoT-ESP32-green) ![Embedded C](https://img.shields.io/badge/Language-Embedded%20C-orange) ![MATLAB](https://img.shields.io/badge/Simulation-MATLAB%20Simulink-red)

##  Overview

A fully functional **Battery Management System** designed for Electric Vehicle (EV) applications, built on the **STM32F407VG** microcontroller. The system monitors a **3S Li-Ion battery pack** in real time, estimates State of Charge (SoC), detects faults, and transmits live telemetry data to a mobile dashboard via **ESP32 and Blynk IoT**.

---

##  Features

- Real-time cell pack voltage and temperature monitoring
- State of Charge (SoC) estimation
- Fault detection and protection logic
- I2C communication for cell monitoring
- UART data logging for debugging and analysis
- ESP32 + Blynk IoT for wireless telemetry dashboard
- MATLAB/Simulink HIL simulation for EV load profile validation

---

##  Hardware Used

| Component | Purpose |
|---|---|
| STM32F407VG | Main microcontroller |
| ESP32 | Wi-Fi telemetry and IoT dashboard |
| Li-Ion Cells (3S) | Battery pack |
| Cell Monitoring sensor | Voltage and temperature sensing via I2C |
| Blynk IoT App | Real-time mobile dashboard |

---

##  Communication Protocols

| Protocol | Usage |
|---|---|
| **I2C** | Cell voltage and temperature monitoring |
| **UART** | Serial data logging and debug output |
| **Wi-Fi (ESP32)** | Wireless data transmission to Blynk cloud |

---

##  System Architecture

```
[Li-Ion 3S Pack]
      │
      ▼
[Cell Monitoring IC] ──I2C──► [STM32F407VG]
                                    │
                              ┌─────┴─────┐
                              │           │
                           [UART]      [GPIO]
                           Logging    Fault Output
                              │
                           [ESP32]
                              │
                           [Blynk IoT Dashboard]
                           (Mobile App)
```

---

##  Software Tools

- **STM32CubeIDE** — Firmware development and flashing
- **Arduino IDE** — ESP32 programming
- **MATLAB Simulink** — HIL simulation under EV load profiles
- **Blynk IoT** — Real-time telemetry dashboard

---

##  Simulation

Validated the BMS design under real EV load profiles using **MATLAB/Simulink Hardware-in-the-Loop (HIL) simulation** to ensure reliability before physical deployment.

---

##  Key Parameters Monitored

- Pack temperature
- State of Charge (SoC) %
- Fault status (overvoltage, undervoltage, overtemperature)

---

##  How to Run

1. Clone this repository
2. Open `BMS_STM32` folder in **STM32CubeIDE**
3. Build and flash to STM32F407VG via ST-Link
4. Open `ESP32_Blynk` folder in **Arduino IDE**
5. Configure your Wi-Fi credentials and Blynk Auth Token
6. Flash to ESP32
7. Open Blynk app to view live telemetry

---

##  Author

**Saravanan Sankar**
B.Tech EEE — Vellore Institute of Technology, Chennai
📧 saravanansankar2917@gmail.com
🔗 [LinkedIn](https://www.linkedin.com/in/saravanan-sankar/)
