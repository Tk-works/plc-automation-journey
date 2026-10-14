# PLC & Industrial Automation — Learning Journey

A documented, hands-on path from PLC fundamentals to integrated automation projects, built with **free software** and microcontrollers I already own.

> **Author:** Tokelo — final-year Mechatronics Engineering student, University of Cape Town
> **Started:** 14 October 2026
> **Approach:** simulate first (CODESYS), then move to physical low-voltage I/O (ESP32-S3 running OpenPLC, plus an STM32F4 PLC-runtime written in C)

---

## Progress

| Stage | Topic | Status | Completed |
|---|---|---|---|
| 01 | [PLC fundamentals — scan cycle, contacts, coils](stages/stage-01-plc-fundamentals/) | 🟡 In progress | |
| 02 | [Boolean logic, NO/NC, fail-safe stops](stages/stage-02-boolean-logic/) | ⚪ Not started | |
| 03 | [Latching, seal-in, edge detection + first ESP32-S3 build](stages/stage-03-latching-and-edges/) | ⚪ Not started | |
| 04 | [Timers and counters](stages/stage-04-timers-and-counters/) | ⚪ Not started | |
| 05 | [Interlocks and motor control](stages/stage-05-interlocks-and-motor-control/) | ⚪ Not started | |
| 06 | [Sequencing and state machines](stages/stage-06-sequencing/) | ⚪ Not started | |
| 07 | [Analogue signals and process control](stages/stage-07-analogue-signals/) | ⚪ Not started | |
| 08 | [Structured programming (ST, FBD, function blocks)](stages/stage-08-structured-programming/) | ⚪ Not started | |
| 09 | [Industrial communications and HMI](stages/stage-09-industrial-communications/) | ⚪ Not started | |
| 10 | [Integrated projects](stages/stage-10-integrated-projects/) | ⚪ Not started | |

Status key: ⚪ Not started · 🟡 In progress · ✅ Complete

**Latest:** see the [learning log](journal/learning-log.md).

---

## Repository map

```
.
├── stages/                 # One folder per stage; one sub-folder per lesson
│   └── stage-01-plc-fundamentals/
│       └── lesson-01-scan-cycle-first-rung/
│           ├── README.md   # Notes, exercise spec, test results, reflections
│           ├── codesys/    # CODESYS project files (.project)
│           └── screenshots/
├── assessments/
│   ├── quizzes/            # Prediction questions — my answers + corrections
│   ├── challenges/         # End-of-lesson build challenges
│   └── skills-checklist.md # What I can demonstrate, with evidence links
├── projects/               # Integrated, portfolio-grade projects
├── hardware/
│   ├── esp32-s3-openplc/   # OpenPLC on ESP32-S3: pin maps, builds, tests
│   ├── stm32f4-plc-runtime/# My own scan-cycle PLC runtime in C (HAL)
│   └── wiring-diagrams/
├── journal/learning-log.md # Dated session log
├── docs/                   # Roadmap, tool setup, safety notes, glossary, resources
└── templates/              # Templates for lessons, exercises, projects, journal entries
```

## Tools

| Tool | Role | Cost |
|---|---|---|
| CODESYS Development System V3 | Main IEC 61131-3 IDE + simulator | Free |
| OpenPLC Editor | Ladder → ESP32-S3 firmware | Free, open source |
| STM32CubeIDE / PlatformIO | STM32F4 PLC-runtime track | Free |
| Factory I/O (planned, Stage 6) | 3D virtual plant | 30-day trial |
| Beckhoff TwinCAT 3 (planned, Stage 8) | Second CODESYS-based dialect | Free engineering, renewable 7-day runtime trial |

See [docs/tooling-setup.md](docs/tooling-setup.md).

## Safety statement

All physical experiments in this repository use **3.3 V / 5 V low-voltage** electronics only. Microcontrollers here are **learning platforms, not industrial or safety-rated controllers**. Nothing in this repo should be connected to mains voltage, industrial field wiring or contactor coils without proper isolation, rated interface hardware and qualified supervision. See [docs/safety-notes.md](docs/safety-notes.md).

## License

Code and notes: [MIT](LICENSE).
