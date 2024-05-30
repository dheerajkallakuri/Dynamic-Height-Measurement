# Dynamic-Height-Measurement

## Overview

The Automated Overhead Equipment (OHE) Height Measurement System is designed to dynamically measure the height of OHE cables and detect any lag, which can lead to power supply disruptions and rail traffic issues. The system uses an Arduino-based setup with ultrasonic and GPS sensors to measure and record the height of the OHE cables in real time, storing the data in an Excel sheet for easy access by railway maintenance personnel.

## Table of Contents

1. Introduction
2. Hardware Setup
3. Software Setup
4. Implementation Details
   - Dynamic Readings
   - Stimulus/Response Sequences
   - Functional Requirements
5. Data Storage
6. Usage Instructions
7. Precise Location

## Introduction

Monitoring the height of overhead electrification (OHE) cables is crucial to prevent power supply disruptions caused by cable lag. Traditionally, this measurement is performed manually, which is time-consuming and requires blocking the rail line. This project automates the process using an Arduino setup equipped with ultrasonic and GPS sensors, enabling dynamic measurement and pinpointing locations requiring maintenance.

## Hardware Setup

1. **Arduino**: The central microcontroller unit.
2. **Ultrasonic Sensor**: Measures the distance between the top of the train bogey and the OHE cable.
3. **GPS Sensor**: Provides the precise location of each measurement.
4. **Reflector Plates**: Enhances the accuracy of the ultrasonic sensor by reflecting the ultrasonic waves.
5. **Serial Port Communication**: Used for interfacing the Arduino with a computer to retrieve sensor data.

### Connection Diagram

- Connect the ultrasonic sensor to the appropriate pins on the Arduino.
- Connect the GPS sensor to the Arduino.
- Attach the reflector plates to the relevant positions to ensure accurate measurements.
- Establish a serial connection between the Arduino and a computer.

## Software Setup

1. **Operating System**: Windows 7
2. **Development Environment**: Visual Studio 2017, Arduino IDE
3. **Programming Languages**: Embedded C, C#
4. **Libraries**:
   - `newping.h` for ultrasonic sensor handling
   - `tinygps` for GPS sensor handling

### Installation Steps

1. **Install Arduino IDE**: Download and install the Arduino IDE from the official website.
2. **Install Visual Studio 2017**: Download and install Visual Studio 2017.
3. **Install Necessary Libraries**:
   - In the Arduino IDE, use the Library Manager to install `newping.h` and `tinygps`.

## Implementation Details

### Dynamic Readings

Dynamic readings are crucial for real-time monitoring of OHE cable height. As cable lag increases over time, timely measurements are necessary to prevent power disruptions. The system continuously records the height of the OHE cables and logs the data with timestamps and GPS locations.

### Stimulus/Response Sequences

1. **Login**: The administrator logs into the system.
2. **Start Measurement**: Click the "START" button to begin recording values.
3. **Stop Measurement**: Click the "STOP" button to end the recording.
4. **Data Logging**: The recorded values are stored in an Excel sheet, accessible to railway officials for maintenance planning.

### Functional Requirements

- **Ultrasonic Sensor Accuracy**: Occasionally, the ultrasonic sensor may return a '0' value due to poor reflection. The system is designed to retry and obtain accurate readings.
- **GPS Sensor Accuracy**: The GPS sensor may experience delays during a warm start. The system accounts for this and waits for accurate location data before logging.

## Data Storage

All sensor readings, including OHE height, location, and timestamp, are stored in an Excel sheet. This data is crucial for identifying and addressing areas where the OHE cable height needs adjustment.

## Usage Instructions

1. **Power On**: Connect the Arduino setup to the power source.
2. **Run the Application**: Open the Visual Studio project and run the application.
3. **Login**: Enter administrator credentials to access the system.
4. **Start Measurement**: Click the "START" button to begin capturing data.
5. **Stop Measurement**: Click the "STOP" button to end data capture.
6. **Access Data**: Open the generated Excel sheet to view the recorded measurements and locations.

## Precise Location

The system uses GPS data to provide precise locations for maintenance activities. This feature enables maintenance personnel to quickly locate and address issues with the OHE cables, significantly improving efficiency compared to manual methods.

## Links

- ![Presentation Preview](Presentation.pdf)
- ![Report Preview](Report.pdf)

