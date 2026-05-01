# ThermoGuard — CDEC (Compact Dashboard Evaporative Cooler)

A standalone retrofit evaporative cooling device for parked cars —
designed to prevent heat-related fatalities caused by extreme cabin
temperatures when a vehicle is completely OFF.

Submitted to **Varroc Eureka Challenge 3.0** — a national-level
automotive innovation hackathon. Result awaited.

Team Name: **Scrum and Coke**
Team: 4 members — Sri Sairam Engineering College, Chennai (B.E. CSE 2027)

---

## Problem Statement

Parked cars under direct sunlight reach internal temperatures of
65-70°C within 60 minutes (NREL Vehicle Thermal Study). VOC levels
inside the cabin are 6x higher at 60°C vs 25°C. Every existing
solution requires the car to be ON. CDEC is built for the car
completely OFF.

---

## Solution — How CDEC Works

Dual 90mm DC fans push hot cabin air through a water-saturated
CELdek honeycomb pad. Evaporation absorbs heat — outlet air cools
to approximately 31-34°C (within 3°C of ambient).

Water feeds from a 1.5L top tank by gravity through a cotton wick.
No pump. Pure physics. Zero mechanical failure.

ESP32 reads DHT22 sensor every 60 seconds and activates fans only
when needed using 3-condition thermostat logic to maximise battery life.

**Decision Logic:**
- Humidity > 80% → FAN OFF (Monsoon Mode)
- Temp > 42°C → FAN ON (Safety Override)
- Temp - Base > 5°C → FAN ON (Normal Cooling)
- Temp <= Base + 2°C → FAN OFF (Target Reached)

---

## Key Features

- Zero car battery dependency — runs on its own 18650 battery pack
- Charges via car USB while driving or at home
- 8x cheaper than nearest competitor
- 50-70x more airflow than rival products
- Retail price: Rs. 1,999
- Universal retrofit — installs in 2 minutes, no tools needed
- 16.5 hours runtime per charge

---

## Hardware Stack

- Microcontroller: ESP32
- Sensor: DHT22 (Temperature + Humidity)
- Fans: 2x 90mm DC fans (BC547 transistor switching)
- Cooling Pad: CELdek honeycomb evaporative pad
- Power: 3x 18650 Li-ion battery pack (27.75 Wh)
- Charging: TP4056 charge controller via USB Type-C
- Boost Converter: MT3608 (Battery to 5V rail)

---

## Simulation

Built and simulated using **Wokwi** — an online ESP32/Arduino simulator.

Watch simulation: [View Simulation Video](https://youtube.com/shorts/Nz4vqkCiKiw)

---

## Product Design

<img width="961" height="815" alt="Photo from Selvamurugan" src="https://github.com/user-attachments/assets/95d56dc9-5442-4921-964a-0a5214abb87a" />
<img width="1600" height="1131" alt="Photo from Selvamurugan (3)" src="https://github.com/user-attachments/assets/6ffc2946-1d28-42cb-af72-bca0f97ba141" />
<img width="1600" height="1131" alt="Photo from Selvamurugan (2)" src="https://github.com/user-attachments/assets/a8a4a6d4-58ae-44ba-a53c-0b9230adb64a" />
<img width="1600" height="1131" alt="Photo from Selvamurugan (1)" src="https://github.com/user-attachments/assets/1891869e-b4b0-4112-a0e3-6792de80682b" />


Dimensional drawings — 260mm x 280mm (front), 120mm x 280mm (side)
Water tank: 1.5L capacity
Removable collection tray at base

---

