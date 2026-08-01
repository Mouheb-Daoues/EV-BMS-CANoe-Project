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

```
                           +--------------------+
                           |        BMS         |
                           |    Master ECU      |
                           +---------+----------+
                                     |
        ---------------------------------------------------------
        |                 |                  |                  |
        |                 |                  |                  |
+----------------+ +----------------+ +----------------+ +----------------+
|    BATTDOC     | | Thermal System | |    Charger     | | BMS Controller |
| Monitoring ECU | |    Cooling     | | Charging ECU   | | Control Logic  |
+----------------+ +----------------+ +----------------+ +----------------+
```

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
├── Panels/
│
├── Configuration/
│
├── Documentation/
│
├── Images/
│
└── README.md
```

---

# Technical Challenges Solved

## 1. CAPL Physical Value Conversion Bug

### Problem

Signal values defined as physical values in the DBC were unexpectedly truncated due to an implicit float-to-integer conversion during assignment.

### Solution

The signal assignment process was redesigned to preserve floating-point precision and eliminate unintended truncation.

---

## 2. Balancing State Machine Race Condition

### Problem

The balancing algorithm occasionally entered inconsistent states because multiple CAPL events were executed simultaneously.

### Solution

The balancing state machine was redesigned to ensure deterministic transitions and proper event synchronization.

---

## 3. Distributed Balancing Architecture

### Problem

Managing balancing decisions across multiple simulated modules introduced synchronization and communication issues.

### Solution

A distributed coordination strategy was implemented, ensuring coherent balancing behavior across all ECUs.

---

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

---

# Future Improvements

- State of Health (SOH) estimation
- Advanced SOC estimation (Kalman Filter)
- Lithium-Ion battery model
- UDS Diagnostics
- Fault injection simulation
- Simulink co-simulation
- CAN FD support
- AUTOSAR integration

---

# Internship Information

**Company**

LATIS

**Period**

June 2026

**Project**

Distributed Battery Management System (BMS) Simulation using Vector CANoe.

---

# Screenshots

Add screenshots of:

- CANoe Simulation Setup
- Network Architecture
- CAN Messages
- Panels
- State Machine
- Balancing Process

Example:

```
/Images
    CANoe_Network.png
    Simulation.png
    Balancing.png
```

---

# Disclaimer

This repository is intended for educational and portfolio purposes.

Some proprietary resources (CANoe configurations, DBC files, or company-specific assets) may not be included due to confidentiality agreements.

---

## Author

**Mouheb Daoues**

Embedded Systems Engineering Student

Double Degree Student – ENSIL-ENSCI & ENISo

Interested in Automotive Embedded Systems, Battery Management Systems, and Electric Vehicle Software.
