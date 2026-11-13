# Introducing Computational Problem Archetypes (CPAs)
*A Compute-Agnostic Framework for Problem Formulation, Dual-Use Collaboration, and Bottleneck Analysis*

---

## Executive Summary: Engineering for Reuse

Many operational, scientific, and business challenges can be expressed as combinations of a small number of recurring **Computational Problem Archetypes (CPAs)**—such as constrained combinatorial optimisation, graph inference, statistical inference, or sequential decision-making under uncertainty. CPAs provide a compute-agnostic abstraction over specific mathematical models, algorithms, numerical solvers, and underlying hardware technologies.

Real-world use cases are rarely confined to a single archetype; they are typically blends of several. A useful analogy is to think of CPAs as the **primary colours** of computational problem solving. 

For any given challenge, the critical operational question is not whether a specific emergent technology is relevant, but **which CPAs are actively constraining performance**. Understanding the relative contribution of each archetype exposes the dominant bottleneck, guides investment, and determines where advances in compute capability will actually deliver tangible edge. Improving a secondary archetype yields little to no operational return if the dominant archetype remains constrained.

Over time, analysing problems through this lens enables organisations to build enduring, reusable algorithmic competence, collaborate seamlessly across civil and academic ecosystems, and avoid getting locked into volatile, vendor-driven hardware roadmaps.

---

## 1. The Seven Computational Problem Archetypes (The What)

The seven archetypes below capture distinct computational problem structures without requiring deep computer science or quantum physics specialisation. They are inherently dual-use, bridging defence requirements with academic research and civil industry.

### ① Constrained Combinatorial Allocation & Scheduling
*Selecting, assigning, positioning, routing, or scheduling scarce resources subject to operational constraints.*  
Involves discrete choice spaces where the number of possible configurations grows exponentially with problem size. Examples include multi-depot fleet dispatch, asset-to-task assignment, communications spectrum allocation, and mission sortie scheduling.

### ② Sequential Stochastic Decision-Making Under Uncertainty
*Making a series of dependent decisions over time where outcomes depend on uncertain future events, partial observations, and adversarial actions.*  
Involves dynamic state transitions under the fog of war, imperfect information, and changing environments. Examples include multi-stage course-of-action wargaming, adaptive search-and-rescue path planning, and autonomous system trajectory replanning under active threat.

### ③ Graph Inference & Search
*Discovering, traversing, partitioning, and reasoning over relationships, networks, dependencies, and highly connected data structures.*  
Focuses on topological structure, network flows, and entity clustering rather than coordinate geometry. Examples include intelligence knowledge-graph querying, kill-web dependency traversal, supply network vulnerability analysis, and cyber attack-path discovery.

### ④ High-Dimensional Statistical Inference
*Extracting patterns, estimating hidden states, separating signals from noise, and generating predictions from large, heterogeneous, or incomplete datasets.*  
Addresses the curse of dimensionality across noisy multi-sensor and multi-spectral environments. Examples include electronic warfare signal de-interleaving, multi-static sonar/radar track fusion, automated anomaly detection in telemetry, and predictive maintenance estimation.

### ⑤ Electronic Structure & Quantum Dynamics
*Modelling molecules, novel materials, quantum devices, and microscopic quantum-mechanical phenomena from first principles.*  
Simulates microscopic quantum states governed by Hamiltonian time-evolution. Examples include designing high-energy molecular energetics, semiconductor defect engineering for quantum sensors, and catalytic surface modelling for advanced battery chemistries.

### ⑥ Cryptanalytic Number-Theoretic Computation
*Solving mathematical problems rooted in algebraic structures, discrete logarithms, integer factorisation, and lattice mathematics.*  
Focuses on the mathematical structures underpinning cryptographic security, secure communications, and cryptanalysis. Examples include auditing post-quantum cryptographic primitives, vulnerability evaluations of legacy asymmetric schemes, and sovereign mathematical verification.

### ⑦ Physics-Based Simulation
*Modelling continuous physical systems governed by partial differential equations (PDEs) to predict or optimise macroscopic outcomes.*  
Addresses continuum physics across fluid dynamics, structural mechanics, thermodynamics, and electrodynamics. Examples include computational fluid dynamics (CFD) for hypersonic glide bodies, hydrodynamics for sovereign stockpile stewardship, radar cross-section (RCS) propagation, and micro-climate meteorological forecasting.

---

## 2. Assessing Bottlenecks: The 0–3 Scoring Model (The How)

To map a problem without getting lost in technical speculation, each CPA is evaluated against the target challenge using a simple 0–3 contribution scale:

| Score | Meaning | Operational Interpretation |
| :---: | :--- | :--- |
| **0** | **Not materially relevant** | Archetype is absent or has trivial computational impact. |
| **1** | **Present but secondary** | Archetype is required as part of the pipeline, but does not dictate runtime or success. |
| **2** | **Important contributor** | Archetype represents a significant computational demand that impacts performance. |
| **3** | **Dominant bottleneck** | Archetype is the primary rate-limiting factor; operational success hinges on solving this. |

### The Bottleneck Rule
> Operational advantage comes strictly from attacking the **Score 3** archetype.  
> *Example:* If an Intelligence Exploitation pipeline is dominated by **Graph Inference & Search (3)** and only uses **Constrained Allocation (1)** to distribute batch compute jobs, procuring an advanced quantum annealing hardware solver for the allocation step will deliver virtually zero operational advantage to the intelligence analyst.

---

## 3. Beyond the Optimisation Trap (The QOBLIB Context)

Many benchmark libraries, academic communities, and vendor offerings are heavily concentrated on combinatorial optimisation (represented by benchmark suites such as **QOBLIB**, covering assignment, scheduling, routing, packing, and facility location).

While combinatorial optimisation is critical, it represents only one of the seven primary colours. Significant defence, scientific, and industrial challenges live entirely outside optimisation—in graph inference, high-dimensional statistical signal processing, PDE physics simulation, quantum dynamics, or number theory.

- When a challenge maps cleanly to QOBLIB, it indicates a mature combinatorial optimisation component where classical heuristics, mathematical programming (MILP), and hybrid quantum/annealing solvers can be systematically benchmarked.
- The **absence** of a sensible QOBLIB mapping is an immediate signal that the challenge is dominated by an entirely different archetype and must be evaluated through that specific computational lens.

---

## 4. Operational Boundaries: The Lucy Principle

Not every operational friction is a technology problem, and not every technology problem is a computational bottleneck.

Before assuming that advanced or emergent compute is required, capability sponsors must verify where the true operational friction lies:
- **Data Quality & Availability:** Is the bottleneck an algorithmic ceiling, or simply missing, uncalibrated, or siloed data?
- **Sensor & Communication Latency:** Does faster compute matter if edge transmission bandwidth cannot deliver inputs in time?
- **Doctrine, Governance & Decision Cycles:** Does solving a mathematical problem in seconds change operational outcomes if mission approval workflows take days?

A computational problem archetype only creates operational edge when computation itself is the critical path.
