# DynTrust-FedIDS++ — Extracted Figures and Tables

## Figures (from notebook experimental outputs)

| File | Caption |
| --- | --- |
| `Figures/Fig01_Clean_Baseline_0pct_Byzantine_0pct_DP.png` | Fig. 1 – Clean Baseline (0% Byzantine, 0% DP) |
| `Figures/Fig02_Trust_Audit_Honest_vs_Byzantine.png` | Fig. 2 – Trust: Honest vs. Byzantine and Isolation Decision Quality |
| `Figures/Fig03_Baseline_Comparison_30pct_Byzantine_ALIE.png` | Fig. 3 – Baseline Comparison under 30% Byzantine + ALIE |
| `Figures/Fig04_Ablation_Study.png` | Fig. 4 – Ablation Study (Full method vs components removed) |
| `Figures/Fig05_DP_Sigma_Sweep_Privacy_Robustness_Fairness.png` | Fig. 5 – Privacy–Robustness–Fairness Coupling (DP sigma sweep) |
| `Figures/Fig06_Attack_Type_Comparison.png` | Fig. 6 – Proposed Method Under Different Attack Types (30% Byzantine) |

## Tables (CSV + Markdown)

### Experimental result tables (aligned with manuscript Section 5)

- `Table02_Clean_Baseline.csv` / `Table02_Clean_Baseline.md` — Table 2. Clean baseline (0% Byzantine, σ=0)
- `Table03_Baseline_Comparison_30pct_ALIE.csv` / `Table03_Baseline_Comparison_30pct_ALIE.md` — Table 3. Aggregator comparison under 30% Byzantine (ALIE) + σ=0.05 (single seed)
- `Table04_Ablation.csv` / `Table04_Ablation.md` — Table 4. Ablation of DynTrust-FedIDS++ components (30% Byzantine, ALIE, σ=0.05)
- `Table05_DP_Sigma_Sweep.csv` / `Table05_DP_Sigma_Sweep.md` — Table 5. Effect of DP noise scale on the proposed method (30% Byzantine, ALIE)
- `Table06_Attack_Type.csv` / `Table06_Attack_Type.md` — Table 6. Proposed method under different attack types (30% Byzantine, σ=0.05)
- `Table02_PerClient_Sample_Composition.csv` / `Table02_PerClient_Sample_Composition.md` — Table 2 (Methods). Per-client sample size and class composition

### Full manuscript tables (extracted from .docx)

- `Table01_Positioning_Related_Work.csv` / `Table01_Positioning_Related_Work.md`
- `Table02_PerClient_Composition_docx.csv` / `Table02_PerClient_Composition_docx.md`
- `Table02_Clean_Baseline_docx.csv` / `Table02_Clean_Baseline_docx.md`
- `Table03_Baseline_Comparison_docx.csv` / `Table03_Baseline_Comparison_docx.md`
- `Table04_Ablation_docx.csv` / `Table04_Ablation_docx.md`
- `Table05_DP_Sweep_docx.csv` / `Table05_DP_Sweep_docx.md`
- `Table06_Attack_Type_docx.csv` / `Table06_Attack_Type_docx.md`
- `Table07_RQ_Mapping.csv` / `Table07_RQ_Mapping.md`
- `Table08_State_of_the_Art_Comparison.csv` / `Table08_State_of_the_Art_Comparison.md`

## Notes

- Figure PNGs are the actual plots produced by the real-data notebook.
- Table numbers follow the manuscript; Table 1 (related-work positioning) and Table 8 (SOTA) come from the docx.
- “Fig 1. Proposed Framework” architecture diagram is referenced in the paper but is not an embedded PNG in the notebook outputs; place a separately exported architecture diagram as `Fig00_Architecture_Proposed_Framework.png` if available.
