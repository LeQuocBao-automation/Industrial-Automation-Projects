# Sorting System - S7-1200 & Factory I/O

## Project Description
An automated sorting system controlled by Siemens S7-1200 PLC, simulated in Factory I/O. Focuses on logic reliability and mechanical safety.

## Technical Specifications
* **PLC:** Siemens S7-1200 (PLCSIM).
* **Environment:** Factory I/O (Sorting Station - Basic).
* **Core Logic:**
    * Height-based item categorization.
    * **Interlock:** Prevents Pusher-Conveyor collision.
    * **Timer Logic:** 2s delay after Pusher retraction to stabilize the system before the next cycle.
    * **Refactored Tags:** Clean and optimized I/O mapping for easy maintenance.

## Project Files
* `/Source-Code`: TIA Portal project file (.zap).
* `/Documentation`: IO List and Logic Flowchart.

---
*By Le Quoc Bao - K25 HCMUT*
