# BME-analysis: Research Context

## Project Overview

This repository contains statistical analysis for a research paper on ML-based DDoS attack detection evaluated across multiple real-world networks. The analysis answers five research questions (Q1–Q5) using data from the SCLDDoS2024 dataset.

## Dataset: SCLDDoS2024

A publicly accessible dataset of real-world DDoS traffic from four distinct networks:

| Set  | Network type                                                          |
|------|-----------------------------------------------------------------------|
| SetA | Semi-public DCN hosting large streaming services                      |
| SetB | Core network of a major regional ISP (small, client-focused users)    |
| SetC | Public DCN                                                            |
| SetD | Core network of a smaller regional ISP                                |

- **Collection span**: ~6–30 months per dataset (much longer than typical public datasets)
- **Capture hardware**: FPGA-based DDoS detector with 2×100 GbE capture cards; lossless operation at up to 18×100 GbE after payload stripping
- **Granularity**: Flow-level → endpoint-level aggregation at 1-second sampling intervals

### Labeling

The FPGA logic runs custom heuristics and pattern-based DDoS detection algorithms in parallel. Detected traffic is classified as **normal**, **DDoS**, or **suspicious**. A detected event produces:
- **events** files: one record per event (IP-level, 1-second windows)
- **components** files: one record per component (individual 1-second interval), joined to events via `Attack ID`

### Dataset features (events)

| Feature              | Type                    |
|----------------------|-------------------------|
| Attack ID            | categorical             |
| Card                 | categorical             |
| Victim IP            | categorical (anonymized)|
| Port number          | continuous / categorical|
| Attack code          | categorical             |
| Detect count         | continuous              |
| Packet speed (pps)   | continuous              |
| Data speed (bps)     | continuous              |
| Avg packet length    | continuous              |
| Avg source IP count  | continuous              |
| Start / End time     | continuous              |
| Type                 | categorical             |

## Proposed Approach

### Classical vs. Sequence-based

The classical (baseline) approach evaluates each **component** (1-second interval) in isolation against predefined thresholds — one component at a time. This is the "component-based" approach in the experiments.

The **sequence-based** approach evaluates the first **k = 10** components of an event as a multivariate time series, enabling context-aware, temporal classification.

### Feature set (sequence approach)

To maximise generalisability across networks, only network-agnostic features are used:
- Packet speed
- Data speed
- Average packet length
- Source IP address count
- Time difference between consecutive components (d_i = t_{c_i} - t_{c_{i-1}}, d_0 = 0)

Ports, TCP fields, and IP addresses are deliberately excluded (network-specific / easily spoofed).

### Event / Component definition

- **Component** c: a 1-second above-threshold observation vector from the FPGA
- **Event** E = {c_1, …, c_n}: the full sequence of components for one IP address
- **Model input** I = {c_1, …, c_k}, k = 10

## Experiment Methodology

Comprehensive ML evaluation across:
- **Models**: GRU, LSTM, RNN, MLP, NN (sequence-only), KNN, LightGBM, Logistic Regression, Random Forest, SVM, XGBoost (component-based and sequence-based)
- **Tasks**: Binary classification, Multiclass classification
- **Splits**: Random split, Time split
- **Preprocessing**: Multiple strategies (anomalous value handling, scaling, under/over-sampling)
- **Approach**: `enable_sequences=True` (sequence-based) vs `enable_sequences=False` (component-based)
- **Multiple runs**: Several runs per configuration (identified by `run_no`)
- **Sets**: Evaluated on each of SetA, SetB, SetC, SetD independently

Each result is denoted **Result_{i,j,k,l}** where i=Set, j=methodology setting, k=model, l=run number.

## Model Categorisation

| Category | Models |
|----------|--------|
| Deep Learning | GRU, LSTM, RNN, MLP, NN |
| Classical ML  | KNN, LightGBM, Logistic Regression, Random Forest, SVM, XGBoost |

## Research Questions & Analysis Folders

| Folder | Question | Key finding |
|--------|----------|-------------|
| `Q1/`  | Do sequence-based features provide a detection advantage over component-based features, and does this advantage hold across different networks? | Mixed — seq wins on SetB/SetC, comp wins on SetA/SetD |
| `Q2/`  | Does the data splitting strategy (random vs. time-based) significantly inflate reported performance? | Yes — ~4% overall inflation, up to +10% on SetA |
| `Q3/`  | Are models transferable between networks? | No — mean transfer drop +0.28 F1, 84.7% of configs significant |
| `Q4/`  | Is cross-network transfer symmetric, or does training source choice systematically matter? | Asymmetric — SetC is best source, SetD is worst; 69.3% of pairs significant |
| `Q5/`  | Do deep learning models outperform classical ML, especially under time-split and cross-network conditions? | DL wins in-network (+0.04 F1 under time-split); Classical ML transfers better cross-network |
| `Q6/`  | Does Cross-Network Validation Help DDoS Detectors Generalise? | TBD |
