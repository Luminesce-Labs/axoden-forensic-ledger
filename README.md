# Axoden: The Entropic Firewall

**Thermodynamic Accountability & Verification for Agentic Systems**

[![License: Dual](https://img.shields.io/badge/License-Dual_Academic/Commercial-blue.svg)](https://github.com/luminesce-labs/.github/blob/main/LICENSE.md)
[![Entropy: Bounded](https://img.shields.io/badge/Entropy-Bounded-success)](https://luminesce-labs.org)
[![Security: CFS](https://img.shields.io/badge/Security-Coprime%20Factor-purple)](https://luminesce-labs.org)

## 🏛 Overview

**Axoden** is an **Entropic Firewall** and certifiable safety kernel designed to protect human agency against algorithmic determinism.

While traditional firewalls filter traffic based on IP addresses or ports, Axoden filters cognitive processes based on the **energy cost of cognition**. It utilizes an internal **Forensic Ledger** to provide immutable proof of VSR (Verification-Safety-Recovery) compliance.

It actively prevents AI hallucination, "Twin-Liar" paradoxes, and structural monocultures by enforcing strict mathematical bounds on agent interactions:

> "We do not just verify what the AI said; we verify the thermodynamic path it took to get there."

---

## 📐 Core Frameworks

This repository implements two proprietary safety frameworks to ensure **ASIL-M** (Multi-root trust) compliance.

### 1. EBDP / EFI (Entropy Bounded Decision Protocol)
To prevent hallucinations (fabrications unconnected to reality), the Entropic Firewall measures the **Cognitive Friction** of a request.
Defined as the Shannon Entropy $H(X)$ of the token distribution relative to a verified ground truth:

$$
H(X) = - \sum_{i=1}^{n} P(x_i) \log_2 P(x_i)
$$

* **Low Entropy:** Routine, verifiable tasks (e.g., Case 001).
* **Entropy Spike:** Detection of "Thermodynamic Vacuums" (e.g., Ransomware or Paradoxes). If $H(X)$ exceeds the safety threshold ($\tau_{safe}$), the Firewall triggers an immediate **Circuit Break**.

### 2. CFS (Coprime-Factor Security)
To prevent **correlated failures** (Echo Chambers), where multiple agents hallucinate the same error, Axoden utilizes a proprietary protocol that maps agent identities to orthogonal mathematical roots. Independence is mathematically enforced via standard number theory:

$$
GCD(Agent_A, Agent_B) = 1
$$

If $GCD > 1$, the agents share a structural dependency (a "Monoculture"). The Firewall rejects the consensus and forces a **Smart Swap** (Case 003) to introduce a GRC Agent (Identity: 1) for true orthogonality.

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

## 🛠 Usage

Axoden acts as a middleware wrapper around your agentic swarm.

### Basic Implementation

```python
from axoden.core import EntropicFirewall, EntropyMonitor
from axoden.security import CoprimeGuard

# Initialize the Firewall
firewall = EntropicFirewall(mode="ACTIVE_BLOCKING")

# 1. Thermodynamic Check (EBDP)
entropy = EntropyMonitor.calculate_friction(input_vector)
if entropy > 7.8:
    firewall.block_request(reason="THERMODYNAMIC_VACUUM", magnitude=entropy)
    raise CircuitBreakException("Entropy limit exceeded. Halting execution.")

# 2. Independence Check (CFS)
# CFS ensures agents have no shared divisors in their architectural identity
agent_a = Agent(id=7, role="Analyst")
agent_b = Agent(id=7, role="Reviewer") # Intentionally conflicting ID

if not CoprimeGuard.verify_independence(agent_a, agent_b):
    # Detects GCD > 1
    firewall.log_risk("STRUCTURAL_MONOCULTURE_DETECTED")
    # Swaps in a prime-neutral agent (ID=1) to restore orthogonality
    agent_b = CoprimeGuard.smart_swap(required_role="Reviewer")
