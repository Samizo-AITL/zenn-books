---
title: "【Control Design】Why a 10% Deviation Is the Right Trigger for FSM in PID Systems"
emoji: "🎛️"
type: "tech"
topics: ["control", "PID", "FSM", "reliability", "industrial"]
published: true
---

## Introduction

In many industrial control systems, PID control is often sufficient for long-term operation.  
However, modern designs increasingly add FSM-based supervision or adaptive logic.

This article explains **why FSM should NOT be always active**,  
and why **a 10% deviation from the initial PID response is a practical and defensible trigger**.

The discussion is based on **commercial constraints**, not academic optimality.

---

## The Core Design Philosophy

The hierarchy is simple:

1. **PID is the primary controller**
2. **FSM is a safety mechanism, not an optimizer**
3. **Reliability Guard exists to stop FSM from making things worse**

FSM should only intervene when **the system behavior clearly deviates from its expected baseline**.

---

## Why FSM-First Designs Fail in Practice

Aggressive FSM insertion often causes:

- Excessive mode switching
- Artificial waveform distortion
- Control authority fragmentation
- Loss of predictability

In extreme cases, FSM **degrades performance faster than plant aging itself**.

This is not a theoretical issue — it is a field failure pattern.

---

## Establishing a Quantitative Trigger

### Why Not Always-On FSM?

Because plant degradation is:
- Slow
- Continuous
- Often tolerable within PID margins

FSM activation must therefore be **event-driven**, not time-driven.

---

## Why 10% Deviation?

### Empirical Observation from a Typical Aging Model

Using a standard friction-aging plant model:

- PID response after **~5 years equivalent aging**
- Shows approximately **10% deviation** from the initial waveform
  - Amplitude
  - Phase
  - Energy consumption

This provides a **natural engineering reference**, not an arbitrary number.

---

## What Does "10% Deviation" Mean?

The deviation can be defined using **OR logic**:

FSM is triggered if **any** of the following exceeds 10%:

- Amplitude deviation
- Phase / timing deviation
- Control effort deviation

> **AND conditions are too strict and delay intervention dangerously.**

---

## Why OR Logic Is Essential

Unexpected degradation can cause:

- Sudden friction increase
- Partial actuator failure
- Environmental contamination

These events can compress *years of degradation into months*.

OR logic ensures:
- Fast response
- Predictable intervention
- Clear explainability to customers

---

## The Role of Reliability Guard (B-Type)

FSM itself can cause harm.

Therefore, B-Type control introduces a **Reliability Guard**:

- Limits FSM authority
- Penalizes control effort escalation
- Allows graceful fallback to PID dominance

FSM is allowed to act —  
but **not allowed to destabilize**.

---

## Commercial Perspective: What Customers Expect

From a customer viewpoint:

- PID works for years → acceptable
- FSM activates only when deviation is visible → acceptable
- Sudden behavior change without explanation → unacceptable

The **10% rule** is explainable, defensible, and auditable.

---

## Summary

- PID should remain the default controller
- FSM should activate only after **observable deviation**
- 10% deviation aligns with realistic aging timelines
- OR-based triggers reflect real-world failures
- Reliability Guard protects against overreaction

FSM is not intelligence.  
FSM is **insurance**.

---

## Closing Thoughts

If FSM activates at day zero,  
**your PID is not trusted**.

If FSM activates at 10% deviation,  
**your system behaves like a commercial product**.
