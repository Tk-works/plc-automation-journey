# Hardware tracks

| Track | Board | Purpose | Starts |
|---|---|---|---|
| [esp32-s3-openplc](esp32-s3-openplc/) | ESP32-S3 | Ladder logic on real low-voltage I/O via OpenPLC; Modbus TCP over Wi-Fi later | Stage 03 |
| [stm32f4-plc-runtime](stm32f4-plc-runtime/) | STM32F4 / Black Pill | My own PLC runtime in C: I/O image, timer-driven scan, watchdog, TON, edges, Modbus RTU | Stage 04 |
| [wiring-diagrams](wiring-diagrams/) | — | Schematics and breadboard diagrams for every physical build | — |

**MCU ≠ PLC.** These boards have 3.3 V logic, no isolation and no surge protection, and they are not certified. They are for learning only.
