# EV BMS CANoe Simulation

> Distributed Battery Management System (BMS) simulation for Electric Vehicles using **Vector CANoe** and **CAPL**.

![Platform](https://img.shields.io/badge/Platform-Vector_CANoe-blue)
![Language](https://img.shields.io/badge/Language-CAPL-green)
![Protocol](https://img.shields.io/badge/Protocol-CAN-orange)
![Domain](https://img.shields.io/badge/Domain-Automotive-red)
![Status](https://img.shields.io/badge/Status-Completed-success)

---

## Overview

This project simulates a distributed **Battery Management System (BMS)** architecture for an electric vehicle using **Vector CANoe** and **CAPL**.

Developed during an engineering internship, the simulation reproduces CAN communication between multiple Electronic Control Units (ECUs) responsible for battery supervision, thermal management, charging, and cell balancing.

The objective was to design a realistic embedded automotive simulation while solving several software architecture and CAPL programming challenges.

<img width="1920" height="1080" alt="Capture d&#39;écran 2026-07-17 152630" src="https://github.com/user-attachments/assets/bd8d14c6-feb7-4af7-90c0-94ebbf0ed02e" />

---

## Features

- Distributed BMS architecture
- Multi-ECU CAN communication
- Battery State of Charge (SOC) monitoring
- Cell voltage monitoring
- Temperature monitoring
- Battery balancing logic
- Thermal management simulation
- Charger simulation
- CAPL event-driven programming
- DBC-based signal communication
- Real-time monitoring in CANoe

---

# System Architecture

<img width="1536" height="1024" alt="BMS" src="https://github.com/user-attachments/assets/5bf192e3-ebf3-4530-8e8b-ae851d65043e" />

---

## ECU Description

### BMS

- Central Battery Management Unit
- Battery supervision
- CAN communication coordinator
- SOC calculation
- Decision making

### BATTDOC

- Battery monitoring
- Diagnostic information
- Cell balancing management
- Battery status reporting

### BMS Controller

- Control algorithms
- State machine management
- Coordination between ECUs

### Thermal System

- Battery temperature monitoring
- Cooling management
- Thermal protection

### Charger

- Charging process simulation
- Charging state management
- Communication with BMS

---

# Technologies

- Vector CANoe
- CAPL
- CAN Bus
- DBC Databases
- Automotive Embedded Systems

---

## Database Files

```
PowerTrain.dbc
BMS_CAN_Database.dbc
```

---

# Project Structure

```
EV_BMS_CANoe
│
├── CAPL/
│   ├── BMS.can
│   ├── BATTDOC.can
│   ├── BMS_Controller.can
│   ├── Thermal_System.can
│   └── Charger.can
│
├── DBC/
│   ├── PowerTrain.dbc
│   └── BMS_CAN_Database.dbc
│
├── dashboard/
│
│
└── README.md
```

# Skills Demonstrated

- Embedded Software Development
- Automotive Software Architecture
- CAPL Programming
- CAN Communication
- Vector CANoe
- Event-Driven Programming
- State Machine Design
- DBC Integration
- Debugging Complex Embedded Systems
- Battery Management Systems
- Electric Vehicle Software
