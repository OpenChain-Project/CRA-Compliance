# CRA-Compliance

This repository defines the organizational compliance framework for the EU Cyber Resilience Act (CRA, Regulation 2024/2847). It serves simultaneously as a policy framework and a self-certification checklist, covering program governance, SBOM quality, vulnerability handling, regulatory reporting, OSS stewardship, and technical file obligations.

## Overview

The CRA (Regulation EU 2024/2847) establishes mandatory cybersecurity requirements for products with digital elements placed on the EU market. Organizations that develop, maintain, or distribute software with digital elements must ensure their products meet essential cybersecurity requirements throughout the product lifecycle.

This framework is:

- Aligned with **OpenChain ISO/IEC 5230** and **ISO/IEC 18974** (Open Source Security Assurance)
- Structured for **self-certification** (Internal Control Module A) for Default and certain Class I products
- Compatible with **CycloneDX** and **SPDX** SBOM formats
- Cross-referenced to **NIS2**, **EU AI Act**, **DORA**, and the **Data Act**

## Repository Contents

| File | Description |
|---|---|
| `versions` | Archive directory for Checklist versions |
| `CRA_Checklist_Requirement_latest.md` | CRA Compliance Checklist and Requirements latest version (182 checklist items) |

## Checklist Structure

The checklist covers 9 sections and 182 requirements:

| Section | Topic | Items |
|---|---|---|
| 2 | Program Architecture and Governance | 46 |
| 3 | Component Management, SBOM Quality and Provenance | 46 |
| 4 | Vulnerability Handling, VEX and Art. 14 Reporting | 35 |
| 5 | OSS Stewardship | 15 |
| 6 | Security Updates and Support Period | 7 |
| 7 | Technical File, DoC and Supply Chain Sharing | 20 |
| 8 | Cross-Framework Integration (NIS2, AI Act, DORA, Data Act) | 8 |
| 9 | Procurement and Buyer-Side Obligations | 5 |

## Key Features

- **Art. 14 three-stage reporting cascade** (24h Early Warning / 72h Notification / 14-day Final Report) with full RACI and tabletop exercise requirements
- **SBOM quality controls** including dependency pinning, provenance, signing, and HBOM for hardware products
- **Secure build infrastructure** and secrets management requirements
- **EU Declaration of Conformity** workflow with Annex V template structure
- **Authorized Representative** operational procedures for non-EU manufacturers
- **Appendix A** - CRA Annex I Traceability Matrix
- **Appendix B** - Definitions and Glossary

## Status

Current version: **RC1 (Release Candidate)**

The document is under active development. Contributions and feedback are welcome via pull requests and issues.

## License

CC-BY-4.0 - See [LICENSE](LICENSE) for details.

## Contributors

| Name | Affiliation |
|---|---|
| Devashri Datta | Independent Researcher / OpenSSF SBOM Everywhere SIG |
| Mary Meixia Wang | OpenChain Project |
| Ummo Schwarting | Open Source Consultant / Chairman, OpenChain Business Operations Study Group |

For checklist contributions see [Contributors section in the Checklist document](CRA_Checklist_Requirement_latest.md#Contributors)
