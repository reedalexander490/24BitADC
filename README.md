# README.md

# 24-Bit ADC for Vacuum Chamber Automation

This project involves the design and implementation of a **24-bit Analog-to-Digital Converter (ADC)** used in a vacuum chamber automation setup. The system automates the pumping process by controlling the pressure within the chamber, utilizing a panel for user interaction and an Arduino-based state machine to manage operations based on pressure sensor readings.

## Project Overview

<img width="500" height="535" alt="image" src="https://github.com/user-attachments/assets/273114c3-0f5a-42c7-b6f7-749c71721a93" />

The 24-bit ADC is crucial for accurately monitoring pressure levels in the vacuum chamber. By integrating this ADC into our automation system, we can ensure precise control over the pumping process, enhancing the efficiency and reliability of the vacuum chamber operations. The project includes a control panel for user input and a state machine that responds to pressure changes, allowing for automated adjustments.

## Table of Contents
- [Design Specifications](#design-specifications)
- [Design Solution](#design-solution)
- [Project Results](#project-results)
- [Conclusion](#conclusion)
- [Artifacts](#artifacts)

## Design Specifications

### Performance Requirements
- **ADC Resolution:** 24 bits for high precision
- **Signal Frequency:** 20 Hz for effective monitoring
- **Control System:** Automated pumping up and down based on pressure readings
- **User Interface:** Control panel for manual and automated operations

### Key Performance Metrics
- **Input Voltage Range:** 0-10 V stepped down for Arduino compatibility
- **Communication Protocol:** SPI interface for external ADC communication
- **State Machine Logic:** Arduino-based state machine to manage pressure states
- **Oversampling:** Used to improve signal-to-noise ratio (SNR)

## Design Solution

<img width="661" height="537" alt="image" src="https://github.com/user-attachments/assets/4ae098a3-4341-4575-967b-295fa1018d9a" />

### Overall Assembly
The system consists of a vacuum chamber equipped with a pressure sensor connected to a **24-bit ADC**. The ADC communicates with an Arduino microcontroller via SPI, allowing for real-time pressure monitoring and control.

### Physical Components
- **ADC Model:** **ADC1243** (Delta-Sigma ADC)
- **Operational Amplifier:** **OPA4192** for filtering
- **Regulator:** **REF195** for voltage regulation
- **Resistors:** 0.1% tolerance resistors with potentiometers for voltage trimming to reduce costs
- **Control Panel:** Custom-built panel for user interaction
- **Microcontroller:** Arduino for state machine implementation

### Electronic System
The electronic system includes:
- **Voltage Step-Down Circuit:** Steps down the 0-10 V range to be compatible with the Arduino.
- **ADC Circuit:** Integrated circuit for ADC functionality.

**Diagram of ADC Architecture:**

<img width="604" height="344" alt="image" src="https://github.com/user-attachments/assets/bfda5bd6-2d53-4546-817c-67a0a8cf70e3" />


### Design Summary
The design focuses on achieving high precision with the 24-bit ADC while ensuring reliable communication and control through the Arduino. The system is designed to operate efficiently within the vacuum chamber environment, with a total board cost kept under $100 by using cost-effective components.

## Project Results

The implementation of the 24-bit ADC in the vacuum chamber automation setup has successfully automated the pumping process. The state machine effectively reads pressure data and switches states based on predefined thresholds.

### Testing Observations
- **Initial Testing:** Conducted to verify ADC readings and state transitions.
- **Performance Metrics:** Achieved accurate pressure readings with minimal noise.

## Conclusion

The integration of the 24-bit ADC into the vacuum chamber automation system has proven successful, allowing for precise control over the pumping process. The project demonstrates the effectiveness of using a state machine to manage operations based on real-time pressure data.

### Future Work
- Optimize the state machine logic for improved response times.
- Explore additional features for the control panel to enhance user experience.
- Conduct further testing to validate system performance under varying conditions.

## Artifacts

**Schematic and Simulation of ADC Circuit:**

<img width="698" height="476" alt="image" src="https://github.com/user-attachments/assets/2ae284f6-e6a9-49c6-8f58-06e6ccc5d803" />

<img width="640" height="299" alt="image" src="https://github.com/user-attachments/assets/dc4ded0b-7e90-42b1-8b74-a74f76741e1f" />


**Control Panel Design:**

<img width="309" height="529" alt="image" src="https://github.com/user-attachments/assets/50bc3b6c-c235-4d7e-a51c-3571f39103ef" />

This project exemplifies the application of engineering principles in automation, providing a reliable solution for vacuum chamber operations through precise pressure monitoring and control.


