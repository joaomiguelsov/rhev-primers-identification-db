# RHEV Primers Database

This repository contains curated RHEV primer data associated with the Master's thesis of Margarida Cardeano **"Genomic Diversity and Zoonotic Potential of Hepatitis E Virus in European Rabbits: Implications for Diagnostic and Therapeutic Approaches."** 	https://hdl.handle.net/10216/164527

---

## Overview

This repository organizes two complementary primer datasets for rabbit hepatitis E virus (RHEV): one compiled from published studies (**AROLit**) and one generated *in silico* (**iSOP**) for candidate primer discovery and evaluation. Together, the files include primer sequences, genomic positions, target regions, thermodynamic properties, and pair-level scoring information that support primer comparison and downstream assay development.

---

## Repository Contents

```
RHEV-Primers-Database/
│
├── AroLit_Primers_Database.xlsx     # Literature-derived primer combinations
├── ISOP_Primers_Database_CS85_V1.xlsx       # In silico generated primer combinations
└── README.md                        # This file
```

---

## Dataset Descriptions

### `AroLit_Primers_Database.xlsx`
Contains forward and reverse primer combinations curated from peer-reviewed publications. Each entry includes:
- Forward and reverse primer identifiers and DOI-linked source references
- Nucleotide sequences for forward and reverse primers
- GC content (forward, reverse, combined)
- Melting temperature — Tm (forward, reverse, combined)
- Homodimer and self-complementarity energy values
- Dimer interaction and fold metrics
- Genomic start and end coordinates
- Amplicon length
- Target genomic region (e.g., ORF2, RdRp, Methyltransferase)
- Primer combination score

### `ISOP_Primers_Database_CS85_V1.xlsx`
Contains computationally generated primer combinations (labeled `insilicoprimer`). The structure mirrors `AroLit_Primers_Database.xlsx`, with the same thermodynamic, positional, regional, and scoring fields. This dataset extends the literature-based collection with novel candidate pairs ranked by a custom scoring model.

---

## Data Fields Reference

| Field | Description |
|---|---|
| `ID Forward` / `ID Reverse` | Unique primer identifier |
| `Forward Ref` / `Reverse Ref` | Source reference (DOI or `insilicoprimer`) |
| `Forward Sequence` / `Reverse Sequence` | Oligonucleotide sequence (5'→3') |
| `Forward GC` / `Reverse GC` / `Comb GC` | GC content (%) per primer and combined |
| `Forward Tm` / `Reverse Tm` / `Comb Tm` | Melting temperature (°C) per primer and combined |
| `Forward Homo` / `Reverse Homo` | Homodimer ΔG (kcal/mol) |
| `Forward Self` / `Reverse Self` | Self-complementarity ΔG (kcal/mol) |
| `Dimer` | Heterodimer ΔG between the pair (kcal/mol) |
| `Fold` | Secondary structure folding metric |
| `Forward Start` / `Reverse End` | Genomic coordinates on the reference alignment |
| `Amplicon Length` | Expected PCR amplicon size (bp) |
| `Region` | Target genomic region |
| `Primer Combination Score` | Custom composite score for pair ranking |

---

## Target Genomic Regions

Primer pairs in both datasets target key functional regions of the RHEV genome:

- **ORF2** — Capsid protein-encoding region; primary target for most detection assays
- **RNA-dependent RNA polymerase (RdRp)** — Conserved replication enzyme; suitable for broad-spectrum detection
- **Methyltransferase (Met)** — Non-structural region used in select amplification strategies

---

## Purpose

This repository provides a structured and reusable resource for exploring RHEV primer candidates in the context of genomic diversity, diagnostic development, and zoonotic surveillance. By combining literature-derived primers with *in silico* designs, it supports comparative assessment of existing and newly proposed primer pairs for rabbit HEV research.

---

## Suggested Use

Researchers can use these files to:

1. Review previously reported RHEV primer sequences and their associated literature references
2. Compare thermodynamic properties and predicted interaction metrics across candidate pairs
3. Prioritize primer pairs by genomic target region, amplicon size, and combination score
4. Identify top-ranked candidates for experimental validation in molecular detection workflows

---

## Citation

If you use this repository in your research, please cite the associated Master's thesis:

> **Genomic Diversity and Zoonotic Potential of Hepatitis E Virus in European Rabbits: Implications for Diagnostic and Therapeutic Approaches.**
> Master's Thesis, 2024.

Please cite this resource as follows:

> Pinheiro, Margarida Cardeano; Abrantes, Joana; Lopes, Ana M.; Pratas, Diogo; Carneiro, João.
> **RHEV primers database**, 2024.

---

## Notes

> **Important:** This repository is intended as a research resource. All primer candidates should undergo appropriate laboratory validation before any diagnostic or therapeutic application. Predicted thermodynamic metrics and combination scores are computed values; actual amplification performance may differ depending on experimental conditions, template variability, and assay chemistry.

---

## License

This dataset is made available for academic and research use. Please contact the authors for commercial use inquiries.

---

## Contact

For questions or collaborations, please open an issue in this repository or contact the corresponding authors via the associated thesis institution.
