# IDS-SDN-Overview

**Intrusion Detection System Generalization in Software-Defined Networks**

Bachelor's Thesis — Universitat Politecnica de Valencia (UPV)

## Abstract

This project investigates the generalization capabilities of machine learning-based Intrusion Detection Systems (IDS) deployed in Software-Defined Networking (SDN) environments. The research focuses on whether models trained on one network topology can effectively detect attacks in different, unseen topologies — a critical requirement for real-world SDN deployments.

## Objectives

1. **Evaluate IDS transferability** across different SDN topologies
2. **Analyze feature importance** for topology-independent intrusion detection
3. **Propose a generalization framework** that maintains detection accuracy across diverse network configurations
4. **Benchmark** against existing IDS approaches in SDN literature

## Methodology

- **SDN Controller**: OpenDaylight / Ryu
- **Network Emulation**: Mininet with custom topologies (linear, tree, mesh, fat-tree)
- **Traffic Generation**: Benign traffic patterns + attack scenarios (DDoS, port scan, ARP spoofing, flow table overflow)
- **Feature Extraction**: Flow-level statistics from OpenFlow counters
- **Models**: Random Forest, XGBoost, ensemble methods
- **Evaluation**: Cross-topology validation (train on topology A, test on topology B)

## Tech Stack

| Component | Technology |
|-----------|-----------|
| SDN Controller | Ryu (Python) |
| Network Emulation | Mininet |
| Traffic Analysis | Scapy, CICFlowMeter |
| ML Pipeline | scikit-learn, XGBoost |
| Visualization | Matplotlib, Seaborn |
| Data Processing | Pandas, NumPy |

## Key Results

- Achieved cross-topology detection rates comparable to same-topology training
- Identified flow-level features that generalize well across topologies
- Demonstrated that topology-specific features degrade model portability
- Proposed a feature selection pipeline for topology-agnostic IDS deployment

## Project Structure

```
├── src/                 # Source code
│   ├── controller/      # SDN controller modules
│   ├── topologies/      # Mininet topology definitions
│   ├── features/        # Feature extraction pipeline
│   └── models/          # ML model training and evaluation
├── data/                # Datasets (pcaps, flow records)
├── models/              # Trained model artifacts
├── figures/             # Generated plots and visualizations
└── docs/                # Thesis document (LaTeX)
```

## Status

This thesis was completed as part of the Telecommunications Engineering degree at UPV. Source code is maintained in a private repository.

## Contact

- [LinkedIn](https://www.linkedin.com/in/miguel-serra-ferrando)
