# DynTrust-FedIDS++ — GitHub Repository and Zenodo DOI Setup Instructions

Follow these steps exactly. Do **not** invent a DOI. Zenodo will generate it after you publish the release.

---

## Part 1 — Create / use your GitHub account

1. Go to https://github.com/
2. Sign up (or log in) with the account that will own the repository.
3. Verify the email address.
4. Confirm you have full access to this account; the repository will live under it.

---

## Part 2 — Create the repository

1. Log in to GitHub.
2. Go to https://github.com/new
3. Fill in:

   | Field | Value |
   |-------|--------|
   | **Repository name** | `DynTrust-FedIDS-plusplus` |
   | **Description** | Optimization-Based Trust Aggregation for Privacy-Aware Byzantine-Robust Federated Intrusion Detection under Data Drift |
   | **Visibility** | Public (recommended for open science / DOI) |

4. **Do NOT** select “Add a README file” (the package already contains README.md).
5. **Do NOT** add a license at this stage (LICENSE is already in the folder).
6. Click **Create repository**.

---

## Part 3 — Upload the prepared package

You have a prepared folder named:

```
DynTrust-FedIDS-plusplus/
```

It should contain at least:

```
DynTrust-FedIDS-plusplus/
├── DynTrust_FedIDS_plusplus_REALDATA_pipeline.ipynb
├── README.md
├── requirements.txt
├── LICENSE
├── CITATION.cff
├── zenodo_metadata.json
├── figures/          (may be empty initially)
├── results/          (may be empty initially)
└── docs/
    ├── GitHub_and_Zenodo_DOI_Setup_Instructions.md
    └── DynTrust-FedIDS-plusplus_manuscript_draft.docx   (optional)
```

**Rules:**

- Do not rename the notebook or core files.
- Do not delete generated results or figures once you have run experiments and saved them.
- Do **not** include passwords, API keys, Google Drive credentials, private links, or personal tokens.

---

## Part 4 — Upload files to GitHub

1. Open the new empty repository.
2. Click **Add file → Upload files**.
3. Open the local `DynTrust-FedIDS-plusplus` folder.
4. Select all project files and folders and upload them.
5. Confirm the final structure matches the tree above. The notebook must be in the **root** of the repository.
6. Commit message:

   ```
   Initial DynTrust-FedIDS++ project release
   ```
7. Click **Commit changes**.

---

## Part 5 — Pre-DOI checklist

Before creating a release / DOI, verify:

- [ ] README.md renders correctly on GitHub
- [ ] requirements.txt is present
- [ ] DynTrust_FedIDS_plusplus_REALDATA_pipeline.ipynb is present
- [ ] LICENSE and CITATION.cff are present
- [ ] zenodo_metadata.json is present
- [ ] No missing critical files
- [ ] No unnecessary or private files
- [ ] No passwords, API keys, tokens, or personal Drive links
- [ ] Experimental results (if present) have not been altered

Do not modify numerical experimental results after they have been generated for the paper.

---

## Part 6 — Create a GitHub Release

A DOI is attached to a **specific version**.

1. Open the repository.
2. Go to **Releases** (right sidebar) → **Create a new release**.
3. Tag: `v1.0.0`
4. Release title: `DynTrust-FedIDS++ v1.0.0`
5. Description (suggested):

   ```
   Initial public release of DynTrust-FedIDS++ real-data experimental pipeline,
   including the corrected notebook, requirements, and supporting metadata.
   ```
6. Click **Publish release**.
7. Do not create extra releases unless a new version is needed.

---

## Part 7 — Create / log in to Zenodo

1. Go to https://zenodo.org/
2. Click **Log in**.
3. Prefer “Log in with GitHub” and authorise Zenodo.
4. Use the **same** GitHub account that owns the DynTrust-FedIDS-plusplus repository.

---

## Part 8 — Connect GitHub to Zenodo

1. In Zenodo: account settings → GitHub integration.
2. Enable GitHub if not already enabled.
3. Find the repository **DynTrust-FedIDS-plusplus**.
4. Flip the switch to enable it for Zenodo archiving.
5. Confirm Zenodo has permission to access the repository.

---

## Part 9 — Create the Zenodo deposit

After enabling the repository, Zenodo should detect the GitHub release `v1.0.0`.

Select that release. Complete metadata carefully (you can copy from `zenodo_metadata.json`):

| Field | Value |
|-------|--------|
| **Title** | DynTrust-FedIDS++: Optimization-Based Trust Aggregation for Privacy-Aware Byzantine-Robust Federated Intrusion Detection under Data Drift |
| **Upload type** | Software |
| **Version** | 1.0.0 |
| **License** | MIT |
| **Language** | English |

**Description** (short form is fine):

> DynTrust-FedIDS++ is a federated intrusion-detection framework that combines FISTA optimisation-based trust-weighted aggregation, multi-criteria drift-aware trust, Gaussian differential privacy, and evaluation under sign-flip, Gaussian and ALIE Byzantine attacks on four real flow-level IDS datasets (NF-CSE-CIC-IDS2018, NF-ToN-IoT, UNSW-NB15, CIDDS-001).

---

## Part 10 — Add authors

Add authors **exactly** as they appear in the final manuscript (order and spelling).

- Add ORCID only if the author has a verified ORCID account.
- **Do not invent ORCID IDs.**

Update the `creators` section of `zenodo_metadata.json` before publishing if you use it as a checklist.

---

## Part 11 — Keywords

Suggested keywords (already in zenodo_metadata.json):

- Federated Learning  
- Intrusion Detection  
- Byzantine Robustness  
- Trust-Aware Aggregation  
- Differential Privacy  
- Data Drift  
- Optimisation-based Aggregation  
- FISTA  
- Non-IID  
- Class Imbalance  
- ALIE  
- Network Security  
- IoT Security  

---

## Part 12 — Publish and obtain the DOI

1. Review every field once more.
2. Confirm the correct GitHub release (`v1.0.0`) is selected.
3. Confirm no private information is present.
4. Click **Publish**.
5. Zenodo will assign a DOI of the form:

   ```
   10.5281/zenodo.xxxxxxx
   ```

   **Do not type or invent a DOI yourself.**

---

## Part 13 — Save the DOI

Copy and keep:

1. The DOI (`10.5281/zenodo.xxxxxxx`)
2. The Zenodo record URL

Send both to the corresponding author / manuscript coordinator.

---

## Part 14 — Add the DOI to the GitHub README

Edit `README.md` and replace the placeholder badge with:

```markdown
[![DOI](https://zenodo.org/badge/DOI/10.5281/zenodo.xxxxxxx.svg)](https://doi.org/10.5281/zenodo.xxxxxxx)
```

Commit the change (e.g. “Add Zenodo DOI badge”).

---

## Part 15 — Update the manuscript

The manuscript currently contains a Data Availability Statement that points to the original dataset sources.

Once the software DOI exists, add a sentence such as:

> The experimental pipeline and source code for DynTrust-FedIDS++ are archived at Zenodo: https://doi.org/10.5281/zenodo.xxxxxxx

Replace the placeholder with the real DOI. Never insert a guessed DOI.

---

## Final checklist

### GitHub
- [ ] Account created / verified
- [ ] Repository named `DynTrust-FedIDS-plusplus`
- [ ] Owner is the correct author account
- [ ] Prepared files uploaded
- [ ] README displays correctly
- [ ] Notebook present in root
- [ ] requirements.txt, LICENSE, CITATION.cff present
- [ ] No sensitive information
- [ ] Release `v1.0.0` created

### Zenodo
- [ ] GitHub connected
- [ ] Repository enabled for archiving
- [ ] Release `v1.0.0` selected
- [ ] Title, authors, version, keywords correct
- [ ] Record published
- [ ] DOI generated

### Deliver to manuscript coordinator
1. GitHub repository URL  
2. Zenodo record URL  
3. DOI (`10.5281/zenodo.xxxxxxx`)

The DOI can then be inserted into the manuscript Data Availability Statement and the README badge.
