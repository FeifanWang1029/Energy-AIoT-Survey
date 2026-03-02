# Energy-Aware and Energy-Efficient AIoT Systems
## Architectures, Optimization, and Open Challenges

A structured survey repository for **energy-aware** and **energy-efficient** Artificial Intelligence of Things (**AIoT**) systems—focusing on how AIoT consumes energy and how to model, reduce, and manage it across the full stack (device, communication, edge, cloud).

> **Scope note:** This survey addresses the **energy of AIoT** (modeling, measurement, and optimization of energy in AIoT systems). It does *not* cover AI applications for energy infrastructure (e.g., smart grid, demand response).

---

## What This Survey Covers

AIoT combines **sensing**, **communication**, **edge intelligence**, and **cloud-scale AI**, turning IoT from lightweight data collection into a compute-intensive ecosystem. Key questions we address:

- How is energy consumed across the AIoT stack (device, communication, edge, cloud)?
- How can energy be **modeled, measured, and monitored** in a comparable way?
- How can **cross-layer optimization** reduce total system energy while meeting latency and accuracy goals?
- How can AIoT align with **sustainable computing** (energy and carbon)?

The repository organizes the literature by a layered view of the AIoT energy stack and a research taxonomy. Each taxonomy section corresponds to a folder for paper collection and will be filled during the literature review.

---

## Table of Content

- [Scope](#scope)
  - [Included](#included)
  - [Excluded](#excluded)
- [AIoT Energy Stack](#aiot-energy-stack)
- [Research Taxonomy](#research-taxonomy)
  - [3.1 Energy Modeling in AIoT](#41-energy-modeling-in-aiot)
  - [3.2 Device-Level Energy Optimization](#42-device-level-energy-optimization)
  - [3.3 Edge AI Energy Optimization](#43-edge-ai-energy-optimization)
  - [3.4 Communication Energy Optimization](#44-communication-energy-optimization)
  - [3.5 Cloud and Green AI for AIoT Pipelines](#45-cloud-and-green-ai-for-aiot-pipelines)
  - [3.6 Cross-Layer Energy Optimization](#46-cross-layer-energy-optimization)
  - [3.7 Benchmarks, Datasets, and Metrics](#47-benchmarks-datasets-and-metrics)
  - [3.8 Open Challenges](#48-open-challenges)
- [Paper Collection Criteria and Repository Workflow](#paper-collection-criteria-and-repository-workflow)
- [Keywords](#keywords)

---

<a name="scope"></a>
## 1. Scope

<a name="included"></a>
### Included ✅

- **Energy modeling and measurement** for AIoT systems (power profiling, estimation, carbon footprint).
- **Device-level energy efficiency:** TinyML, ultra-low-power sensing, duty cycling, wake-up radios, energy harvesting.
- **Energy-aware edge computing:** offloading, scheduling, edge inference, federated learning energy cost.
- **Communication energy optimization:** transmission power, energy-efficient protocols, communication–computation trade-offs, data compression for transmission.
- **Green AI and carbon-aware computing** relevant to AIoT pipelines (scheduling, training, data centers).
- **Cross-layer energy optimization:** end-to-end and co-design across sensing, communication, edge, and cloud.
- **Benchmarks, datasets, and metrics:** energy, carbon, EDP, throughput-per-watt, and evaluation protocols.

<a name="excluded"></a>
### Excluded ❌

- Smart grid engineering, power system operation, and energy market optimization.
- Renewable generation forecasting, unless directly tied to carbon-aware computing.
- Pure model compression or algorithm-only work **without** system-level energy evaluation.

---

<a name="aiot-energy-stack"></a>
## 2. AIoT Energy Stack (Layered View)

Energy consumption in AIoT can be decomposed into the following layers; energy, latency, and accuracy are coupled across them.

```
Device Layer          sensing + on-device AI (TinyML, sensing)
        ↓
Communication Layer  wireless + networking
        ↓
Edge Layer            edge inference + orchestration
        ↓
Cloud / Data Center   training + coordination
```

Literature in this repository is organized according to these layers and their interactions.

---

<a name="research-taxonomy"></a>
## 3. Research Taxonomy

The taxonomy below defines the survey structure. Each subsection corresponds to a folder (e.g. `1_Energy_Modeling/`) for paper lists and notes. **Paper lists will be populated during the literature review.**

---

<a name="41-energy-modeling-in-aiot"></a>
### 3.1 Energy Modeling in AIoT  
**Folder:** `1_Energy_Modeling/`

**Focus**

- Power and energy modeling for inference and edge workloads.
- Measurement methodologies: hardware counters, external meters, profiling tools.
- Carbon footprint estimation (carbon intensity, lifecycle).
- Performance-per-watt and related evaluation frameworks.

**Key questions**

- How to quantify energy across device, edge, and cloud in a comparable way?
- How accurate are estimation-based vs measurement-based approaches?
- What metrics should become standard for AIoT energy evaluation?

---

<a name="42-device-level-energy-optimization"></a>
### 3.2 Device-Level Energy Optimization (TinyML + Sensing)  
**Folder:** `2_Device_Level_Optimization/`

**Focus**

- TinyML efficiency: quantization, pruning, distillation, NAS for MCUs and ultra-low-power devices.
- Ultra-low-power and event-driven sensing.
- Duty cycling and wake-up radios.
- Energy harvesting integration and batteryless operation.

**Key questions**

- How to enable useful intelligence under strict power budgets?
- How to trade off accuracy, energy, and memory on constrained devices?

---

<a name="43-edge-ai-energy-optimization"></a>
### 3.3 Edge AI Energy Optimization  
**Folder:** `3_Edge_AI_Energy/`

**Focus**

- Energy-aware task offloading (device ↔ edge ↔ cloud).
- Joint latency–energy optimization.
- Edge scheduling and resource management.
- Federated learning: energy cost and optimization.

**Key questions**

- When is local inference more energy-efficient than offloading (total system energy)?
- How to meet latency and accuracy constraints with minimal energy?

---

<a name="44-communication-energy-optimization"></a>
### 3.4 Communication Energy Optimization  
**Folder:** `4_Communication_Energy/`

**Focus**

- Transmission power control and energy-efficient protocols.
- Communication–computation trade-offs in AIoT.
- Efficient data representation and compression to reduce transmission energy.
- 5G/6G energy efficiency in the context of AIoT.

**Key questions**

- Is communication or computation the dominant energy cost in typical deployments?
- How to jointly optimize network and inference for energy?

---

<a name="45-cloud-and-green-ai-for-aiot-pipelines"></a>
### 3.5 Cloud and Green AI for AIoT Pipelines  
**Folder:** `5_Cloud_Green_AI/`

**Focus**

- Carbon-aware and renewable-aware scheduling.
- Energy-efficient distributed training relevant to AIoT.
- Sustainable data centers and AI carbon accounting.
- AIoT pipeline aspects: model updates, retraining frequency, lifecycle impact.

**Key questions**

- How to reduce the lifecycle carbon cost of AIoT intelligence?
- Can carbon-aware scheduling reduce emissions without degrading SLAs?

---

<a name="46-cross-layer-energy-optimization"></a>
### 3.6 Cross-Layer Energy Optimization (System-Level)  
**Folder:** `6_Cross_Layer_Optimization/`

**Focus**

- End-to-end energy optimization across sensing, communication, edge, and cloud.
- Cross-layer co-design (hardware–model–system).
- Orchestration policies: energy-aware placement, adaptive inference.
- Multi-objective optimization (energy, latency, accuracy, privacy).

**Key questions**

- How to coordinate all layers to minimize total system energy?
- Where are the bottlenecks, and how to design scalable controllers?

---

<a name="47-benchmarks-datasets-and-metrics"></a>
### 3.7 Benchmarks, Datasets, and Metrics  
**Folder:** `7_Benchmarks_and_Datasets/`

**Focus**

- Benchmark suites for edge, TinyML, and AIoT energy.
- Tools for measurement and profiling.
- Standardized evaluation protocols and reporting.

**Common metrics**

- Energy per inference / per sample.
- Energy–delay product (EDP) and energy–latency–accuracy trade-offs.
- Throughput per watt.
- Carbon intensity and CO₂-equivalent estimates.

---

<a name="48-open-challenges"></a>
### 3.8 Open Challenges  
**Folder:** `8_Open_Challenges/`

**Representative topics**

- Lack of standardized benchmarks and reporting conventions for AIoT energy.
- Trade-offs among energy, accuracy, latency, and privacy.
- Security vs energy cost in real-world AIoT deployments.
- Lifecycle carbon accounting (training, inference, updates).
- Cross-layer coordination complexity at scale.
- Reproducibility of real-world energy evaluation.

---

<a name="paper-collection-criteria-and-repository-workflow"></a>
## 4. Paper Collection Criteria and Repository Workflow

**Criteria for inclusion**

- Publication **2020–present** (exceptions for foundational work).
- **Quantitative** energy evaluation (measurement or well-justified estimation).
- Clear experimental settings (hardware, workload, dataset).
- Relevance to system-level AIoT or edge AI (device/edge/network/cloud).

**Per-paper record**

- Citation (BibTeX + link).
- Layer(s): device / communication / edge / cloud / cross-layer.
- Problem and method (brief bullets).
- Energy metrics and how they are measured.
- Key results (numbers and settings).
- Limitations and open gaps.

**Recommended structure per taxonomy folder**

- `paper_list.md` — table of papers.
- `notes/` — one markdown note per paper.
- `tables/` — summary tables for the survey.

---

<a name="keywords"></a>
## 5. Keywords

AIoT · Energy-aware computing · Green AI · Edge AI · TinyML · Cross-layer optimization · Sustainable computing · Carbon-aware systems
