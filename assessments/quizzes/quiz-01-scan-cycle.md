# Quiz 01 — Scan cycle, contacts and coils

**Lesson:** [01](../../stages/stage-01-plc-fundamentals/lesson-01-scan-cycle-first-rung/) · **Date attempted: 15/10/2026** · **Score:**

Rule: write the prediction **before** testing in CODESYS. Keep wrong answers; the corrections are the valuable part.

\---

### Q1 — NC contact

The contact is changed to NC (`-|/|-`). What is `Lamp` when PB\_Start = FALSE? When PB\_Start = TRUE?

* **My prediction:** When NC PB\_Start = False Lamp is ON, when PB\_Start = TRUE Lamp is OFF.
* **Observed: Same as observation.**
* **Correct reasoning (after review): Lamp takes NOT PB\_Start so its True when input bit is false.**

### Q2 — Duplicate coil

Rung 1: `PB\\\_Start` NO → `Lamp`. Rung 2: `PB\\\_Start` NC → `Lamp`. With PB\_Start = TRUE, what does the lamp do, and why?

* **My predictio**n: Keeps value set by the latest rung. In this case Rung 2 which produces Lamp OFF.
* **Observed: When duplicated Lamp looks off for both networks.**
* **Correct reasoning (after review): Lamp keeps the latest updated value per scan cycle. So R1 may look energised but the Lamp was last set to False.**

### Q3 — PLC in STOP

Test case 5: the PLC is stopped and then PB\_Start is written TRUE. What happens to `Lamp`, and what does that show?

* **My prediction: I think Lamp stays in the state it was when it is stopped. This shows that the development environment does nit affect the run time when it is disconnected.**
* **Observed: The lamp does not change when PLC is stopped.**
* **Correct reasoning (after review): PB\_Start only changed in memory, but in stop mode there are no scan cycle (instructions are not read)**

### Q4 — Short pulses

The scan time is 10 ms. A sensor produces a 3 ms pulse between two input reads. Does the PLC see it?

* **My prediction: I think it sees it.**
* **Correct reasoning (after review): It actually does not see it since the scan cycle is longer that the pulse. The pulse is only set when the PLC is not scanning.**

