# power-subsystem

# EEE3088F 2025 Micro-Mouse Project

Welcome to the **EEE3088F 2025 Micro-Mouse Project**! This repository documents the design and implementation process for the **Micro-Mouse power subsystem**. This project is part of the curriculum for the University of Cape Town's EEE3088F course.

---

## Overview

The Micro-Mouse is a **maze-solving robot**. The project focuses on designing and manufacturing the power module while meeting strict **budget, space, and performance requirements**. Other modules, such as the processor, sensing, and motherboard, are pre-designed and provided.

---

## Project Modules

### 1. **Motherboard**  
- Baseboard connecting all PCBs.
- Contains a **2x16 pin header (2.54mm pitch)** for the power module.

### 2. **Processor**  
- Features the **STM32L476 microcontroller** with 78 available pins for interfacing.

### 3. **Sensing System**  
- Detects obstacles using **Time-of-Flight (ToF) sensors**.
- Operates on I2C.

### 4. **Power System**  
- The module you will design to meet specific requirements detailed in the next section.

---

## Power Subsystem Requirements

Your power subsystem must achieve the following:

1. **Motor Control**:  
   - Operate 4 brushed DC motors bidirectionally.  
   - Motors 1 & 2: **200mA each**, auxiliary motors: **500mA each**.

2. **Battery Monitoring**:  
   - Integrate **INA219** on the I2C bus for voltage and current measurement.  
   - Configure hardware correctly (e.g., A0 and A1 pins cannot both be grounded).

3. **Battery Charging**:  
   - Support **slow (200mA)** and **fast (600mA)** charging modes.  
   - Charge from the **9V input pin** and support USB-C integration (outputs **9V from the host**).

4. **Voltage Regulation**:  
   - Provide **5V @ 1.5A** (±5%) with peak current of **2A**.  
   - Provide **3.3V @ 300mA** (±5%).  

5. **Load Switching**:  
   - Support **2 high-side external loads**, each up to **1A**.  

6. **ON/OFF Control**:  
   - OFF state: Battery draw **<30µA**.  
   - ON state: Deliver peak current of **2A**.

---

## Physical and Mechanical Constraints

- **Dimensions**: PCB must fit within **82mm × 60mm**.  
- **Connectors**: Include a **JST PH 2mm pin pitch** connector for the battery.  
- Must align with the **2x16 pin motherboard header**.

---

## Deliverables and Milestones

### **1. PCB Production Files**  
Due: **28 March 2025 (5 PM)**  
Submit a zipped folder containing:  
- Gerber files.  
- Bill of Materials (BOM).  
- Pick-and-Place (PnP) file.  
- Screenshots of BOM and JLCPCB add-to-cart pages.  

### **2. Interim Design Report**  
Due: **25 April 2025 (5 PM)**  
- Document your design choices, specifications, and acceptance testing procedures.  
- Highlight 3 key design decisions with supporting evidence (e.g., calculations, diagrams).  

### **3. Final Demonstration**  
Date: **14 May 2025**  
- Bring all **5 PCB boards** to the lab demonstration.  
- Use the auto-marking jig to verify functionality (e.g., voltage regulation, motor control, charging).

### **4. Final Report**  
Due: **16 May 2025 (5 PM)**  
- Summarize the final design.  
- Present the final schematic and PCB layout with explanations.

