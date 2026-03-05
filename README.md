# 🪨 Rosettable

> *Just as the Rosetta Stone decoded three scripts in parallel, **Rosettable** translates and aligns 6 security frameworks across 17 domains.*

---

## 🌐 Live Demo

👉 **[Open Rosettable](https://pedrolastiko.github.io/rosettable)**

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
├── HTML                 ← table structure, 17 rows × 6 framework columns
└── JavaScript
    ├── toggleTheme()    ← light / dark mode switch
    ├── toggleLanguage() ← FR / EN switch (full i18n)
    ├── toggleNorm()     ← column visibility by framework
    └── filterDomain()   ← row filtering by domain
```

**Dependencies:** none. Google Fonts loaded via CDN (optional — falls back to system fonts when offline).

---

## Translation Approach

All control labels are translated using the **official wording** of each framework — not paraphrases:

- **ISO 27001 / 42001** → Annex A control titles from the official English editions
- **NIST CSF 2.0** → Official category and subcategory labels
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
