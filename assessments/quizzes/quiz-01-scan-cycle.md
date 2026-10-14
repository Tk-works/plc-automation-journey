# Quiz 01 — Scan cycle, contacts and coils

**Lesson:** [01](../../stages/stage-01-plc-fundamentals/lesson-01-scan-cycle-first-rung/) · **Date attempted:** · **Score:**

Rule: write the prediction **before** testing in CODESYS. Keep wrong answers; the corrections are the valuable part.

---

### Q1 — NC contact
The contact is changed to NC (`-|/|-`). What is `Lamp` when PB_Start = FALSE? When PB_Start = TRUE?

- **My prediction:**
- **Observed:**
- **Correct reasoning (after review):**

### Q2 — Duplicate coil
Rung 1: `PB_Start` NO → `Lamp`. Rung 2: `PB_Start` NC → `Lamp`. With PB_Start = TRUE, what does the lamp do, and why?

- **My prediction:**
- **Observed:**
- **Correct reasoning (after review):**

### Q3 — PLC in STOP
Test case 5: the PLC is stopped and then PB_Start is written TRUE. What happens to `Lamp`, and what does that show?

- **My prediction:**
- **Observed:**
- **Correct reasoning (after review):**

### Q4 — Short pulses
The scan time is 10 ms. A sensor produces a 3 ms pulse between two input reads. Does the PLC see it?

- **My prediction:**
- **Correct reasoning (after review):**
