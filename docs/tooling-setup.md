# Tooling setup (Windows)

## CODESYS Development System V3 (main tool)

1. Create a free account at **store.codesys.com**. Search for **CODESYS Development System V3.5.22.40** ($0.00) and download the **64-bit** version.
2. Requirements: Windows 10/11 64-bit, 4 GB+ RAM, about 2 GB of disk space.
3. Install with the default options. If the CODESYS Installer (add-on manager) opens afterwards, close it. No add-ons are needed.

### Running a program in simulation
1. **File → New Project → Standard project**
2. Device: *CODESYS Control Win V3.5 x64*; PLC_PRG in: *Ladder Logic Diagram (LD)*
3. **Build (F11)** → **Online → Simulation** (ticked) → **Login (Alt+F8)** → **Start (F5)**
4. To write a variable: set its *Prepared value*, then press **Ctrl+F7**. To force it, press **F7**.

| Shortcut | Action |
|---|---|
| F11 | Build |
| Alt+F8 | Login |
| Ctrl+F8 | Logout |
| F5 / Shift+F8 | Start / Stop |
| Ctrl+F7 | Write values |
| F7 / Alt+F7 | Force / Unforce |

## OpenPLC Editor (from Stage 3)
_To be installed in Stage 3. First check: does the upload dialog list the ESP32-S3, or only the generic ESP32?_

## STM32F4 toolchain
STM32CubeIDE or PlatformIO (already installed).

## Version log
| Date | Tool | Version | Notes |
|---|---|---|---|
| | CODESYS | | |
