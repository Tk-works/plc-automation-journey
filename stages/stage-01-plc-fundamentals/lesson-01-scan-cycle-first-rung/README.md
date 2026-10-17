# xLesson 01 — The scan cycle and your first rung

**Stage:** 01 PLC fundamentals · **Platform:** CODESYS simulation · **Hardware:** none
**Status:** 🟡 In progress · **Started:** 2026-10-14

## Learning objectives

* \[ ] Explain the PLC scan cycle and why it matters in industry
* \[ ] Read three ladder symbols: NO contact, NC contact, coil
* \[ ] Build, simulate and test a push button → lamp rung

## Key concept: the scan cycle

1. **Read inputs** into the input image
2. **Execute logic**, top to bottom, using only that snapshot
3. **Write the output image** to the physical outputs, all at once
4. **Housekeeping** (communications, diagnostics), then repeat

Embedded analogy: a superloop that reads all inputs into a struct at the top, computes, then writes all outputs at the end.

## Symbols

```
 -| |-   NO contact (XIC): passes power when its bit is TRUE
 -|/|-   NC contact (XIO): passes power when its bit is FALSE
 -( )-   Coil (OTE):       sets its bit TRUE when the rung has power, FALSE otherwise
```

## Exercise: push button → lamp

```
 |    PB\\\_Start                         Lamp     |
 |-----| |-----------------------------( )------|
```

Equivalent C: `Lamp = PB\\\_Start;` · Equivalent ST: `Lamp := PB\\\_Start;`

Declarations:

```iecst
PROGRAM PLC\\\_PRG
VAR
    PB\\\_Start : BOOL;   // simulated momentary push button
    Lamp     : BOOL;   // simulated lamp output
END\\\_VAR
```

Save the project to [`codesys/`](codesys/) and screenshots to [`screenshots/`](screenshots/).

## Test results

|#|Action|Expected PB\_Start|Expected Lamp|Observed Lamp|Pass?|
|-|-|-|-|-|-|
|1|Start PLC, no input|FALSE|FALSE|FALSE|YES|
|2|Write PB\_Start = TRUE|TRUE|TRUE|FALSE|NO|
|3|Write PB\_Start = FALSE|FALSE|FALSE|TRUE|NO|
|4|Write TRUE twice|TRUE|TRUE (no toggle)|TRUE|YES|
|5|Stop PLC, then write PB\_Start = TRUE|TRUE|*predict*|SAME AS BEFORE STOP|YES|

## Troubleshooting notes

|Problem|Cause|Fix|
|-|-|-|
|"No gateway/device" on login|Simulation not ticked|Online → Simulation|
|Nothing updates|PLC in STOP|F5|
|Value doesn't change|Prepared value not written|Ctrl+F7|
|"Identifier not defined"|Typo or missing declaration|Check the VAR block|
|Simulated button stays on|Written values persist|Expected; a real push button springs back|

## Quiz and challenge

* Predictions: [Quiz 01](../../../assessments/quizzes/quiz-01-scan-cycle.md)
* Challenge: Lamp ON only when **PB\_A AND PB\_B** are both pressed. Save the solution in [`codesys/`](codesys/) and add a screenshot.

## Reflection

*What I learned, what surprised me, mistakes I made:*
Understanding the PLC scan cycle is quite important. Especially in debugging PLC logic and writing code with apparent bugs. Also in the stop mode values may be written in memory as long as we are logged in but the scan cycle stops. This means output scan as was before stop. This is quite important because behavior in stop mode has to be defined to avoid accidents. One of my mistakes was thinking a 10 ms scan cycle can see 3 ms pulses between sensor reads, but it does not, because during the pulses the cycle is not active.

