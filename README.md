## Overview

This project presents a **custom Power Distribution Board (PDB)** designed for **multirotor drones**.  
The board ensures reliable, efficient, and safe power management between the **battery**, **Motors**, **flight controller**, and **auxiliary modules** such as Workswell Camera, Doodle labs mesh radio, and Gremsy Gimbal.

 <img width="692" height="545" alt="image" src="https://github.com/user-attachments/assets/7d12bdc8-25ee-4bb1-804f-6e1f56bb7d6a" />


The design prioritizes:
- Efficient DC-DC conversion
- Compact integration for UAV frames
- High current capacity and thermal stability
- Modular multi-voltage support (28 V, 22.2 V, 12 V, 5 V)

## Features
- **Input Voltage:** 48 V 
- **Power Outputs:**
  - 1x Motor Output (28 V / 5 A)
  - 1x Workswell Camera (22.2 V / 0.8108 A)
  - 1x Gremsy Gimbal (12 V / 4 A)
  - 1x Doodle labs mesh radio (5 V / 1 A)
  - 1x Flight Controller (5 V / 2.5 A)
- **Voltage Regulators:**
  - Buck converter : XL4015(28V , 12V rail) and LMR50410(22.2V and 5V rail)
- **Protection Features:**
  - Reverse polarity protection (MOSFET or diode)

## Components 

- XT60 Connector
- XL4015
- LMR50410
- Schottky Diode (1N5822)


## Schematic

<img width="1287" height="768" alt="image" src="https://github.com/user-attachments/assets/6798a080-8fe2-4dc1-b33e-f95f46081fba" />

## Functional Description

###  Input Stage
**Vin = 48 V** DC main bus  

### Output Stages
1. **U6 (XL4015)** → 48 V → 28 V @ 5 A  

2. **U4 (XL4015)** → 48 V → 12 V @ 4 A  

3. **U2 (LMR50410)** → 48 V → 22.2 V @ 0.8 A  

4. **U5 (LMR50410)** → 48 V → 5 V @ 2.5 A  

5. **U3 (LMR50410)** → 48 V → 5 V @ 1 A  

