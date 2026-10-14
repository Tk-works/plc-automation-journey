# Roadmap

| Stage | Topics | Platform | Programme phase |
|---|---|---|---|
| 01 | PLC architecture, scan cycle, contacts and coils | CODESYS simulation | 1 |
| 02 | Boolean logic, NO vs NC, fail-safe stop buttons | CODESYS simulation | 1 |
| 03 | Latching (seal-in, SET/RESET), edge detection, toggle | Simulation → **first ESP32-S3 build (OpenPLC)** | 2 |
| 04 | Timers (TON/TOF/TP), counters (CTU/CTD) | Simulation + ESP32-S3; STM32F4 C runtime begins | 2 |
| 05 | Interlocks, permissives, motor start/stop, forward/reverse | Simulation | 2–3 |
| 06 | Sequencing: state machines, SFC, traffic light, conveyor | Simulation (+ Factory I/O trial) | 2–4 |
| 07 | Analogue: scaling, hysteresis, filtering, alarms, PID intro | ESP32-S3 / STM32F4 ADC + simulation | 3 |
| 08 | Structured Text, function blocks, FBD, fault handling | CODESYS (+ TwinCAT 3) | 4 |
| 09 | Modbus RTU/TCP, HMI, SCADA basics, troubleshooting | CODESYS ↔ ESP32-S3 / STM32F4 | 5 |
| 10 | Integrated capstone project(s) | All | 6 |

## Hardware tracks

- **ESP32-S3 + OpenPLC** — ladder logic running on real low-voltage I/O.
- **STM32F4 PLC runtime (C)** — build the internals of a PLC myself: input/output image tables, fixed-period scan driven by a timer interrupt, watchdog, IEC-style timers and edge detection, later a Modbus RTU slave.

## Planned free/student resources

- Ask the UCT Electrical Engineering department about Siemens SCE (TIA Portal) licences, PLC trainers and Factory I/O licences.
- Check UCT ICTS for MATLAB/Simulink access (Simulink PLC Coder).
- Siemens SCE training material (free to read).
