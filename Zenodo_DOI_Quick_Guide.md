# Zenodo DOI — Quick Link Guide for DynTrust-FedIDS++

## Files in this package

| File | Purpose |
|------|---------|
| `zenodo_deposit_metadata.json` | Full metadata to copy into Zenodo when creating the deposit (before DOI exists) |
| `zenodo_metadata.json` | Shorter metadata checklist |
| `zenodo_doi_link.json` | **Fill this AFTER** Zenodo gives you the real DOI — used to link GitHub ↔ Zenodo ↔ manuscript |

---

## Step-by-step (DOI linking)

### A. Before the DOI exists

1. Create GitHub repo: `DynTrust-FedIDS-plusplus`
2. Upload this package
3. Create GitHub Release **v1.0.0**
4. Log in to https://zenodo.org with the **same** GitHub account
5. Enable the repository under Zenodo → GitHub settings
6. Zenodo detects release `v1.0.0` → create deposit
7. Copy fields from `zenodo_deposit_metadata.json` (title, description, keywords, license, version)
8. Add **real authors** (never invent ORCID)
9. Publish → Zenodo assigns DOI like `10.5281/zenodo.1234567`

### B. After the DOI exists (linking)

1. Open `zenodo_doi_link.json`
2. Replace:
   - `REPLACE_WITH_YOUR_USERNAME`
   - `REPLACE_WITH_DOI_NUMBER` (e.g. `1234567`)
   - `REPLACE_WITH_RECORD_ID`
   - `REPLACE_AUTHORS`
3. Add this line to `README.md` (near the top badges):

```markdown
[![DOI](https://zenodo.org/badge/DOI/10.5281/zenodo.1234567.svg)](https://doi.org/10.5281/zenodo.1234567)
```

4. Add to manuscript **Data Availability Statement**:

> The experimental pipeline and source code for DynTrust-FedIDS++ are archived at Zenodo: https://doi.org/10.5281/zenodo.1234567

5. Commit & push the README update to GitHub.

### C. What to send the coordinator

```
1. GitHub repository URL:  https://github.com/<user>/DynTrust-FedIDS-plusplus
2. Zenodo record URL:      https://zenodo.org/records/<id>
3. DOI:                    10.5281/zenodo.<number>
```

---

## Important rules

- **Never invent or type a fake DOI.** Only use the number Zenodo prints after Publish.
- ORCID: add only if the author has a real, verified ORCID.
- Datasets stay at their original sources; this DOI is for the **code/pipeline**, not the raw traffic data.
