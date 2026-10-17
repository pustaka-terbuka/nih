# Pustaka Terbuka — NIH (Perpustakaan National Institutes of Health / IMR)

> **Pustaka Terbuka: Katalog Induk Terbuka untuk Perpustakaan dan Sekolah Malaysia.**  
> *Official Perpustakaan National Institutes of Health / IMR (NIH) Bibliographic Dataset & Standalone Harvester.*

This repository contains the harvested open MARCXML collection and harvester pipeline for **Perpustakaan National Institutes of Health / IMR** (`NIH`), contributing to the national Malaysian union catalog at [pustaka-terbuka/opac](https://github.com/pustaka-terbuka/opac).

---

## Institutional Metadata

| Attribute | Value |
| :--- | :--- |
| **Institution Code** | `nih` |
| **Agency Code** | `NIH` |
| **Official Name** | Perpustakaan National Institutes of Health / IMR |
| **Institution Type** | `special` |
| **State / Territory** | Selangor |
| **Target End Bib** | 100,000 |
| **OPAC Base URL** | [https://library.nih.gov.my/](https://library.nih.gov.my/) |
| **Subject Focus** | Medical research, tropical epidemiology, infectious diseases, and health management |

---

## Directory Structure

```text
nih/
├── README.md                      # Institutional repository documentation
├── package.json                   # Node.js project specification & scripts
├── harvest/
│   └── inbox/nih/             # Sealed MARCXML batch chunks and manifests
│       └── <run-id>-chunk-001/
│           ├── manifest.json      # Chunk SHA-256 manifest & metadata
│           ├── provenance.jsonl   # Record-level attribution and fetch logs
│           └── records/           # Batched MARC21 slim XML files
├── tools/
│   ├── harvesters/nih/        # Automated OPAC crawler & XML converter
│   └── lib/                       # Supporting MARCXML and validation utilities
└── tests/
    └── harvester-nih.test.js  # Autonomous test suite
```

---

## Usage

```bash
# Install dependencies
npm install

# Test run harvester (10 sample records)
npm run harvest:sample

# Run full collection sweep
npm run harvest:full

# Validate dataset integrity
npm run validate-inbox harvest/inbox/nih/<chunk-directory>
```

---

## Attribution & License

Dataset harvested and preserved under open library metadata standards for educational, civic, and cooperative indexing. Attribution: **Perpustakaan National Institutes of Health / IMR (NIH)** & **Pustaka Terbuka**.
