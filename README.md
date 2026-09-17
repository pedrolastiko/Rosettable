# 🪨 Rosettable

> *Just as the Rosetta Stone decoded three scripts in parallel, **Rosettable** translates and aligns 9 security frameworks across 17 domains.*

---

## 🌐 Live Demo

👉 **[🪨 Rosettable](https://pedrolastiko.github.io/Rosettable/)**

---

## What is it?

**Rosettable** is an interactive mapping and alignment tool for major cybersecurity and IT governance frameworks. It allows any security professional, architect, or compliance officer to instantly visualize cross-framework correspondences — without having to parse hundreds of pages of documentation.

The name is a deliberate play on words: **Rosetta** (the Stone that unlocked multiple languages at once) + **Table** (the alignment table that is the tool itself) + **-able** (actionable, usable).

---

## Frameworks Covered

| Framework | Version | Scope |
|---|---|---|
| **NIST CSF** | 2.0 | Cybersecurity — Govern, Identify, Protect, Detect, Respond, Recover |
| **ISO/IEC 27001** | 2022 | Information Security Management System (ISMS) |
| **ISO/IEC 42001** | 2023 | Artificial Intelligence Management System (AIMS) |
| **CIS Controls** | v8 | Technical cybersecurity controls (18 controls) |
| **ITIL** | v4 | IT Service Management (SVS, practices) |
| **COBIT** | 2019 | Governance and Management of Enterprise IT (EDM, APO, BAI, DSS, MEA) |
| **NIST AI RMF** | 1.0 | AI Risk Management Framework (Govern, Map, Measure, Manage) |
| **NIST IR 8596 Cyber AI Profile** | Preliminary draft (Dec. 2025) | CSF 2.0 Community Profile for AI — three focus areas: Secure AI system components, Defend with AI-enabled cyber defense, Thwart AI-enabled cyberattacks |
| **EU AI Act** | 2024/1689 | European regulation for trustworthy AI (risk-based obligations, transparency, prohibited practices) |

---

## Domains Covered

| # | Domain |
|---|---|
| 01 | Governance & Security Policy |
| 02 | Risk Management |
| 03 | Asset Management |
| 04 | Access Control & Identity Management (IAM) |
| 05 | Awareness & Training |
| 06 | Physical & Environmental Security |
| 07 | Configuration Management (Hardening) |
| 08 | Data Protection & Encryption |
| 09 | Network Security & Infrastructure |
| 10 | Application Security & DevSecOps |
| 11 | Monitoring & Detection |
| 12 | Incident Response |
| 13 | Continuity & Resilience (BCP/DR) |
| 14 | Supplier Management & TPRM |
| 15 | Compliance, Audit & Improvement |
| 16 | HR Security & Personnel Management |
| 17 | AI Governance & Ethics |

---

## Features

- **🔍 Domain filtering** — display only the domains relevant to your context (Governance, Risk, Technical, Cyber Ops, AI…)
- **🧩 Combined views (IT / Cyber / AI)** — switch from the matrix to a consolidated view of one framework family, where the criteria of each domain are grouped into coherent sub-domains, each criterion keeping its code and its framework of origin
- **👁️ Column toggle** — hide any framework column with a single click to focus on what matters
- **🌙 Light / dark theme** — instant toggle between both display modes
- **🌐 Bilingual FR / EN** — the full interface and all control labels are translated using the official wording of each framework
- **📄 Single-file HTML** — no dependencies, no server, no installation. One `.html` file to open in any browser

---

## Usage

### Option 1 — GitHub Pages

```
https://pedrolastiko.github.io/rosettable/
```

### Option 2 — Intranet / internal portal

Copy the `index.html` file localy or directly into your internal portal. No external dependencies — the file is 100% self-contained.

---

## Technical Architecture

```
rosettable.html          ← single self-contained file
│
├── CSS                  ← light theme + dark theme (CSS custom properties)
├── HTML                 ← matrix table, 17 rows × 9 framework columns + combined-view table (rendered by JS)
└── JavaScript
    ├── toggleTheme()    ← light / dark mode switch
    ├── toggleLanguage() ← FR / EN switch (full i18n)
    ├── toggleNorm()     ← column visibility by framework
    ├── filterDomain()   ← row filtering by domain
    ├── setView()        ← Matrix / IT / Cyber / AI view switch
    └── VIEWS            ← sub-domain groupings per domain and family; criteria are referenced by
                            [framework, code] and their labels are read from the matrix cells
```

**Dependencies:** none. Google Fonts loaded via CDN (optional — falls back to system fonts when offline).

---

## Combined Views

The **IT**, **Cyber** and **AI** buttons replace the matrix with a consolidated view of one framework family:

| View | Frameworks combined |
|---|---|
| IT | ITIL v4, COBIT 2019 |
| Cyber | NIST CSF 2.0, ISO 27001:2022, CIS Controls v8 |
| AI | ISO 42001:2023, NIST AI RMF 1.0, NIST IR 8596 Cyber AI Profile, EU AI Act |

For each of the 17 domains, the criteria of the family are grouped into three to five **sub-domains** ordered in a consistent reading sense (framework and governance → identification and assessment → treatment and controls → monitoring and improvement). Every criterion appears exactly once and keeps its code and its framework of origin. The sub-domain grouping is an editorial proposal by Rosettable, not a structure defined by the standards. Domain filters and framework toggles apply to the combined views as well.

---

## Translation Approach

All control labels are translated using the **official wording** of each framework — not paraphrases:

- **ISO 27001 / 42001** → Annex A control titles from the official English editions
- **NIST CSF 2.0** → Official category and subcategory labels
- **NIST IR 8596 Cyber AI Profile** → CSF 2.0 subcategory IDs, each tagged with its focus area (Secure / Defend / Thwart) and the AI-specific consideration
- **CIS Controls v8** → Official titles of the 18 CIS Controls
- **ITIL v4** → Official practice names (*Incident Management*, *Service Configuration Management*…)
- **COBIT 2019** → Official *Managed…* / *Ensure…* nomenclature

---

## Roadmap

- [ ] **People · Process · Technology** dimension per domain
- [ ] Add **NIS2** (EU Cybersecurity Directive)
- [ ] Add **SOC 2** (Trust Services Criteria)
- [ ] Add **DORA** (Digital Operational Resilience Act)
- [ ] Filtered matrix **PDF / Excel export**
- [ ] Maturity level indicator per control (CMMI-inspired)


---

## Contributing

Contributions are welcome! To suggest a correction, translation improvement, or the addition of a new framework:

1. Fork the repository
2. Create a branch: `feature/framework-name` or `fix/description`
3. Submit a **Pull Request** with a clear description of the changes

> ⚠️ Please use the **official wording** of the standards — not paraphrases or summaries.

---

## License

Distributed under the **MIT License**. See [`LICENSE`](./LICENSE) for details.

---

---

*Rosettable — Decipher your frameworks. Align your controls.*
