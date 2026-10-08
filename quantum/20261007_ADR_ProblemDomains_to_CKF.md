# Architecture Decision Record (ADR): Transition from Problem Domains to Canonical Kernel Families (CKFs)

- **Date:** 2026-10-07
- **Status:** Proposed / Recommended
- **Scope:** Mindmap Pipeline Layer 6 (`Problem Domain` -> `Computational Kernel Families`)
- **Downstream Impact:** All 17 Layer 7 Use Cases (`Use Cases (MOD Relevance)`)

---

## 1. Executive Summary & Context

The quantum capability pipeline currently models 7 conceptual layers:
```
[1. Science Discovery]
       ↓
[2. Computational Engineering]
       ↓
[3. Computing Paradigm]
       ↓
[4. Algorithm Paradigm]
       ↓
[5. Example Algorithms]
       ↓
[6. Problem Domain]                 <--- TARGET LAYER FOR CHANGE
       ↓
[7. Use Cases (MOD Relevance)]
```

Historically, Layer 6 was designated as **"Problem Domains"** (8 nodes). While functional as an initial taxonomy, it conflated computational mechanics with broad operational application areas (e.g. *Optimisation*, *Simulation of Quantum systems*, *Interpretation of Quantum sensing*).

To provide a compute-agnostic, enduring abstraction suitable for Ministry of Defence (MOD) capability planning, capability procurement, and algorithmic assessment, Layer 6 is proposed to transition to **Canonical Kernel Families (CKFs)** (7 shortlisted nodes).

---

## 2. Why Change? (The Core Rationale)

1. **Elimination of Artificial Overlaps in the Existing Taxonomy:**
   - In the legacy 8-domain set, *Optimisation* and *Combinatorial Search & Pathfinding* heavily overlapped, creating ambiguous routing into logistics and scheduling use cases.
   - *Interpretation of Quantum sensing* was classified as a domain, whereas computationally it is multi-sensor statistical inference / signal exploitation.

2. **Resolution of Physical Simulation Misplacements:**
   - Under the legacy model, macroscopic continuum physics (e.g. `Use Case ⑱ Nuclear Stockpile Stewardship & High-Energy Physics`) was forced into *Simulation of Quantum systems*. 
   - Separating microscopic quantum dynamics from macroscopic continuous physics restores physical and algorithmic integrity.

3. **Pragmatic Defence Capability Focus vs. Academic Abstraction:**
   - A pure theoretical/computer science critique suggested reducing all kernels to pure mathematical primitives (e.g., *Tensor Contractions*, *Primitive Operator Algebras*, *Algebraic Ring Reduction*).
   - For a Defence (MOD/DSTL) audience, pure mathematical abstractions obscure mission value. CKFs maintain the operational bridge—retaining clear descriptors like *Electronic Structure*, *Cryptanalytic*, and *Physical Simulation*—while remaining compute-agnostic (spanning classical HPC, quantum, neuromorphic, and analogue).

---

## 3. The 7 Shortlisted Canonical Kernel Families (CKFs)

| # | Proposed CKF Node | Scope & MOD Relevance |
|---|---|---|
| **1** | **Constrained Combinatorial Allocation & Scheduling** | Discrete, non-convex optimization under constraints (weapon-target allocation, theater supply routing, force laydown, flight scheduling). |
| **2** | **Sequential Stochastic Decision-Making Under Uncertainty** | Multi-stage dynamic control and planning under fog-of-war (wargaming, C2 course-of-action replanning, autonomous swarm doctrine). |
| **3** | **Graph Inference & Search** | Structural traversal and topological analysis on networks (intelligence graph search, C4ISR kill-web resilience, multi-tier supply chain dependency). |
| **4** | **High-Dimensional Statistical Inference** | High-dimensional pattern extraction, multi-sensor data fusion, and emitter/signal classification (ISR exploitation, RF signature matching). |
| **5** | **Electronic Structure & Quantum Dynamics** | Quantum mechanical Hamiltonian evolution and molecular state simulation (stealth metamaterials, energetic formulations, quantum sensor materials). |
| **6** | **Cryptanalytic Number-Theoretic Computation** | Discrete logarithm, integer factorization, and algebraic group exploration (public-key vulnerability assessment, Shor's algorithmic impact). |
| **7** | **Physical System Simulation** | Continuous PDE/ODE field solvers, fluid dynamics, plasma, and hydrodynamics (nuclear stockpile stewardship, blast dynamics, aerodynamics, acoustic propagation). |

---

## 4. Lineage: Legacy Problem Domains to New CKFs

| Legacy Problem Domain (8 Nodes) | Disposition in 7-CKF Model | Rationale |
|---|---|---|
| **Optimisation** | Absorbed into **CKF 1** (*Combinatorial Allocation & Scheduling*) | Replaces ambiguous generic optimization with concrete constrained allocation. |
| **Combinatorial Search & Pathfinding** | Merged across **CKF 1** and **CKF 3** | Separates discrete resource selection (CKF 1) from network pathfinding (CKF 3). |
| **Modelling under Uncertainty** | Replaced by **CKF 2** (*Sequential Stochastic Decision-Making...*) | Tightens passive modeling into multi-stage operational decision dynamics. |
| **Graph Analytics & Network Topology** | Renamed to **CKF 3** (*Graph Inference & Search*) | Aligns with standard computational terminology. |
| **Pattern Classification & Anomaly Detection** | Tightened to **CKF 4** (*High-Dimensional Statistical Inference*) | Removes "anomaly detection" (an operational use case) to keep the kernel compute-agnostic. |
| **Simulation of Quantum systems** | Split into **CKF 5** (*Electronic Structure*) & **CKF 7** (*Physical System Simulation*) | Fixes the miscategorisation of macroscopic physics (e.g. stockpile stewardship) under quantum systems. |
| **Cryptography / Secure comms** | Tightened to **CKF 6** (*Cryptanalytic Number-Theoretic Computation*) | Eliminates protocol jargon; focuses strictly on the computational hard-problem. |
| **Interpretation of Quantum sensing** | Retired as a standalone domain; mapped to **CKF 4** | Ingesting and processing quantum sensor streams is statistical sensor fusion, not a distinct computational kernel. |

---

## 5. Mapping to the 17 Layer 7 MOD Use Cases

All 17 existing defence use cases map cleanly into the 7 CKF nodes:

```
[CKF 1: Constrained Combinatorial Allocation & Scheduling]
   ├── ① Tactical Combat Supply Routing
   ├── ② Strategic Force Projection & Expeditionary Scheduling
   ├── ③ Strategic Force & Logistics Readiness
   ├── ⑦ Tactical Search & Rescue Path Planning
   └── ⑯ Tactical Asset Disposition & Force Effectiveness

[CKF 2: Sequential Stochastic Decision-Making Under Uncertainty]
   ├── ④ Wargaming & Course-of-Action Simulation
   ├── ⑧ Strategic Risk & Geopolitical Forecasting
   ├── ⑨ Tactical Threat-Probability Estimation
   └── ⑩ Strategic Defense Policy Simulation

[CKF 3: Graph Inference & Search]
   ├── ① Tactical Combat Supply Routing (network topology aspect)
   ├── ⑤ Large-Scale Intelligence Graph Search
   ├── ⑯ Tactical Asset Disposition & Force Effectiveness (kill-web mesh)
   └── ⑰ Strategic Industrial Base Resilience (supply chain tiers)

[CKF 4: High-Dimensional Statistical Inference]
   ├── ⑥ ISR Pattern-Matching & Data Exploitation
   ├── ⑨ Tactical Threat-Probability Estimation (sensor fusion aspect)
   └── ⑮ Tactical Signal De-Interleaving & Emitter Identification

[CKF 5: Electronic Structure & Quantum Dynamics]
   ├── ⑪ Sovereign Materials & Energetics R&D (microscopic quantum design)
   └── ⑫ Quantum Sensor Hardware Design (atomic cavity / defect physics)

[CKF 6: Cryptanalytic Number-Theoretic Computation]
   └── ⑬ Strategic Cryptanalysis & Vulnerability Evaluation

[CKF 7: Physical System Simulation]
   ├── ⑪ Sovereign Materials & Energetics R&D (macroscopic hydrodynamics & burn)
   ├── ⑫ Quantum Sensor Hardware Design (classical EM fields)
   └── ⑱ Nuclear Stockpile Stewardship & High-Energy Physics
```

---

## 6. Open Items & Future Considerations

1. **Signal Processing & Electronic Warfare (Use Case ⑮):**
   - *Current Mapping:* Folded under CKF 4 (*High-Dimensional Statistical Inference*).
   - *Consideration:* If radar beamforming, PRI sorting, and Fourier/spectral transforms expand in future iterations, assess whether a dedicated *Continuous Signal Processing & Spectral Transforms* kernel is warranted.
2. **Post-Quantum Cryptography Scope (Use Case ⑬):**
   - *Current Scope:* CKF 6 focuses on number-theoretic computation (Shor/RSA/ECC).
   - *Consideration:* As PQC attacks (lattice reduction, BKZ) evolve, the scope may gently generalize to *Cryptanalytic & Algebraic Computation*.
