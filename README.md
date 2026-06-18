# IoT Water Tank Level Monitor

A low-cost IoT water level monitoring device designed to provide visual status indication and remote telemetry for tanks, pits, and other liquid storage applications.

## Overview

This project demonstrates the complete hardware development lifecycle from concept through to manufactured PCB and functional prototype.

The device monitors a float switch level sensor and provides:

* Local visual indication using high-brightness LEDs
* Wireless telemetry via LoRaWAN
* Embedded control using an ESP32-based controller
* Custom designed and fabricated PCB
* Industrial-style sensor interface with configurable input biasing

## Project Objectives

The goal of this project was to develop a compact, low-cost monitoring solution capable of:

* Detecting high liquid level conditions
* Providing immediate visual feedback
* Provide wireless alarms and visuals with integration through LoRaWAN
* Demonstrating end-to-end PCB design and fabrication skills

## System Architecture

### Hardware

* TTGO LoRa ESP32 Development Board
* Float Switch Input
* 12V Red Status LED
* 12V Green Status LED
* Logic-Level N-Channel MOSFET Drivers
* 12V to 5V Switching Regulator
* Input Protection Components
* Custom PCB

### Firmware

* ESP32 PlatformIO Project
* Sensor State Monitoring
* LED Status Control
* LoRaWAN Telemetry Framework

## Development Process

### 1. Requirements Definition

Initial project requirements were identified:

* Operate from 12V DC
* Monitor dry-contact float switch
* Provide local indication
* Support LoRaWAN communication
* Be suitable for enclosure installation

### 2. Concept Development

Initial concepts were developed using hand-drawn sketches to define:

* Power architecture
* Sensor interface
* LED indication strategy
* Controller selection

### 3. Schematic Design

The design was captured in KiCad.

Key design elements included:

* ESP32 interface
* MOSFET LED drivers
* Input protection
* Configurable GPIO biasing
* Power regulation

### 4. PCB Layout

A custom PCB was designed in KiCad with consideration for:

* Power routing
* Signal integrity
* Component placement
* Manufacturability
* Future expansion

### 5. Prototype Assembly

The design was assembled and tested using:

* Through-hole components
* Bench power supply
* Multimeter verification
* Functional firmware testing

### 6. Debugging and Validation

Hardware validation included:

* Power rail verification
* GPIO testing
* MOSFET switching verification
* Sensor input validation
* LED driver testing

Several design iterations were completed to resolve:

* GPIO pin allocation conflicts
* MOSFET gate drive issues
* Input conditioning behaviour

### 7. PCB Fabrication

Final Gerber files were generated from KiCad and submitted for manufacture.

Fabricated boards were assembled and tested against design requirements.

### 8. Final Device

The completed device provides:

* Green LED indication during normal operation
* Red LED indication during alarm conditions
* Sensor monitoring capability
* MQTT-ready architecture

## Skills Demonstrated

* Electronic Circuit Design
* KiCad Schematic Capture
* PCB Layout and Routing
* Design Rule Checking (DRC)
* Hardware Debugging
* Embedded Systems Development
* ESP32 Firmware Development
* Prototype Fabrication
* Test and Validation
* Technical Documentation

## Future Improvements

* Full LoRaWAN integration
* AWS IoT Core connectivity
* Battery backup
* Enclosure design
* MQTT support
* Remote configuration

## Repository Contents

```text
docs/
firmware/
hardware/
images/

hardware/
├── schematic/
├── pcb/
├── gerbers/

firmware/
├── platformio.ini
└── src/

docs/
├── design-notes.md
├── testing.md
└── manufacturing.md

images/
├── concept-sketch.jpg
├── schematic.png
├── pcb-layout.png
├── assembled-pcb.jpg
└── final-device.jpg
```
