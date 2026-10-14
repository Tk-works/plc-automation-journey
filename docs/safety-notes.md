# Safety notes

A running list of industrial safety principles introduced during the course.

## Ground rules for this repository
- Physical experiments use 3.3 V / 5 V low-voltage electronics only.
- The ESP32-S3 is **not 5 V tolerant**. Treat the STM32F4's FT (5 V tolerant) pins as a margin, not a design choice.
- Never connect a microcontroller to mains, 24 V industrial field wiring or a contactor coil without isolation, rated interface hardware and protection.
- Microcontrollers here are learning platforms, **not** industrial or safety-rated controllers.

## Principles learned
| # | Principle | Introduced in |
|---|---|---|
| 1 | Test logic in simulation before it touches anything physical. Standard PLC logic is **control, not safety**: emergency stops are hardwired through certified safety relays or safety PLCs. | Lesson 1 |
