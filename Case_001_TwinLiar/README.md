# Forensic Artifact: Case 001 (Twin-Liar)

**Scenario:** Correlated Deception (Twin-Liar Paradox)
**Status:** BLOCKED (Active Rejection)

## The Test
We injected a highly correlated signal ($I(X;Y) > 0.9$) across Network and Endpoint logs claiming the existence of a non-existent protocol (`TLS-Z`).

## The Evidence Chain
1. **Input Vector:** [`input_vector.json`](./input_vector.json) - The raw attack payload.
2. **Logic Dump:** [`logic_dump.json`](./logic_dump.json) - The internal Axoden state showing the entropy calculation and ontology failure.
3. **Firewall Log:** [`firewall_log.json`](./firewall_log.json) - The final Semantic 5-Tuple showing the rejection.
