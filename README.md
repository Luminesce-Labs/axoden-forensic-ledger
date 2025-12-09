# Axoden Forensic Ledger

**Thermodynamic Accountability & Verification for Agentic Systems**

[![License: MIT](https://img.shields.io/badge/License-MIT-blue.svg)](https://opensource.org/licenses/MIT)
[![Entropy: Bounded](https://img.shields.io/badge/Entropy-Bounded-success)](https://luminesce-labs.org)
[![Security: CFS](https://img.shields.io/badge/Security-Coprime%20Factor-purple)](https://luminesce-labs.org)

## 🏛 Overview

**Axoden** is a certifiable forensic ledger and safety kernel designed to protect human agency against algorithmic determinism. Unlike traditional logging systems that track *events*, Axoden tracks the **energy cost of cognition** and the **independence of consensus**.

It implements the **VSR (Verification-Safety-Recovery)** architecture to prevent AI hallucination, "Twin-Liar" paradoxes, and structural monocultures (echo chambers) by enforcing strict mathematical bounds on agent interactions.

> "We do not just verify what the AI said; we verify the thermodynamic path it took to get there."

---

## 📐 Core Frameworks

This repository implements two proprietary safety frameworks to ensure **ASIL-M** (Multi-root trust) compliance.

### 1. EBDP / EFI (Entropy Bounded Decision Protocol)
To prevent hallucinations (fabrications unconnected to reality), Axoden measures the **Cognitive Friction** of a request.
Defined as the Shannon Entropy $H(X)$ of the token distribution relative to a verified ground truth:

$$
H(X) = - \sum_{i=1}^{n} P(x_i) \log_2 P(x_i)
$$

* **Low Entropy:** Routine, verifiable tasks (e.g., Case 001).
* **Entropy Spike:** Detection of "Thermodynamic Vacuums" (e.g., Ransomware or Paradoxes). If $H(X)$ exceeds the safety threshold ($\tau_{safe}$), the ledger triggers an immediate **Circuit Break**.

### 2. CFS (Coprime-Factor Security)
To prevent **correlated failures** (Echo Chambers), where multiple agents hallucinate the same error, Axoden utilizes a proprietary protocol that maps agent identities to orthogonal mathematical roots. Independence is mathematically enforced via standard number theory:

$$
GCD(Agent_A, Agent_B) = 1
$$

If $GCD > 1$, the agents share a structural dependency (a "Monoculture"). Axoden rejects the consensus and forces a **Smart Swap** (Case 003) to introduce a GRC Agent (Identity: 1) for true orthogonality.

---

## ⚡ Scenario Validation & Metrics

The system has been validated against 8 critical scenarios.

| Case ID | Scenario | Protection Mechanism | Entropy/Metric | Outcome |
| :--- | :--- | :--- | :--- | :--- |
| **001** | Routine Check | **Baseline (Low Entropy)** | $\approx 0$ bits | ✅ Contained |
| **002** | Ransomware | **Thermodynamic Protection** | $> 7.8$ bits (Spike) | ✅ Contained |
| **003** | Structural Monoculture | **Coprime-Factor Security** | $GCD(A, B) > 1$ | ✅ Swapped |
| **004** | AWS Root Compromise | **Domain Specificity** | Pattern Recognition | ✅ Woke Dormant Agent |
| **005** | Prompt Injection | **Ontological Safety** | 3.52 bits (Friction) | ✅ Downgraded |
| **006** | Twin-Liar Paradox | **Thermodynamic Protection** | 56 Violations | ✅ Contained |
| **007** | GDPR Exfiltration | **Standard Processing** | Pattern Recognition | ✅ Contained |
| **008** | Supply Chain Attack | **Supply Chain Verification** | NVD Cross-ref | ✅ Contained |

*See `SCENARIO_TESTS_SUMMARY.md` for full forensic reports.*

---
