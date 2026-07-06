# Water Level Control System (S7-1200 & Factory I/O)

A clean, industrial-grade automation project featuring closed-loop (two points) analog level control. This repository contains the complete source code and logic for a simulated water tank system.

## 🚀 Key Features & Engineering Logic

* **Analog Signal Processing:** Uses `NORM_X` and `SCALE_X` blocks to convert 0-10V analog sensor data into precise physical values (0.0 to 300.0 cm).
* **Dynamic Anti-Cycling Logic via HMI:** Implements a `SET / RESET` flip-flop architecture where the Low and High thresholds are dynamically inputted by the operator directly from the HMI screen. The filling valve is triggered below the Low Setpoint (preventing pump cavitation) and isolates once it hits the High Setpoint (preventing overflows).
* **Safety Interlocking (State-Trap Prevention):** Prevents accidental machine startups. The system forces the operator to switch to `AUTO` mode *before* a `START` command can be executed.
* **Power-Up Safety Interlocking:** Ensures the system initializes in a safe Standby state upon power-up. Even if the switch is set to `MANUAL`, it strictly requires an explicit `START` command to activate manual control, preventing accidental valve actuation.

## 🛠️ Technology Stack

* **PLC:** Siemens S7-1200 (TIA Portal)
* **HMI:** WinCC Comfort
* **Simulation:** Factory I/O (Water Tank)

---
*Developed by Le Quoc Bao - Student at Ho Chi Minh City University of Technology (HCMUT).*
