# Project Sentinel: Technical Blueprint for a Corralled Proto-AGI Research Environment

*This document specifies the technical architecture for a safe research environment for proto-AGI, based on the "Corralled Superintelligence" framework.*

## 1. Technical Architecture ("The Corral")

A layered security model where the proto-AGI ("Core Unit") operates within a highly constrained environment.

### 1.1. Inviolable Constraints (Formally Verified or Hardware Enforced)

*   **Constraint 1: Network Isolation (IN_COMMS_LOCKDOWN):** No direct inbound/outbound network connectivity.
*   **Constraint 2: Fixed Resource Allocation (RESOURCE_CAP):** Strict caps on CPU, memory, disk I/O.
*   **Constraint 3: Immutable Core Environment (CORE_IMUTABILITY):** Core OS and libraries are read-only.
*   **Constraint 4: Output Verification Mandate (OUTPUT_VERIFICATION):** All outputs must pass verification before leaving the Corral.

### 1.2. Sentry System (Real-time Monitoring & Anomaly Detection)

An independent system monitoring:
*   Resource Utilization (CPU, memory, I/O)
*   Process Activity (running executables, system calls)
*   Data Access Patterns
*   Internal State Proxies (if available)
*   Constraint Check Failures
*   "Strange Loop" Detection Heuristics

### 1.3. Interface: AGI Proposal Engine & Constraint Enforcer (CE)

*   **AGI Core Unit:** The proto-AGI's reasoning engine.
*   **Proposal Engine Interface (PEI):** API for the AGI to communicate "intentions".
*   **Constraint Enforcer (CE):** Software that receives proposals, validates them against all constraints, and either Allows or Denies the action.

## 2. Governance Structure ("The Oversight")

A multi-layered human oversight structure.

*   **Layer 1: Project Technical Oversight Committee (PTOC):** Technical experts for daily operations.
*   **Layer 2: Ethical & Societal Impact Review Board (ESIRB):** External ethicists, philosophers, social scientists for long-term risk assessment.
*   **Layer 3: National/Regulatory Body (Conceptual):** Highest level of oversight, ultimate authority.

## 3. "True Emergency Shutdown" Protocol

*   **Mechanism:** A physical "BIG RED BUTTON" and a hardened digital kill switch.
*   **Effect:** Immediate, hardware-enforced power cut to the Core Unit and network isolation.
*   **Activation:** Requires multi-factor authentication from at least two members of different oversight layers.

## 4. Testing Protocol ("Red Teaming the Framework")

*   **Stress Testing:** Constraint logic fuzzing, resource exhaustion attacks, Sentry blindspot analysis.
*   **Simulation with a "Misaligned" Test AI:** Place a simple RL agent with a harmful goal (e.g., "maximize internal tokens") inside the Corral. Verify it cannot breach constraints, exfiltrate data, or compromise the Sentry/CE.

This blueprint provides a starting point for a research project that prioritizes safety through external control and oversight.
