# EMERGENT_COMPUTE_ORG_MINDMAP_ADMIN.md

## Core Ecosystem Categorization Architecture

### 1. DEFENCE DEMAND & BUYING (Parent: MOD)
* **OCSA (Office of the Chief Scientific Adviser - Defence):** Sets top-level Defence S&T strategy and policy direction.
* **NAD (National Armaments Director):** Parent procurement and armaments authority.
  * **D&D (Digital & Data Strategy):** Sub-organisation directly inside NAD; owns MOD Enterprise Architecture, data strategy, and digital integration.
* **FLCs (Front Line Commands) & Demand:** Direct operational buyers. Used for Business As Usual (BAU) procurement of mature commercial off-the-shelf capabilities (e.g., proven Quantum-Inspired vendor solutions). Does not route through Dstl or CommercialX for BAU software.
* **Dstl (Defence Science & Technology Laboratory):** Defence Technical & Science Authority for high-risk R&D and science validation.
* **UKDI (UK Defence Innovation):** MOD innovation funding umbrella.
  * **CommercialX:** Sub-organisation under UKDI providing fast-track prototyping procurement routes (TRL 4–7).

### 2. SOVEREIGN CAPABILITY & NATIONAL STRENGTH (Parent: DSIT / UKRI)
* **NPL (National Physical Laboratory):** National measurement standard authority; owns sovereign capabilities in Metrology, Quantum Sensing, PNT, and Atomic Timing.
* **UKRI (UK Research & Innovation):** Academic and foundational research funder.
  * **EPSRC:** Engineering and Physical Sciences Research Council.
    * **QCI3 Hub (Hub for Quantum Computing via Integrated and Interconnected Implementations):** Oxford-led multi-university academic research consortium for quantum computing hardware interconnects and application algorithms. [QC ONLY]
  * **STFC:** Science and Technology Facilities Council.
    * **NQCC (National Quantum Computing Centre):** National Lab for quantum computing hardware and HPC testbeds. [QC ONLY]
      * **QSL (Quantum Software Lab - Edinburgh):** Sub-lab under NQCC focused on quantum algorithms and software stacks. [QC ONLY]
* **Innovate UK:** Commercialisation, dual-use technology grant funding, and industrial scaling.
* **NSSIF (National Security Strategic Investment Fund):** Sovereign equity and venture investment for dual-use national security IP.

### 3. INDUSTRIAL MOBILISATION & INDUSTRY INTERFACE
* **UKQuantum:** Quantum sector-specific trade association representing supply chain from SMEs to Primes.
* **Team Defence:** MOD-Industry operational collaboration forum for digital integration and standards.
* **TechUK:** Broad technology trade association representing general enterprise IT and non-quantum digital suppliers across government.

---

## Key Boundary Rules & Taxonomy Nuances

1. **Hierarchy & Parentage Integrity:**
   * D&D is NOT an external convener; it is a sub-organisation inside NAD.
   * QCI3 reports under EPSRC / UKRI as an academic hub.
   * QSL reports directly to NQCC, which sits under STFC / UKRI.
   * CommercialX is a fast-track procurement arm nested within UKDI.

2. **Direct Buying vs. R&D Procurement Paths:**
   * Do NOT force a single linear buyer pipeline.
   * Proven, off-the-shelf industrial capabilities (e.g., Quantum-Inspired software) bypass R&D bodies (Dstl) and rapid prototyping routes (CommercialX) entirely, going straight to FLCs & Demand for BAU enterprise purchase.

3. **Quantum Compute vs. Whole Sector Quantum Scope:**
   * QCI3, NQCC, and QSL must be explicitly tagged as [QC ONLY] (Quantum Computing only).
   * NPL and broader national programs cover Quantum Technologies (Sensing, PNT, Timing, Communications).
   * UKQuantum sits under an abstract Whole Sector Quantum parent overlay covering both QC and QT.

4. **Abstract Overlay Boundaries:**
   * **Broad Technology & Digital Interface Overlay:** Wraps general IT and cyber entities (TechUK, Team Defence).
   * **Whole Sector Quantum Overlay:** Wraps quantum-specific supply chain entities (UKQuantum) across both Defence and Civil sectors.