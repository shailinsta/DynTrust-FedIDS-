DynTrust-FedIDS++: Optimization-Based Trust Aggregation for Privacy-Aware Byzantine-Robust Federated Intrusion Detection under Data Drift
Over View 
Federated learning enables collaborative intrusion detection without exchanging raw network traffic, yet it remains vulnerable to Byzantine client updates, heterogeneous and non-stationary data distributions, privacy-induced noise, and severe class imbalance. These factors interact in ways that can degrade conventional aggregation rules and suppress detection of minority attack classes. This paper presents DynTrust-FedIDS++, a federated intrusion-detection framework that unifies optimisation-based adaptive aggregation, multi-criteria client trust estimation, Gaussian differential privacy, and drift-aware residual analysis. Aggregation is formulated as a convex optimisation problem solved by accelerated proximal gradient (FISTA), allowing client contributions to be weighted according to trust and robustness criteria rather than fixed heuristic rules. The framework is evaluated on four real flow-level datasets—NF-CSE-CIC-IDS2018, NF-ToN-IoT, UNSW-NB15 and CIDDS-001, under heterogeneous non-IID partitions and an explicit 30 % Byzantine participation scenario using the ALIE attack. Under these conditions DynTrust-FedIDS++ attains a balanced accuracy of 0.646 and a minority-class recall of 0.942, substantially outperforming classical robust aggregators (FedAvg, coordinate median, trimmed mean, Krum, Multi-Krum and static trust-weighted Krum), several of which collapse to chance-level performance. Ablation experiments confirm that the iterative optimisation step is the primary source of resilience, while a modest differential-privacy noise scale (σ=0.05) acts as a beneficial regulariser that further improves minority recall. An explicit trust-module audit, however, reveals that the current trust scores do not reliably separate honest from Byzantine clients and occasionally produce inverted rankings. This finding underscores the necessity of independently validating trust mechanisms rather than assuming that trust-weighted aggregation guarantees adversary isolation. Overall, the results provide reproducible empirical evidence for the joint evaluation of robustness, privacy and minority-class fairness on real network data, while identifying trust calibration, multi-seed statistical validation and broader attack-rate sweeps as essential directions for future refinement.

Repository Structure 
DynTrust_Figures_and_Tables/
├── INDEX.md
├── Figures/
│   ├── Fig01_Clean_Baseline_0pct_Byzantine_0pct_DP.png
│   ├── Fig02_Trust_Audit_Honest_vs_Byzantine.png
│   ├── Fig03_Baseline_Comparison_30pct_Byzantine_ALIE.png
│   ├── Fig04_Ablation_Study.png
│   ├── Fig05_DP_Sigma_Sweep_Privacy_Robustness_Fairness.png
│   └── Fig06_Attack_Type_Comparison.png
└── Tables/
    ├── Table01_Positioning_Related_Work.csv / .md
    ├── Table02_Clean_Baseline.csv / .md
    ├── Table02_PerClient_Sample_Composition.csv / .md
    ├── Table03_Baseline_Comparison_30pct_ALIE.csv / .md
    ├── Table04_Ablation.csv / .md
    ├── Table05_DP_Sigma_Sweep.csv / .md
    ├── Table06_Attack_Type.csv / .md
    ├── Table07_RQ_Mapping.csv / .md
    ├── Table08_State_of_the_Art_Comparison.csv / .md
    └── (+ matching *_docx versions from the manuscript)

Dataset sources:
•	NF-CSE-CIC-IDS2018 and NF-ToN-IoT: University of Queensland NIDS Dataset Repository :ML-Based NIDS Datasets
•	UNSW-NB15: University of New South Wales: The UNSW-NB15 Dataset | UNSW Research
•	CIDDS-001: Hochschule Coburg : CIDDS - Coburg Intrusion Detection Data Sets | Hochschule Coburg

Colab Notebook 
https://colab.research.google.com/drive/1MSswW6RsLCq0Dsc8l4mb4uhzSqbinO9P?usp=sharing
Authors
Shailendra Mishra (Corresponding author) – Majmaah University
Megha Rathi – Jaypee Institute of Information Technology
Saumitya Srivastava – Jaypee Institute of Information Technology

# Figures directory

Save notebook-generated figures here with descriptive names, for example:

- `fig1_clean_baseline.png`
- `fig2_trust_audit_honest_vs_byzantine.png`
- `fig3_baseline_comparison_30pct_alie.png`
- `fig4_ablation_study.png`
- `fig5_dp_sigma_sweep.png`
- `fig6_attack_type_comparison.png`

These names are suggestions only; keep whatever filenames the notebook produces if you prefer.
