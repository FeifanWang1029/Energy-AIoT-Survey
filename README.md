# Energy-Aware and Energy-Efficient AIoT Systems  
## Architectures, Optimization, and Open Challenges

A structured research repository for systematically collecting, classifying, and analysing literature on **energy-aware** and **energy-efficient** Artificial Intelligence of Things (**AIoT**) systems.

> Focus: **Energy of AIoT** (how AIoT consumes energy and how to reduce/manage it), **not** AI applications for energy infrastructure.

---

## 1. Motivation

AIoT systems increasingly combine **sensing**, **communication**, **edge intelligence**, and **cloud-scale AI**. This evolution turns IoT from lightweight data collection into a compute-intensive ecosystem involving:

- On-device inference (TinyML)
- Edge intelligence and orchestration
- Distributed / federated learning
- Cloud-assisted training and coordination

This growth creates urgent questions:

- How is energy consumed across the AIoT stack?
- How can energy be **modeled, measured, and monitored**?
- How can cross-layer optimization reduce total system energy?
- How can AIoT align with **sustainable computing** goals (energy + carbon)?

This repository provides a **taxonomy + paper base** to support a survey and long-term research.

---

## 2. Scope

### Included ✅
- Energy **modeling / measurement** for AIoT systems  
- Device-level energy efficiency (TinyML, sensing, duty cycling)  
- Energy-aware **edge computing** (offloading, scheduling, inference)  
- Communication energy optimization and comm–comp trade-offs  
- Green AI / carbon-aware cloud computing relevant to AIoT pipelines  
- Cross-layer energy optimization (end-to-end, co-design)  
- Benchmarks, datasets, and metrics (energy, carbon, EDP, etc.)

### Excluded ❌
- Smart grid engineering and power system operation  
- Energy market optimization / dispatch / grid economics  
- Renewable generation forecasting (unless directly tied to carbon-aware computing)  
- Pure model compression work **without** system energy evaluation

---

## 3. AIoT Energy Stack (Layered View)

AIoT energy consumption can be decomposed into layers:

```
Device Layer (sensing + on-device AI)
  ↓
Communication Layer (wireless + networking)
  ↓
Edge Layer (edge inference + orchestration)
  ↓
Cloud / Data Center Layer (training + coordination)
```

Energy, latency, and accuracy are tightly coupled across layers. This repo organizes literature accordingly.

---

## 4. Research Taxonomy

> Each section corresponds to a folder and a paper list to be filled during literature review.

---

### 4.1 Energy Modeling in AIoT  
**Folder:** `1_Energy_Modeling/`

**Focus**
- Power/energy modeling for inference and edge workloads  
- Measurement methodologies (hardware counters, external meters, profiling)  
- Carbon footprint estimation (carbon intensity, lifecycle)  
- Performance-per-watt evaluation

**Key questions**
- How to quantify energy across devices/edge/cloud reliably?  
- How accurate are estimation vs measurement approaches?  
- What metrics should become **standard** for AIoT energy evaluation?

---

### 4.2 Device-Level Energy Optimization (TinyML + Sensing)  
**Folder:** `2_Device_Level_Optimization/`

**Focus**
- TinyML efficiency (quantization, pruning, distillation, NAS for MCUs)  
- Ultra-low-power sensing, event-driven sensing  
- Duty cycling / wake-up radios  
- Energy harvesting integration

**Key questions**
- How to enable intelligence under strict power budgets?  
- How to trade accuracy vs energy vs memory on constrained devices?

---

### 4.3 Edge AI Energy Optimization  
**Folder:** `3_Edge_AI_Energy/`

**Focus**
- Energy-aware task offloading (device ↔ edge ↔ cloud)  
- Joint latency–energy optimization  
- Edge scheduling / resource management  
- Federated learning energy cost and optimization

**Key questions**
- When is local inference better than offloading (total energy)?  
- How to meet latency constraints with minimal energy?

---

### 4.4 Communication Energy Optimization  
**Folder:** `4_Communication_Energy/`

**Focus**
- Transmission power control and energy-efficient protocols  
- Communication–computation trade-offs  
- Efficient data representation / compression to reduce transmission  
- 5G/6G energy efficiency aspects for AIoT

**Key questions**
- Is communication or computation more energy expensive in practice?  
- How to jointly optimize network + inference?

---

### 4.5 Cloud and Green AI for AIoT Pipelines  
**Folder:** `5_Cloud_Green_AI/`

**Focus**
- Carbon-aware scheduling and renewable-aware computing  
- Energy-efficient distributed training  
- Sustainable data centers and AI carbon accounting  
- AIoT pipeline considerations (model updates, retraining frequency, etc.)

**Key questions**
- How to reduce lifecycle carbon cost of AIoT intelligence?  
- Can carbon-aware scheduling reduce emissions without harming SLAs?

---

### 4.6 Cross-Layer Energy Optimization (System-Level Core)  
**Folder:** `6_Cross_Layer_Optimization/`

**Focus**
- End-to-end energy optimization across sensing/comm/edge/cloud  
- Cross-layer co-design (hardware–model–system)  
- Orchestration policies (energy-aware placement, adaptive inference)  
- Multi-objective optimization (energy, latency, accuracy, privacy)

**Key questions**
- How to coordinate all layers to minimize total energy?  
- Where are the bottlenecks and how to design scalable controllers?

---

### 4.7 Benchmarks, Datasets, and Metrics  
**Folder:** `7_Benchmarks_and_Datasets/`

**Focus**
- Benchmark suites for edge/TinyML/AIoT energy  
- Tools for measurement and profiling  
- Standardized evaluation protocols

**Common metrics**
- Energy per inference / per sample  
- Energy-delay product (EDP) / energy-latency-accuracy trade-offs  
- Throughput per watt  
- Carbon intensity and CO₂-equivalent estimates

---

### 4.8 Open Challenges  
**Folder:** `8_Open_Challenges/`

**Examples**
- Lack of standardized benchmarks and reporting conventions  
- Energy vs accuracy vs latency vs privacy trade-offs  
- Security vs energy costs in AIoT deployments  
- Lifecycle carbon accounting (training + inference + updates)  
- Cross-layer coordination complexity at scale  
- Real-world evaluation reproducibility

---

## 5. Paper Collection Criteria

Papers included in this repository should ideally:

- Be published **2020–present**  
- Include **quantitative** energy evaluation (measurement or well-justified estimation)  
- Provide clear experimental settings (hardware, workload, dataset)  
- Address system-level optimization (device/edge/network/cloud)  
- Be relevant to AIoT or edge AI deployments

---

## 6. Repository Workflow (How to Fill This Repo)

For each paper, record:

- **Citation** (BibTeX + link)
- **Layer(s)**: device / comm / edge / cloud / cross-layer  
- **Problem** + **method** (2–5 bullet points)  
- **Energy metrics** used and how measured  
- **Key results** (numbers + settings)  
- **Limitations** / assumptions  
- **Open gaps** (what remains unsolved)

Recommended files per folder:
- `paper_list.md` (table of papers)
- `notes/` (one markdown note per paper)
- `tables/` (summary tables for the survey)

---

## 7. Long-Term Vision

This repository aims to:

- Build a structured knowledge base for **energy-efficient AIoT**
- Identify research gaps for **sustainable AI systems**
- Support cross-layer energy optimization research directions
- Serve as the foundation for a survey paper and future projects

---

## 8. Keywords

AIoT · Energy-aware computing · Green AI · Edge AI · TinyML · Cross-layer optimization · Sustainable computing · Carbon-aware systems
