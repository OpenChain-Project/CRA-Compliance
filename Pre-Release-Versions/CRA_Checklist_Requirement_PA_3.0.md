

| OpenChain-Aligned Cyber Resilience Act (CRA) Compliance Requirements & Checklist Self-Certification Document   \-   ISO/IEC 18974 Aligned   \-   EU Regulation 2024/2847 |
| :---- |

   
 

 

| Document Title | CRA Compliance Requirements & Checklist |
| :---- | :---- |
| **Document Type** | Self-Certification / Governance Framework |
| **Current Version** | PA3 |
| **Date** | 29 Jul 2026 |
| **Status** | DRAFT \- Pre-Approval (PA) |
| **Review Cycle** | Annual; additionally triggered by major releases, significant dependency changes, or regulatory guidance updates (see §2.4.2) |
| **Document Owner** | Devashri Datta (Chairman) |
| **Standards Alignment** | ISO/IEC 18974 \- EU CRA (Reg. 2024/2847) \- OpenChain ISO/IEC 5230 |
| **CRA Art. 14 Reporting Deadline** | 11 Sep 2026 \- see §4.4-4.5 for mandatory actions |

   
**Abstract**

**This document defines the organizational compliance framework for the EU Cyber Resilience Act (CRA, Regulation 2024/2847), structured in alignment with the OpenChain Project's adoption framework and ISO/IEC 18974\. It serves simultaneously as a policy framework and a self-certification checklist, covering program governance, SBOM quality, vulnerability handling, regulatory reporting (including the CRA Article 14 three-stage cascade), OSS stewardship, and technical file obligations. This document does not constitute legal advice; consult qualified legal counsel before formal regulatory submission.**

   
 

   
**License:** CC-BY-4.0.  **Community:** OpenChain Project / Linux Foundation  **GitHub:** [github.com/OpenChain-Project/CRA-Compliance](https://github.com/OpenChain-Project/CRA-Compliance)

   
**Important:** All bracketed \[INSERT ...\] fields must be completed with organization-specific information before any compliance claim or self-certification is made.

 

# **Revision History**

 

| Version / Date | Description | Author |
| :---- | :---- | :---- |
| PA1 / 21 Jul 2026 | 1st draft \- full 5-section structure, Art. 14 cascade, §4.5 RACI | Devashri Datta |
| PA3 / 29 Jul 2026 | Incorporated community feedback: §7.4 AR wording corrected (AR is one of three options per Daniel Thompson-Yvetot); §1 applicability table by org role added; ISO/IEC 18974 \+ OWASP SAMM mapping added as Annex C; PT1/PT3 reference added to §2.6 and References; hyperlinks added throughout Guidance column and References section. Total items: 156\. | Devashri Datta |
| 1.0 / TBD | Initial approved release |   |

 

# **Contributors**

   
We would like to express our sincere gratitude to the following contributors and organizations, whose efforts and insights have been invaluable.

| Name | Email | Company | GitHub ID |
| :---- | :---- | :---- | :---- |
| **Devashri Datta (Chairman)** | devashri.datta@gmail.com |   | devashridatta-dotcom |
| **Andreas Kotulla** | \[andreas@bitsea.de \- confirm\] | Bitsea GmbH | \[GitHub ID \- confirm\] |

 

 

# **Section 1: Introduction & Scope**

This document defines the organization's compliance program for the EU Cyber Resilience Act (CRA), structured in alignment with the OpenChain Project's adoption framework and ISO/IEC 18974 (Open Source Security Assurance). It serves as both a policy framework and a self-certification checklist.

The CRA (Regulation (EU) 2024/2847) establishes mandatory cybersecurity requirements for products with digital elements placed on the EU market. Organizations that develop, maintain, or distribute software with digital elements must ensure their products meet essential cybersecurity requirements throughout the product lifecycle.

 

**Scope of this document:**

●  All software products with digital elements placed on the EU market by \[INSERT: Full legal entity name of manufacturer\]

●  Open-source components included in released products

●  Software supply chain processes including SBOM generation, vulnerability management, and disclosure

●  Personnel and processes involved in development, security operations, legal, and compliance

 

**Applicability by Organizational Role**

The CRA creates distinct obligations for different organizational roles. Determine which role(s) apply before completing this checklist. A single organization may occupy multiple roles simultaneously (e.g., a manufacturer that also distributes third-party products). Complete all sections that apply to each role held.

 

| Section | Manufacturer | Importer | Distributor | OSS Steward | Both Mfr+Steward | Notes |
| :---- | :---- | :---- | :---- | :---- | :---- | :---- |
| **§2 Governance** | Required | Required | Required | Recommended | Required | All roles need basic governance |
| **§3.1-3.4 SBOM & SDLC** | Required | N/A | N/A | N/A | Required | Manufacturer builds the product |
| **§3.5 Importer/Distributor** | N/A | Required | Required | N/A | N/A | Only applies to resellers |
| **§4 Vuln Handling** | Required | Partial (4.4 only) | Partial (4.4 only) | N/A | Required | Importers must notify manufacturer |
| **§5 OSS Stewardship** | Optional | Optional | Optional | Required | Required | Core for steward role |
| **§6 Support Period** | Required | N/A | N/A | N/A | Required | Manufacturer sets support period |
| **§7.1-7.4 Technical File** | Required | Verify only | Verify only | N/A | Required | Importers check, not produce |
| **§8 Cross-Framework** | As applicable | As applicable | As applicable | N/A | As applicable | Based on NIS2/DORA/AI Act scope |
| **§9 Procurement** | Optional | Optional | Optional | N/A | Optional | Buyer-side obligation |

 

Role definitions: Manufacturer \- places a product with digital elements on the EU market under its own name or trademark. Importer \- places a product from a non-EU manufacturer on the EU market under the manufacturer's name. Distributor \- makes a product available on the EU market without placing it on the market. OSS Steward \- provides open-source software for integration into products placed on the EU market without commercial activity (CRA Art. 3(14)).

Note on OSS Steward column: "Optional" indicates the section is not typically required by CRA Annex II steward obligations but may be adopted voluntarily to strengthen security posture. "Recommended" indicates good practice that supports steward obligations indirectly. OSS Stewards are not subject to Annex I essential requirements but must maintain a security policy and vulnerability handling process (CRA Annex II).

   
**Important:** All bracketed \[INSERT ...\] fields throughout this document must be completed with organization-specific information before any compliance claim or self-certification is made. Unsigned or incomplete checklists do not constitute a valid conformity claim under CRA Regulation (EU) 2024/2847.

 

Hardware scope note: Hardware-specific requirements (including §3.1.7 Hardware Bill of Materials) apply only to products containing physical hardware components. Software-only organizations may mark hardware-specific items N/A with documented rationale.

   
**Section Deadline & Standards Coverage Reference**

The table below shows, for each checklist section: (1) whether it contains items subject to the 11 Sep 2026 Art. 14 reporting deadline; (2) whether it contains items subject to the 11 Dec 2027 full CRA compliance deadline; and (3) whether the section is covered by ISO/IEC 18974\. Use this table to prioritize implementation effort.

 

| Ref | Section Title | Art. 14 Reporting Deadline (11 Sep 2026\) | CRA Full Compliance Deadline (11 Dec 2027\) | Covered by ISO/IEC 18974? |
| :---- | :---- | :---- | :---- | :---- |
| **2.1** | CRA Policy | No | No | Partial \- §3.1.1 security policy for open source |
| **2.2** | Roles & Responsibilities | No | No | Yes \- §3.4.1 roles and responsibilities |
| **2.3** | Competence & Training | No | No | Yes \- §3.1.2 competence and awareness |
| **2.4** | Sustainability & Review | No | No | Yes \- §3.4.2 program review and continuous improvement |
| **2.5** | Product Risk Categorization | No | Yes \- 11 Dec 2027 | No \- CRA-specific; no 18974 equivalent |
| **2.6** | Harmonized Standards Tracking | No | Yes \- 11 Dec 2027 | No \- CRA-specific regulatory requirement |
| **3.1** | SBOM Generation | Partial \- §3.1.5 SBOM depth required to meet 24h window | Yes \- 11 Dec 2027 | Yes \- §3.2.1-3.2.3 SBOM process and tooling |
| **3.2** | SBOM Data Quality | No | Yes \- 11 Dec 2027 | Yes \- §3.2.2 SBOM completeness and data quality |
| **3.3** | Provenance & Integrity | No | Yes \- 11 Dec 2027 | Yes \- §3.2.3 SBOM provenance and integrity |
| **3.4** | Secure Development Properties | No | Yes \- 11 Dec 2027 | Partial \- §3.3 covers vuln handling; full SDL not in 18974 |
| **3.5** | Importer & Distributor Obligations | No | Yes \- 11 Dec 2027 | No \- CRA-specific legal obligation |
| **4.1** | Vulnerability Ingestion & Monitoring | Yes \- EUVDB and KEV feeds required to detect exploited vulnerabilities before 11 Sep 2026 | No | Yes \- §3.3.1 vulnerability identification process |
| **4.2** | Risk Adjudication & VEX | Yes \- VEX output informs Art. 14 exploitability decisions | No | Yes \- §3.3.2 vulnerability response and remediation |
| **4.3** | Actionable Decisions | Yes \- remediation decisions trigger Art. 14 reporting clock | No | Yes \- §3.3.2 vulnerability remediation process |
| **4.4** | Disclosure & Regulatory Reporting | **YES \- §4.4.2-4.4.5 all subject to 11 Sep 2026 deadline** | No | Partial \- §3.3.3 CVD policy only; ENISA Art. 14 cascade not in 18974 |
| **4.5** | Art. 14 Notification RACI | **YES \- all six items subject to 11 Sep 2026 deadline** | No | No \- CRA Art. 14 regulatory obligation; not covered by 18974 |
| **5.1** | OSS Contribution & Engagement | No | Yes \- 11 Dec 2027 | Partial \- §3.1.1 security policy for open source |
| **5.2** | Steward vs. Maintainer Boundaries | No | Yes \- 11 Dec 2027 | No \- CRA Steward concept is not addressed in 18974 |
| **6.1** | Support Period & Update Obligations | No | Yes \- 11 Dec 2027 | Partial \- §3.3.2 covers patching; 5-year support period not in 18974 |
| **7.1** | Market Surveillance Deliverables | No | Yes \- Technical File required 11 Dec 2027 | Partial \- §3.5.1 conformance documentation |
| **7.2** | Downstream Customer Provisioning | No | Yes \- SBOM delivery required 11 Dec 2027 | Partial \- §3.2.1 SBOM process |
| **7.3** | EU DoC & CE Marking | No | Yes \- required 11 Dec 2027 | Partial \- §3.5.1 conformance documentation; CE marking not in 18974 |
| **7.4** | EU Authorized Representative | No | Yes \- required 11 Dec 2027 if non-EU | No \- CRA-specific legal requirement; not in 18974 |
| **8.1** | CRA and NIS2 | Partial \- NIS2 incident reporting aligns with Art. 14 cascade | No | No \- regulatory cross-mapping not in 18974 |
| **8.2** | CRA and AI Act | No | Yes \- 11 Dec 2027 | No \- regulatory cross-mapping not in 18974 |
| **8.3** | CRA and DORA | No | No | No \- regulatory cross-mapping not in 18974 |
| **8.4** | CRA and Data Act | No | No | No \- regulatory cross-mapping not in 18974 |
| **9.1** | Vendor CRA Qualification | Partial \- §9.1.4 supplier Sep 2026 monitoring capability check | No | No \- procurement obligations not covered by 18974 |

 

# **Section 2: Program Architecture & Governance**

This section establishes the organizational foundation for CRA compliance. Effective governance requires a documented policy commitment, clear role assignments, trained personnel, and a sustainable review cadence to ensure the program remains current across all release cycles.

 

## **2.1 CRA Policy**

A documented, published policy defining the organization's commitment to Cyber Resilience Act compliance and security assurance.

 

| Ref | Requirement | Conformant? (Yes / No / Partial) | Evidence & Rationale | Guidance / Reference |
| :---- | :---- | :---- | :---- | :---- |
| **2.1.1** | \[CRA REQUIREMENT\] The organization SHALL maintain a documented cybersecurity policy for CRA compliance that has been approved by senior management. | ☐ Yes   ☐ No   ☐ Partial |   | Policy document; approval signature or board/exec minute. |
| **2.1.2** | \[CRA REQUIREMENT\] The policy SHALL be published and accessible to all relevant personnel and made publicly available on the organization's website or product portal. | ☐ Yes   ☐ No   ☐ Partial |   | URL or intranet link; screenshot or acknowledgement log. |
| **2.1.3** | \[CRA REQUIREMENT\] The policy SHALL explicitly reference the organization's obligations under CRA Articles 13, 14, and 15\. | ☐ Yes   ☐ No   ☐ Partial |   | Policy text mapped to CRA articles. |
| **2.1.4** | \[CRA REQUIREMENT\] The policy SHALL cover the full product lifecycle: design, development, release, maintenance, and end-of-support. | ☐ Yes   ☐ No   ☐ Partial |   | Lifecycle phase coverage section in policy. |

 

## **2.2 Roles & Responsibilities**

Clear assignment of CRA compliance roles across management, legal, product engineering, and security operations.

 

| Ref | Requirement | Conformant? (Yes / No / Partial) | Evidence & Rationale | Guidance / Reference |
| :---- | :---- | :---- | :---- | :---- |
| **2.2.1** | \[CRA REQUIREMENT\] The organization SHALL designate a named CRA Program Manager with documented authority over compliance program decisions. | ☐ Yes   ☐ No   ☐ Partial |   | RACI chart or org chart with role highlighted. |
| **2.2.2** | \[CRA REQUIREMENT\] Legal or regulatory counsel SHALL have a defined role for interpreting CRA obligations, essential requirements, and regulatory changes. | ☐ Yes   ☐ No   ☐ Partial |   | Legal review sign-off records. |
| **2.2.3** | \[CRA REQUIREMENT\] Product Engineering SHALL have assigned owners for SBOM generation, dependency management, and secure-by-design requirements. | ☐ Yes   ☐ No   ☐ Partial |   | Ticket/backlog owner assignments; job description excerpts. |
| **2.2.4** | \[CRA REQUIREMENT\] Security Operations SHALL have defined responsibilities for vulnerability monitoring, vulnerability exploitability exchange, and incident response under CRA. | ☐ Yes   ☐ No   ☐ Partial |   | SecOps runbook referencing CRA. |
| **2.2.5** | \[GOOD PRACTICE\] Role assignments SHOULD be reviewed and updated at least annually or upon significant organizational change. | ☐ Yes   ☐ No   ☐ Partial |   | Change-log or version history of the RACI document. |

 

## **2.3 Competence & Training**

Requirements for ensuring personnel dealing with CRA compliance, SBOMs, and vulnerability handling are properly trained and maintain current knowledge.

 

| Ref | Requirement | Conformant? (Yes / No / Partial) | Evidence & Rationale | Guidance / Reference |
| :---- | :---- | :---- | :---- | :---- |
| **2.3.1** | \[GOOD PRACTICE\] The organization SHOULD define a training curriculum covering, among others, CRA obligations, SBOM tooling, and vulnerability handling. | ☐ Yes   ☐ No   ☐ Partial |   | Training plan document; LMS catalog entry. |
| **2.3.2** | \[GOOD PRACTICE\] Personnel with CRA compliance responsibilities SHOULD complete required training within a defined review cycle. | ☐ Yes   ☐ No   ☐ Partial |   | Training completion records; LMS export. |
| **2.3.3** | \[GOOD PRACTICE\] Competence requirements (knowledge, skills, experience) SHOULD be documented for each CRA-relevant role. | ☐ Yes   ☐ No   ☐ Partial |   | Role competency matrix. |
| **2.3.4** | \[GOOD PRACTICE\] A mechanism SHOULD exist to keep training current as CRA implementing acts and harmonized standards evolve. | ☐ Yes   ☐ No   ☐ Partial |   | Curriculum review schedule; owner assignment. |

 

## **2.4 Sustainability & Review**

Periodic review processes to ensure CRA compliance mechanisms remain active and up-to-date across release cycles. This subsection also covers compliance exception management (§2.4.6-2.4.8) for recording and governing temporary deviations from controls.

 

| Ref | Requirement | Conformant? (Yes / No / Partial) | Evidence & Rationale | Guidance / Reference |
| :---- | :---- | :---- | :---- | :---- |
| **2.4.1** | \[GOOD PRACTICE\] The CRA compliance program SHOULD be reviewed at least once per calendar year. | ☐ Yes   ☐ No   ☐ Partial |   | Review meeting minutes or audit report dated within 12 months. |
| **2.4.2** | \[GOOD PRACTICE\] Reviews SHOULD be triggered by major product releases, significant dependency changes, or changes to regulatory guidance. | ☐ Yes   ☐ No   ☐ Partial |   | Event-driven review trigger list in governance document. |
| **2.4.3** | \[GOOD PRACTICE\] Review outcomes SHOULD be formally recorded and assigned to responsible owners with target resolution dates. | ☐ Yes   ☐ No   ☐ Partial |   | Issue tracker or action log with owner and due date fields. |
| **2.4.4** | \[CRA REQUIREMENT\] The organization SHALL maintain a process to retire or archive compliance records for end-of-life products. Technical documentation shall be retained for at least 10 years after market placement, or for the duration of the support period if longer (CRA Art. 13(15)). | ☐ Yes   ☐ No   ☐ Partial |   | EoL / archival procedure documentation. |
| **2.4.5** | \[GOOD PRACTICE\] The organization SHOULD conduct periodic internal audits of CRA compliance program effectiveness. | ☐ Yes   ☐ No   ☐ Partial |   | Internal audit plan; audit report; finding tracker. |
| **2.4.6** | \[GOOD PRACTICE\] A compliance exception register SHOULD be maintained to document temporary deviations from controls, including rationale and expiry. | ☐ Yes   ☐ No   ☐ Partial |   | Exception register template; approval workflow. |
| **2.4.7** | \[GOOD PRACTICE\] Each exception SHOULD be assigned a risk owner, a compensating control, and a defined review date. | ☐ Yes   ☐ No   ☐ Partial |   | Exception record with owner, compensating control, and expiry date. |
| **2.4.8** | \[GOOD PRACTICE\] Expired exceptions SHOULD be reviewed and either resolved, renewed with updated justification, or escalated. | ☐ Yes   ☐ No   ☐ Partial |   | Exception renewal procedure; escalation log. |

 

## **2.5 Product Risk Categorization & Conformity Assessment Route**

Before executing self-certification, the organization must determine the CRA product classification (Default, Important Class I, Important Class II, or Critical) per CRA Art. 6, 24, and 32 and Annexes III-IV. Self-certification (Internal Control \- Module A) is only lawful for Default products and certain Class I products using harmonized standards. CRA Annex III lists Important product categories including identity and access management software, password managers, firewalls, network management software, VPNs, and intrusion detection systems.

 

| Ref | Requirement | Conformant? (Yes / No / Partial) | Evidence & Rationale | Guidance / Reference |
| :---- | :---- | :---- | :---- | :---- |
| **2.5.1** | \[CRA REQUIREMENT\] The organization SHALL document whether each in-scope product constitutes a product with digital elements (PDE) under CRA Art. 3(1), distinguishing it from standalone SaaS excluded under Recital 12\. Products whose primary function is remote data processing for a PDE are in CRA scope; standalone SaaS not providing such processing falls under NIS2, not CRA. | ☐ Yes   ☐ No   ☐ Partial |   | Scope determination memo referencing Recital 12 and Commission guidance C(2026) 5252; product-by-product classification table. |
| **2.5.2** | \[CRA REQUIREMENT\] Before selecting a conformity pathway, the organization SHALL determine whether it has an EU establishment. If not EU-established, one of the following SHALL be in place before market placement: (a) an EU Authorized Representative, (b) an EU-based importer, or (c) an EU-based fulfillment service provider. Cross-reference §7.4. | ☐ Yes   ☐ No   ☐ Partial |   | EU establishment confirmation or, where applicable, signed AR mandate, importer agreement, or fulfillment provider contract. |
| **2.5.3** | \[CRA REQUIREMENT\] The organization SHALL formally evaluate each in-scope product against CRA Annex III (Important Class I and II) and Annex IV (Critical) and record a product classification decision with supporting rationale. | ☐ Yes   ☐ No   ☐ Partial |   | Classification register with product name, classification outcome, and decision date. |
| **2.5.4** | \[CRA REQUIREMENT\] For Default products, the organization MAY use self-certification (Internal Control \- Module A) provided the assessment basis is documented. | ☐ Yes   ☐ No   ☐ Partial |   | Self-assessment record referencing applicable harmonized standard or essential requirements mapped to design. |
| **2.5.5** | \[CRA REQUIREMENT\] For Important Class I products, the organization SHALL either: (a) apply a harmonized standard in full and use self-certification, or (b) engage a Notified Body. The decision SHALL be documented and justified. | ☐ Yes   ☐ No   ☐ Partial |   | Notified Body engagement letter OR harmonized standard coverage analysis; classification rationale memo. |
| **2.5.6** | \[CRA REQUIREMENT\] For Important Class II or Critical products, the organization SHALL engage a Notified Body assessment or European Cybersecurity Certification Scheme and track it to completion before EU market placement. | ☐ Yes   ☐ No   ☐ Partial |   | Notified Body contract; assessment status; EU type-examination certificate where required. |
|  |  |  |  |  |
| **2.5.7** | \[CRA REQUIREMENT\] Product classification SHALL be reviewed upon significant product changes and at minimum annually. | ☐ Yes   ☐ No   ☐ Partial |   | Classification review log; change-triggered review records. |
| **2.5.8** | \[CRA REQUIREMENT\] The organization SHALL maintain a documented classification decision tree or equivalent procedure to determine consistently whether new products or significant modifications require reclassification. | ☐ Yes   ☐ No   ☐ Partial |   | Classification decision procedure; examples of classification decisions applied. |

 

## **2.6 Harmonized Standards Tracking**

CRA conformity for Default and Important Class I products depends on harmonized standards under Mandate M/606, being developed by ETSI, CEN, and CENELEC. As of mid-2026, first drafts are emerging but full Annex I coverage is not yet available. The CEN/CENELEC working group standards PT1 (horizontal cybersecurity requirements) and PT3 (vulnerability handling) are advancing toward publication; when published, they will provide the primary harmonized standard basis for Module A self-certification. ISO 27001 and IEC 62443 do not create a presumption of CRA conformity. Monitor PT1/PT3 public drafts via the CEN/CENELEC portal. This section ensures the organization tracks standard development and adjusts its conformity pathway as standards mature.

Informational notice: References in this document to Commission draft guidance (March 2026), PT1, and PT3 are informational and non-binding until formally adopted by the European Commission or published as official harmonized standards under Mandate M/606. Organizations should monitor official publication channels and update their conformity documentation accordingly.

 

| Ref | Requirement | Conformant? (Yes / No / Partial) | Evidence & Rationale | Guidance / Reference |
| :---- | :---- | :---- | :---- | :---- |
| **2.6.1** | \[GOOD PRACTICE\] The organization SHOULD identify which harmonized standards under Standardisation Request M/606 are relevant to its product categories and actively monitor their publication status via ETSI, CEN, and CENELEC. | ☐ Yes   ☐ No   ☐ Partial |   | Standards tracking register; assigned owner; reference to ENISA standards mapping document. Note: CEN/CENELEC PT1 and PT3 are expected by 30 Aug 2026\. |
| **2.6.2** | \[CRA REQUIREMENT\] Where harmonized standards relevant to the product are not yet available, the organization SHALL document the gap and record whether a Notified Body has been engaged (required for Class I products absent harmonized standards). | ☐ Yes   ☐ No   ☐ Partial |   | Conformity pathway decision log; Notified Body engagement record or written rationale. |
| **2.6.3** | \[CRA REQUIREMENT\] The organization SHALL NOT rely on ISO 27001, IEC 62443, or equivalent general security standards as a sole basis for CRA conformity assessment. CRA conformity SHALL be assessed against Annex I requirements directly, pending M/606 finalization. | ☐ Yes   ☐ No   ☐ Partial |   | Written acknowledgement in conformity documentation. |
| **2.6.4** | \[GOOD PRACTICE\] A trigger SHOULD exist to update the conformity pathway and re-run self-certification when a relevant M/606 harmonized standard is published. | ☐ Yes   ☐ No   ☐ Partial |   | Standards publication monitoring procedure; update trigger defined in program governance. |

 

 

# **Section 3: Component Management & SBOM Quality**

This section governs the quality and integrity of Software Bills of Materials (SBOMs). CRA Article 13 requires manufacturers to document components with sufficient granularity to identify known vulnerabilities. OpenChain ISO/IEC 18974 requires a documented process for component identification and vulnerability tracking.

 

## **3.1 Software Identification & Bill of Materials**

Processes for automatically generating and managing machine-readable SBOMs for all released products and dependencies.

 

| Ref | Requirement | Conformant? (Yes / No / Partial) | Evidence & Rationale | Guidance / Reference |
| :---- | :---- | :---- | :---- | :---- |
| **3.1.1** | \[CRA REQUIREMENT\] The organization SHALL maintain a documented process for generating machine-readable SBOMs for all released products and their major dependencies. | ☐ Yes   ☐ No   ☐ Partial |   | SBOM generation procedure; tool configuration (e.g., Syft, Trivy, CycloneDX CLI). Reference: BSI TR-03183. |
| **3.1.2** | \[CRA REQUIREMENT\] SBOMs SHALL be produced in a commonly used, machine-readable format, such as a currently supported version of SPDX or CycloneDX, and SHALL comply with any applicable implementing acts, harmonized standards, or common specifications. | ☐ Yes   ☐ No   ☐ Partial |   | Sample SBOM file; format validation report. Reference: BSI TR-03183-2 for SBOM content requirements. |
| **3.1.3** | \[GOOD PRACTICE\] SBOM generation SHOULD be integrated into the CI/CD pipeline and produce an artifact on every release build. | ☐ Yes   ☐ No   ☐ Partial |   | Pipeline configuration excerpt; build artifact manifest. |
| **3.1.4** | \[CRA REQUIREMENT\] SBOMs SHALL cover, at minimum, top-level dependencies and, where feasible, it is recommended to SHALL include transitive and embedded dependencies to the depth necessary to identify, assess, and remediate vulnerabilities affecting the product. Any components or dependency levels not covered shall be documented together with a risk-based justification and the alternative measures used to ensure effective vulnerability management. | ☐ Yes   ☐ No   ☐ Partial |   | Tooling depth configuration; documented exclusions with risk-based justification; sample SBOM component count vs. dependency graph audit. |
| **3.1.5** | ⚠ DEADLINE: 11 Sep 2026 \- \[CRA REQUIREMENT\] The organization SHALL document a target SBOM depth decision with operational rationale tied to the ability to determine within 24 hours whether a newly published CVE affects any shipped product. A top-level-only SBOM is insufficient for transitive-dependency scenarios. | ☐ Yes   ☐ No   ☐ Partial |   | SBOM depth policy; operational rationale linking depth to 24-hour window; evidence of automated CVE-to-SBOM matching test. |
| **3.1.6** | \[CRA REQUIREMENT\] Each SBOM SHALL include product-level metadata (product name, version, supplier, release date, unique product identifier) and component-level metadata (component name, version, supplier, unique component identifier such as PURL or CPE, and cryptographic hash) for each component. Reference BSI TR-03183-2 for detailed field specifications. | ☐ Yes   ☐ No   ☐ Partial |   | SBOM field mapping to NTIA minimum elements, CRA Annex I, and BSI TR-03183-2. Reference: https://www.bsi.bund.de/TR03183 |
| **3.1.7** | \[GOOD PRACTICE\] For products containing physical hardware components, a Hardware Bill of Materials (HBOM) SHOULD be maintained alongside the SBOM to identify hardware components and their firmware dependencies. Software-only organizations MAY mark this item N/A with documented rationale. | ☐ Yes   ☐ No   ☐ Partial |   | HBOM in a machine-readable format; hardware component inventory; firmware version register. |
| **3.1.8** | \[GOOD PRACTICE\] The organization SHOULD maintain a dependency registry with pinned versions and approved component entries to ensure SBOM reproducibility across builds. | ☐ Yes   ☐ No   ☐ Partial |   | Dependency lock files; package registry configuration; approved component list. |

 

## **3.2 Data Quality & Completeness**

Criteria for validating SBOM completeness, component granularity, and handling Known Unknowns, distinguishing genuinely unknown components from intentionally withheld proprietary code.

 

| Ref | Requirement | Conformant? (Yes / No / Partial) | Evidence & Rationale | Guidance / Reference |
| :---- | :---- | :---- | :---- | :---- |
| **3.2.1** | \[GOOD PRACTICE\] A completeness validation gate SHOULD be applied to SBOMs before release, using automated or manual review. | ☐ Yes   ☐ No   ☐ Partial |   | SBOM linting tool output (e.g., sbom-scorecard, ort); CI gate pass/fail log. |
| **3.2.2** | \[CRA REQUIREMENT\] The organization SHALL maintain a defined policy for handling Known Unknowns \- components whose identity cannot be fully determined \- distinguishing them from intentionally withheld proprietary code. | ☐ Yes   ☐ No   ☐ Partial |   | Policy text or SBOM annotation convention for unknown components. |
| **3.2.3** | \[CRA REQUIREMENT\] Minimum required SBOM fields per CRA Annex I and BSI TR-03183-2 SHALL be validated for every component before SBOM sign-off. | ☐ Yes   ☐ No   ☐ Partial |   | Validation rule set; example of a rejected SBOM and remediation. |
| **3.2.4** | \[GOOD PRACTICE\] Quality metrics for SBOMs (e.g., completeness score, field population rate) SHOULD be tracked and reviewed periodically. | ☐ Yes   ☐ No   ☐ Partial |   | Dashboard screenshot or metrics report. |

 

## **3.3 Provenance & Integrity**

Mechanisms for verifying software origins, tamper prevention, change tracking across release cycles, and secure build infrastructure. Items 3.3.5-3.3.12 cover secure build infrastructure and secrets management requirements.

 

| Ref | Requirement | Conformant? (Yes / No / Partial) | Evidence & Rationale | Guidance / Reference |
| :---- | :---- | :---- | :---- | :---- |
| **3.3.1** | \[CRA REQUIREMENT\] All components in released products SHALL have a verified source (upstream repository URL, commit hash, or verified package registry coordinates). | ☐ Yes   ☐ No   ☐ Partial |   | SBOM externalRef fields; PURL entries; reproducible-build artifacts. |
| **3.3.2** | \[CRA REQUIREMENT\] Cryptographic checksums (SHA-256 or stronger) SHALL be recorded for all binary and source artifacts included in releases. | ☐ Yes   ☐ No   ☐ Partial |   | Artifact manifest with hash values; signing key documentation. |
| **3.3.3** | \[GOOD PRACTICE\] A change-tracking mechanism SHOULD record component additions, removals, and version updates between releases. | ☐ Yes   ☐ No   ☐ Partial |   | SBOM diff report between consecutive releases; changelog integration. |
| **3.3.4** | \[GOOD PRACTICE\] Software signing or attestation (e.g., Sigstore, in-toto, SLSA provenance) SHOULD be applied to release artifacts. | ☐ Yes   ☐ No   ☐ Partial |   | Signing workflow; verification command for customers. SLSA framework: [slsa.dev](https://slsa.dev). |
| **3.3.5** | \[GOOD PRACTICE\] The organization SHOULD maintain a documented secure build infrastructure policy covering build environment isolation, reproducibility, and integrity verification. | ☐ Yes   ☐ No   ☐ Partial |   | Build environment configuration; reproducible build evidence; infrastructure-as-code repository. |
| **3.3.6** | \[GOOD PRACTICE\] Build pipelines SHOULD be isolated from development environments and access to production build systems SHALL be restricted to authorized personnel. | ☐ Yes   ☐ No   ☐ Partial |   | Access control policy for build systems; audit log of build system access. |
| **3.3.7** | \[GOOD PRACTICE\] Build artifacts SHOULD be generated in a clean, reproducible environment and verified before promotion to release. | ☐ Yes   ☐ No   ☐ Partial |   | Build verification procedure; clean-room build evidence. |
| **3.3.8** | \[GOOD PRACTICE\] Secrets (API keys, signing keys, credentials) SHALL NOT be embedded in source code or build artifacts. A secrets management solution SHOULD be used. | ☐ Yes   ☐ No   ☐ Partial |   | Secrets scanning tool configuration; secrets management policy; tool output showing no embedded secrets. |
| **3.3.9** | \[GOOD PRACTICE\] Signing keys used for release artifact attestation SHOULD be stored in a hardware security module (HSM) or equivalent key management system. | ☐ Yes   ☐ No   ☐ Partial |   | Key management policy; HSM or KMS configuration evidence. |
| **3.3.10** | \[GOOD PRACTICE\] The organization SHOULD document the full chain of custody from source code commit to released artifact, enabling post-incident provenance analysis. | ☐ Yes   ☐ No   ☐ Partial |   | Build provenance attestation (e.g., SLSA provenance); artifact lineage documentation. |
| **3.3.11** | \[GOOD PRACTICE\] Third-party build tools, compilers, and dependencies used in the build pipeline SHOULD be inventoried, version-pinned, and monitored for vulnerabilities. | ☐ Yes   ☐ No   ☐ Partial |   | Build tool inventory; version pinning configuration; vulnerability monitoring scope including build tools. |
| **3.3.12** | \[GOOD PRACTICE\] The integrity of the build pipeline itself SHOULD be verified periodically through pipeline audits or automated integrity checks. | ☐ Yes   ☐ No   ☐ Partial |   | Pipeline audit records; integrity check configuration; anomaly detection evidence. |

 

## **3.4 Secure Development Properties & Security Testing (CRA Annex I, Part I)**

CRA Annex I, Part I mandates that products are designed, developed, and produced with security by default. This subsection covers pre-release secure coding properties and testing evidence required to substantiate conformity. Items here also supply required content for the Technical File (§7.1). OWASP SAMM provides a structured maturity model for SDL implementation \- see Annex C for mapping.

 

| Ref | Requirement | Conformant? (Yes / No / Partial) | Evidence & Rationale | Guidance / Reference |
| :---- | :---- | :---- | :---- | :---- |
| **3.4.1** | \[CRA REQUIREMENT\] Products SHALL be delivered without default credentials. Where authentication is required, users SHALL be prompted to set unique credentials on first use and default-deny network exposure SHALL apply (CRA Annex I Part I). | ☐ Yes   ☐ No   ☐ Partial |   | Secure configuration policy; product startup flow documentation; credential policy test records. |
| **3.4.2** | \[CRA REQUIREMENT\] Attack surface minimization SHALL be applied: unnecessary ports, services, and interfaces SHALL be disabled by default and documented in an inbound connections register. | ☐ Yes   ☐ No   ☐ Partial |   | Secure defaults checklist; inbound connections register; network exposure map; hardening guide. |
| **3.4.3** | \[CRA REQUIREMENT\] Data in transit SHALL be encrypted using current standards (TLS 1.2 or higher or equivalent). Data at rest SHALL be encrypted where the cybersecurity risk assessment identifies sensitivity. | ☐ Yes   ☐ No   ☐ Partial |   | Encryption policy; TLS configuration audit; data classification map. |
| **3.4.4** | \[CRA REQUIREMENT\] Memory-safety mechanisms SHALL be applied where technically feasible (e.g., memory-safe languages, compiler mitigations such as ASLR, stack canaries, CFI). Any exceptions SHALL be documented with compensating controls. | ☐ Yes   ☐ No   ☐ Partial |   | Build flag configuration; language or runtime selection rationale; exception register. |
| **3.4.5** | \[CRA REQUIREMENT\] Static Application Security Testing (SAST) SHALL be integrated into the CI/CD pipeline and executed on every release candidate. Critical and high findings SHALL be resolved or formally risk-accepted before release. | ☐ Yes   ☐ No   ☐ Partial |   | SAST tool configuration; scan results summary; finding disposition records. |
| **3.4.6** | \[CRA REQUIREMENT\] Dynamic Application Security Testing (DAST) or fuzzing SHALL be applied at minimum on each major release and results SHALL be documented. | ☐ Yes   ☐ No   ☐ Partial |   | DAST or fuzzing tool output; results triage records; remediation evidence. |
| **3.4.7** | \[CRA REQUIREMENT\] Penetration testing or a structured threat-model-based security review SHALL be performed at minimum annually or upon significant architectural change. An independent assessment SHOULD be used periodically. Findings SHALL be tracked to remediation. | ☐ Yes   ☐ No   ☐ Partial |   | Pentest report or security review record; finding tracker; remediation sign-off. |
| **3.4.8** | \[CRA REQUIREMENT\] Security testing evidence (SAST results, pentest reports, DAST outputs) SHALL be retained as part of the Technical File. Retention period: at least 10 years after market placement, or the support period if longer (CRA Art. 13(15)). | ☐ Yes   ☐ No   ☐ Partial |   | Technical File index entry for security testing artifacts; retention policy. |
| **3.4.9** | \[CRA REQUIREMENT\] A threat model SHALL be produced for each product, covering the attack surface, threat actors, attack vectors, and mitigating controls. The threat model SHALL be updated upon significant architectural change. | ☐ Yes   ☐ No   ☐ Partial |   | Threat model document; methodology used (e.g., STRIDE, PASTA); update history. |
| **3.4.10** | \[CRA REQUIREMENT\] A documented release security gate SHALL exist and SHALL be passed before any product version is placed on the EU market. The gate SHALL verify that all critical and high security findings are resolved or formally risk-accepted. | ☐ Yes   ☐ No   ☐ Partial |   | Release gate checklist; sign-off evidence; exception log for accepted risks. |
| **3.4.11** | \[GOOD PRACTICE\] The organization SHOULD maintain a documented secure coding standard covering input validation, authentication, session management, error handling, and cryptographic usage, and SHALL train developers on its application. | ☐ Yes   ☐ No   ☐ Partial |   | Secure coding standard document; developer training records. |

 

## **3.5 Importer and Distributor Obligations**

CRA Art. 19 and Art. 20 place independent obligations on importers and distributors of products with digital elements. These obligations apply in addition to \- not instead of \- the manufacturer obligations in §§2-3.4. Organizations that import or resell products must complete this sub-section.

 

| Ref | Requirement | Conformant? (Yes / No / Partial) | Evidence & Rationale | Guidance / Reference |
| :---- | :---- | :---- | :---- | :---- |
| **3.5.1** | \[CRA REQUIREMENT\] Before placing an imported product on the EU market, the organization SHALL verify: (a) the manufacturer has completed the appropriate conformity assessment; (b) required technical documentation exists; (c) the product bears CE marking and includes the EU Declaration of Conformity; (d) the manufacturer has a vulnerability handling process in place for the declared support period (CRA Art. 19). | ☐ Yes   ☐ No   ☐ Partial |   | Importer due-diligence checklist per product; manufacturer conformity evidence on file; CE mark verification record. |
| **3.5.2** | \[CRA REQUIREMENT\] If the organization has reason to believe an imported product is not in conformity with the CRA, it SHALL NOT place it on the market until conformity is achieved, and SHALL inform the manufacturer and, where appropriate, market surveillance authorities (CRA Art. 19). | ☐ Yes   ☐ No   ☐ Partial |   | Non-conformity hold procedure; example record of a hold or escalation. |
| **3.5.3** | \[CRA REQUIREMENT\] As a distributor, the organization SHALL verify the product bears CE marking, includes required instructions and information, and meets essential requirements before making it available. If the distributor becomes aware of a vulnerability or cybersecurity risk in a distributed product, it SHALL notify the manufacturer and cooperate with market surveillance authorities (CRA Art. 20). | ☐ Yes   ☐ No   ☐ Partial |   | Distributor due-diligence checklist; vulnerability notification procedure to manufacturer; market surveillance cooperation record. |
| **3.5.4** | \[CRA REQUIREMENT\] System integrators who combine components from multiple manufacturers into a solution placed on the EU market SHALL formally determine whether they are acting as a manufacturer under the CRA. If so, the full conformity assessment obligation applies to the integrated system. | ☐ Yes   ☐ No   ☐ Partial |   | System integrator role determination memo; legal sign-off; conformity assessment plan for the integrated system if applicable. |

 

 

# **Section 4: Vulnerability Handling & VEX (CRA Article 13 Alignment)**

CRA Article 13(6) requires manufacturers to address vulnerabilities without undue delay. Article 14 establishes a mandatory three-stage reporting cascade to the EU CRA Single Reporting Platform (EUVDB) for actively exploited vulnerabilities and severe security incidents. This section defines the end-to-end vulnerability lifecycle from ingestion through disclosure and regulatory notification.

 

## **4.1 Vulnerability Ingestion & Monitoring**

Process for continuously checking software components against known vulnerability databases and advisory feeds.

 

| Ref | Requirement | Conformant? (Yes / No / Partial) | Evidence & Rationale | Guidance / Reference |
| :---- | :---- | :---- | :---- | :---- |
| **4.1.1** | \[CRA REQUIREMENT\] During the support period, the organization SHALL continuously monitor all identified software components contained in supported products against relevant vulnerability databases, supplier advisories, and other reliable vulnerability sources. Monitoring SHALL be performed at a documented, risk-based frequency and at least daily where automated monitoring is available. Known gaps in component coverage SHALL be documented and addressed through supplementary identification and monitoring measures. | ☐ Yes   ☐ No   ☐ Partial |   | Tool configuration; EUVD (euvd.enisa.europa.eu) feed; NVD, OSV, GitHub Advisory feeds; example alert triggered by a new CVE. |
| **4.1.2** | \[GOOD PRACTICE\] Monitoring results SHOULD be logged and retained for audit purposes. | ☐ Yes   ☐ No   ☐ Partial |   | Scan schedule configuration; log retention policy. |
| **4.1.3** | \[GOOD PRACTICE\] A defined intake process SHOULD triage new vulnerability alerts within a documented, risk-based SLA. | ☐ Yes   ☐ No   ☐ Partial |   | Triage SLA table in vulnerability management policy. |
| **4.1.4** | \[GOOD PRACTICE\] Vulnerability data SHOULD be enriched with contextual scoring (e.g., EPSS, KEV catalog status) to support risk-based prioritization. A documented Patch SLA Matrix SHOULD define response timelines by severity tier. | ☐ Yes   ☐ No   ☐ Partial |   | Enrichment pipeline documentation; Patch SLA Matrix; example enriched alert record. |
| **4.1.5** | \[CRA REQUIREMENT\] The EU Vulnerability Database (EUVD, operated by ENISA at euvd.enisa.europa.eu) SHALL be included as a monitored ingestion feed. EUVD is the authoritative CRA source and may publish actively-exploited status ahead of other sources. | ☐ Yes   ☐ No   ☐ Partial |   | EUVD feed configuration; monitoring tool screenshot showing EUVD as an ingestion source. |
| **4.1.6** | \[GOOD PRACTICE\] The CISA Known Exploited Vulnerabilities (KEV) catalog SHOULD be monitored as a trigger for immediate CRA reporting assessment. A KEV listing for any component in a shipped product SHOULD automatically initiate the Art. 14 Early Warning evaluation workflow. | ☐ Yes   ☐ No   ☐ Partial |   | KEV monitoring configuration; documented linkage between KEV listing event and Art. 14 RACI trigger. |
| **4.1.7** | \[GOOD PRACTICE\] Vulnerability monitoring SHOULD extend to third-party and open-source components for which the manufacturer has not received an SBOM from the upstream supplier, using supplementary identification methods. | ☐ Yes   ☐ No   ☐ Partial |   | Supplementary monitoring procedure for components without upstream SBOM; tooling configuration. |
| **4.1.8** | \[GOOD PRACTICE\] Vulnerability management KPIs (e.g., mean time to detect, mean time to remediate by severity tier, percentage of components with confirmed monitoring coverage) SHOULD be tracked and reviewed periodically. | ☐ Yes   ☐ No   ☐ Partial |   | KPI dashboard or metrics report; review cadence documentation. |

 

## **4.2 Risk Adjudication & VEX**

Evaluating vulnerability exploitability in context: reachability, environment, safety relevance and outputting machine-readable VEX statements.

 

| Ref | Requirement | Conformant? (Yes / No / Partial) | Evidence & Rationale | Guidance / Reference |
| :---- | :---- | :---- | :---- | :---- |
| **4.2.1** | \[CRA REQUIREMENT\] The organization SHALL maintain a documented vulnerability exploitability assessment process covering reachability analysis, exploitability in context, and environmental factors. | ☐ Yes   ☐ No   ☐ Partial |   | Vulnerability exploitability assessment process document; assessment criteria checklist. Reference: CISA VEX minimum viable guidelines. |
| **4.2.2** | \[GOOD PRACTICE\] Vulnerability exploitability statements SHOULD be issued in a machine-readable format conforming to a recognised vulnerability exchange standard. Accepted formats include CSAF v2.0 VEX profile, CycloneDX 1.4+ VEX, or OpenVEX. | ☐ Yes   ☐ No   ☐ Partial |   | Sample exploitability statement; tooling used (e.g., Interlynk vexctl, CycloneDX CLI, OpenVEX tooling). |
| **4.2.3** | \[GOOD PRACTICE\] Exploitability statements SHOULD conform to the native status vocabulary and justification fields of the chosen standard without modification. The chosen standard's status values SHALL be used as defined (e.g., CSAF: fixed, known\_affected, known\_not\_affected, under\_investigation; CycloneDX: not\_affected, affected, fixed, under\_investigation, false\_positive). | ☐ Yes   ☐ No   ☐ Partial |   | Exploitability statement status mapping table; sample justified statements per chosen standard. |
| **4.2.4** | \[GOOD PRACTICE\] Exploitability statements SHOULD be versioned, timestamped, and retained as part of the product's technical documentation. | ☐ Yes   ☐ No   ☐ Partial |   | Exploitability statement archive; version control history. |
| **4.2.5** | \[GOOD PRACTICE\] A Safety Relevance classification SHOULD be applied to components where functional safety or AI/autonomous system context applies (e.g., SRIL/SRAP framework or equivalent). Organizations without safety-critical products MAY mark this item N/A with documented rationale. | ☐ Yes   ☐ No   ☐ Partial |   | Safety relevance scoring methodology; component classification register. |

 

## **4.3 Actionable Decisions**

Defined criteria for four clear operational outcomes: Immediate Remediation, Monitored Deferral, Formal Risk Acceptance, and Escalation.

 

| Ref | Requirement | Conformant? (Yes / No / Partial) | Evidence & Rationale | Guidance / Reference |
| :---- | :---- | :---- | :---- | :---- |
| **4.3.1** | \[CRA REQUIREMENT\] The organization SHALL document decision criteria for immediate remediation (e.g., actively exploited vulnerability confirmed, CVSS base score meeting a defined threshold, or safety-critical component affected). | ☐ Yes   ☐ No   ☐ Partial |   | Decision matrix or policy text defining remediation triggers. |
| **4.3.2** | \[GOOD PRACTICE\] Decision criteria for monitored deferral SHOULD be documented, including maximum deferral window and re-assessment trigger. | ☐ Yes   ☐ No   ☐ Partial |   | Deferral SLA table; re-assessment schedule. |
| **4.3.3** | \[GOOD PRACTICE\] Formal risk acceptance SHALL require documented business justification, a named risk owner, and a defined expiry date. | ☐ Yes   ☐ No   ☐ Partial |   | Risk acceptance form template; approval workflow. |
| **4.3.4** | \[CRA REQUIREMENT\] The organization SHALL define escalation criteria and escalation paths, including when regulatory notification under CRA Art. 14 is triggered. | ☐ Yes   ☐ No   ☐ Partial |   | Escalation matrix; contact list with roles. |
| **4.3.5** | \[GOOD PRACTICE\] All vulnerability disposition outcomes SHOULD be tracked in a vulnerability register with current status, owner, and resolution date. | ☐ Yes   ☐ No   ☐ Partial |   | Vulnerability register schema; sample populated record. |

 

## **4.4 Disclosure & Regulatory Reporting (CRA Art. 14 Three-Stage Cascade)**

Standard operating procedures for publicly disclosing fixes, providing mitigation guidance, and meeting the three-stage CRA Article 14 regulatory reporting cascade: Early Warning (24h), Full Notification (72h), and Final Report (14 days). Items marked with DEADLINE are required before 11 Sep 2026\.

 

| Ref | Requirement | Conformant? (Yes / No / Partial) | Evidence & Rationale | Guidance / Reference |
| :---- | :---- | :---- | :---- | :---- |
| **4.4.1** | \[CRA REQUIREMENT\] The organization SHALL maintain a security advisory process to notify affected customers and users without undue delay regarding actively exploited vulnerabilities or severe security incidents, including available mitigations and corrective actions (CRA Art. 14(8)). | ☐ Yes   ☐ No   ☐ Partial |   | Advisory template; distribution channel list (CVE.org, product portal, mailing list). |
| **4.4.2** | ⚠ DEADLINE: 11 Sep 2026 \- \[CRA REQUIREMENT\] Actively exploited vulnerabilities SHALL be reported to ENISA via the CRA Single Reporting Platform (SRP) within 24 hours of the organization becoming aware of active exploitation (CRA Art. 14(2)(a) \- Early Warning). | ☐ Yes   ☐ No   ☐ Partial |   | SRP submission runbook; on-call contact for SRP platform access; test submission record. |
| **4.4.3** | ⚠ DEADLINE: 11 Sep 2026 \- \[CRA REQUIREMENT\] A full vulnerability notification SHALL be submitted to the CRA Single Reporting Platform (SRP) without undue delay and, in any event, within 72 hours after the manufacturer becomes aware of the actively exploited vulnerability, including severity assessment, affected versions, and interim mitigations (CRA Art. 14(2)(b) \- Full Notification). | ☐ Yes   ☐ No   ☐ Partial |   | Full notification template mapped to SRP required fields; 72-hour SLA documented in runbook. |
| **4.4.4** | ⚠ DEADLINE: 11 Sep 2026 \- \[CRA REQUIREMENT\] A final report SHALL be submitted to the CRA Single Reporting Platform (SRP) within 14 days after a corrective or mitigating measure becomes available, including root-cause analysis, remediation details, and disclosure timeline information (CRA Art. 14(2)(c) \- Final Report). | ☐ Yes   ☐ No   ☐ Partial |   | Final report template; post-incident review procedure; 14-day SLA clock definition. |
| **4.4.5** | ⚠ DEADLINE: 11 Sep 2026 \- \[CRA REQUIREMENT\] Severe security incidents impacting the availability, integrity, or confidentiality of a product with digital elements SHALL be reported to ENISA via the CRA Single Reporting Platform (SRP) following the same three-stage cascade (CRA Art. 14(3)). The final report for severe incidents SHALL be submitted within one month of the initial notification. | ☐ Yes   ☐ No   ☐ Partial |   | Severe security incident definition document (aligns with NIS2 thresholds); incident triage criteria; one-month final report template. |
| **4.4.6** | \[CRA REQUIREMENT\] Affected customers and users SHALL be notified without undue delay regarding actively exploited vulnerabilities or severe security incidents, including available mitigations and corrective actions (CRA Art. 14(8)). | ☐ Yes   ☐ No   ☐ Partial |   | Customer advisory template; notification runbook; mailing list, portal, or security advisory feed evidence. |
| **4.4.7** | \[CRA REQUIREMENT\] The organization SHALL publish a Coordinated Vulnerability Disclosure (CVD) policy covering researcher contact channel, response SLA, and safe harbor statement. | ☐ Yes   ☐ No   ☐ Partial |   | CVD policy URL; security.txt file. Reference: ISO/IEC 30111 and 29147\. |
| **4.4.8** | \[CRA REQUIREMENT\] Where a security update is not immediately available, the organization SHALL issue mitigation guidance (workarounds, configuration changes) to affected users without undue delay. | ☐ Yes   ☐ No   ☐ Partial |   | Example advisory with mitigation section. |
| **4.4.9** | \[CRA REQUIREMENT\] The organization SHALL formally identify the national CSIRT to which CRA Art. 14 reports are addressed. Where no EU establishment exists, the CSIRT is determined by where key cybersecurity decisions are made within the Union. This determination SHALL be documented and reviewed annually. Note: CSIRT routing via an Authorized Representative is not among the formal AR obligations defined in CRA Art. 18(3) and should not be assumed as a standard pathway. | ☐ Yes   ☐ No   ☐ Partial |   | CSIRT routing determination memo; reference to Delegated Regulation (EU) 2026/881. |
| **4.4.10** | \[CRA REQUIREMENT\] The organization SHALL document that the SME fine exemption under CRA Art. 14 covers only the financial penalty for missing the 24-hour Early Warning window and does NOT exempt the organization from the reporting obligation itself. | ☐ Yes   ☐ No   ☐ Partial |   | Written acknowledgement in compliance program documentation; Art. 14 RACI maintained regardless of SME status. |
| **4.4.11** | \[CRA REQUIREMENT\] The organization SHALL be aware that under Delegated Regulation (EU) 2026/881, the receiving CSIRT MAY delay dissemination to other member state CSIRTs on justified cybersecurity grounds. Any delay must be strictly limited and ENISA must be informed immediately. The Art. 14 runbook SHALL reference this mechanism. | ☐ Yes   ☐ No   ☐ Partial |   | Art. 14 runbook section on CSIRT dissemination delay; reference to Delegated Regulation (EU) 2026/881. |

 

## **4.5 Art. 14 Notification RACI \- Roles & Trigger Ownership**

CRA Article 14 imposes hard time-based obligations that require pre-assigned, tested role ownership. All items in this section must be completed before 11 Sep 2026\.

 

| Ref | Requirement | Conformant? (Yes / No / Partial) | Evidence & Rationale | Guidance / Reference |
| :---- | :---- | :---- | :---- | :---- |
| **4.5.1** | ⚠ DEADLINE: 11 Sep 2026 \- \[CRA REQUIREMENT\] The organization SHALL designate a named individual (by role) as the Art. 14 Notification Owner responsible for initiating the Early Warning submission to the CRA Single Reporting Platform (SRP) within the 24-hour clock. | ☐ Yes   ☐ No   ☐ Partial |   | RACI table entry; named backup; on-call schedule. |
| **4.5.2** | ⚠ DEADLINE: 11 Sep 2026 \- \[CRA REQUIREMENT\] The organization SHALL designate a named individual (by role) responsible for completing and submitting the 72-hour Full Notification to the CRA Single Reporting Platform (SRP), empowered to escalate to legal or executive if additional approvals are required. | ☐ Yes   ☐ No   ☐ Partial |   | RACI table entry; escalation path documented. |
| **4.5.3** | ⚠ DEADLINE: 11 Sep 2026 \- \[CRA REQUIREMENT\] The organization SHALL designate a named individual (by role) to own the 14-day Final Report for actively exploited vulnerabilities and the one-month final report for severe incidents, coordinate post-incident review inputs, and sign off on the submission. | ☐ Yes   ☐ No   ☐ Partial |   | RACI table entry; final report review workflow. |
| **4.5.4** | ⚠ DEADLINE: 11 Sep 2026 \- \[CRA REQUIREMENT\] The organization SHALL verify access to the CRA Single Reporting Platform (SRP) and complete at least one test submission prior to 11 Sep 2026\. Note: The SRP may not yet be fully operational; organizations SHOULD contact their national CSIRT or MSA for current submission guidance and interim procedures. | ☐ Yes   ☐ No   ☐ Partial |   | SRP account registration confirmation or national CSIRT contact record; test submission record or interim procedure documentation. |
| **4.5.5** | \[CRA REQUIREMENT\] The organization SHALL maintain a documented procedure recording when awareness of an incident or actively exploited vulnerability first occurred, to establish the Art. 14 reporting clock start time. | ☐ Yes   ☐ No   ☐ Partial |   | Incident log with awareness timestamp; governance documentation. |
| **4.5.6** | \[CRA REQUIREMENT\] The Art. 14 RACI SHALL be reviewed and re-confirmed upon any relevant personnel change and at minimum annually. | ☐ Yes   ☐ No   ☐ Partial |   | RACI version history; review record. |

 

 

# **Section 5: Open Source Software (OSS) Stewardship**

CRA Recital 18 and Article 17 create a distinct compliance category for Open Source Software Stewards \- entities that provide OSS for integration into products placed on the EU market. This section governs how the organization engages with upstream communities and clarifies internal steward vs. maintainer boundaries.

 

## **5.1 Open Source Contribution & Engagement**

Policy for engaging with upstream open-source communities while maintaining CRA compliance, including responsible disclosure and community participation.

 

| Ref | Requirement | Conformant? (Yes / No / Partial) | Evidence & Rationale | Guidance / Reference |
| :---- | :---- | :---- | :---- | :---- |
| **5.1.1** | \[GOOD PRACTICE\] The organization SHOULD maintain a documented policy governing how personnel contribute to upstream open-source projects, including CLA/DCO requirements and IP assignment rules. | ☐ Yes   ☐ No   ☐ Partial |   | OSS contribution policy; CLA tool configuration. OpenChain ISO/IEC 5230 as reference. |
| **5.1.2** | \[CRA REQUIREMENT (Manufacturer)\]/\[GOOD PRACTICE (Steward)\] Security vulnerabilities discovered during product work SHALL be responsibly disclosed to upstream maintainers before public disclosure (CRA Art. 13 manufacturer responsibility for third-party components). | ☐ Yes   ☐ No   ☐ Partial |   | Upstream disclosure procedure; example disclosure record. |
| **5.1.3** | \[GOOD PRACTICE\] The organization SHOULD engage with relevant security working groups (e.g., OpenSSF, CISA, CycloneDX community) to improve OSS supply chain security. Note: This is a recommended good practice and is not a published CRA legal requirement. | ☐ Yes   ☐ No   ☐ Partial |   | Membership records; meeting participation log; issue/PR contributions. |
| **5.1.4** | \[GOOD PRACTICE\] OSS dependencies SHOULD be assessed for community health (maintenance status, contributor diversity, EOL date) before adoption. Components whose EOL falls within the product support lifetime SHOULD be avoided or formally risk-accepted. | ☐ Yes   ☐ No   ☐ Partial |   | Dependency health assessment checklist; tooling (e.g., OpenSSF Scorecard: [securityscorecards.dev](https://securityscorecards.dev)). |
| **5.1.5** | \[CRA REQUIREMENT\] For any OSS project where the manufacturer vs. steward classification is non-obvious, the organization SHALL apply a formal commercial-activity test using criteria from Commission guidance C(2026) 5252: (a) charging a fee for the software; (b) charging for technical support exceeding cost recovery; (c) intending to monetize through a platform; (d) collecting personal data beyond security/compatibility purposes; (e) accepting donations exceeding operational costs. If any criterion is met, manufacturer obligations apply. | ☐ Yes   ☐ No   ☐ Partial |   | Commercial-activity test worksheet per project; legal sign-off on borderline cases; reference to Commission guidance C(2026) 5252\. |
| **5.1.6** | \[CRA REQUIREMENT (Manufacturer)\] The organization SHALL maintain a documented approach for upstream OSS components whose maintainers are not directly CRA-obligated, including a process for requesting SBOM artifacts, CVD policy documentation, and patch timelines from upstream projects, and for assessing integration risk for components lacking these. | ☐ Yes   ☐ No   ☐ Partial |   | Upstream due-diligence checklist; criteria for accepting or rejecting components; reference to CRA Art. 13 manufacturer responsibility. |
| **5.1.7** | \[GOOD PRACTICE\] A dependency approval gate SHOULD exist requiring security review of new dependencies before they are introduced into supported products. | ☐ Yes   ☐ No   ☐ Partial |   | Dependency approval procedure; approval workflow; example approved and rejected dependency records. |

 

## **5.2 Steward vs. Maintainer Boundaries**

Guidelines clarifying the distinct obligations of OSS Stewards \- entities that provide OSS for integration into products placed on the EU market (CRA Art. 3(14)) \- versus individual project maintainers, and how the organization determines which role applies.

 

| Ref | Requirement | Conformant? (Yes / No / Partial) | Evidence & Rationale | Guidance / Reference |
| :---- | :---- | :---- | :---- | :---- |
| **5.2.1** | \[CRA REQUIREMENT\] The organization SHALL document whether it meets the definition of an OSS Steward under CRA Art. 3(14) and record this determination with supporting rationale. | ☐ Yes   ☐ No   ☐ Partial |   | Legal determination memo; CRA Art. 3(14) criteria checklist. |
| **5.2.2** | \[CRA REQUIREMENT\] For projects where the organization acts as Steward, a lightweight security policy SHALL be published meeting CRA Annex II steward requirements. | ☐ Yes   ☐ No   ☐ Partial |   | SECURITY.md or equivalent policy for each steward project. |
| **5.2.3** | \[GOOD PRACTICE\] Internal maintainers SHOULD understand their distinct obligations vs. the organization's steward-level obligations and SHOULD receive appropriate guidance. | ☐ Yes   ☐ No   ☐ Partial |   | Training or guidance document; maintainer role definition. |
| **5.2.4** | \[GOOD PRACTICE\] A registry of projects where the organization acts as Steward (vs. Manufacturer) SHOULD be maintained and reviewed annually. | ☐ Yes   ☐ No   ☐ Partial |   | Steward registry document; review record. |

 

 

# **Section 6: Security Updates & Support Period**

CRA Article 13(2) requires manufacturers to formally document the expected support period for each product with digital elements and to provide security updates throughout that period. This section ensures the organization can define, publish, and operationalize product support lifecycles.

 

## **6.1 Support Period Definition & Update Obligations**

Processes for defining support periods, delivering security updates, and communicating product lifecycle status to customers and downstream integrators (CRA Art. 13(2)).

 

| Ref | Requirement | Conformant? (Yes / No / Partial) | Evidence & Rationale | Guidance / Reference |
| :---- | :---- | :---- | :---- | :---- |
| **6.1.1** | \[CRA REQUIREMENT\] The organization SHALL define and publish the expected support period for each product with digital elements placed on the EU market. The support period SHALL be at least five years unless the expected product lifetime is shorter. A rolling-release model is also a valid approach, provided the end of support is clearly communicated and security updates are provided throughout (CRA Art. 13(2)). | ☐ Yes   ☐ No   ☐ Partial |   | Product lifecycle documentation; public-facing support statement; legal justification if period is less than 5 years; rolling-release policy if applicable. |
| **6.1.2** | \[CRA REQUIREMENT\] Security updates addressing vulnerabilities SHALL be provided free of charge throughout the declared support period (CRA Art. 13(9)). | ☐ Yes   ☐ No   ☐ Partial |   | Patch management policy; release history showing security updates issued within support window. |
| **6.1.3** | \[CRA REQUIREMENT\] The organization SHALL document, implement, and test a secure software update mechanism including integrity verification of update packages, protection against rollback attacks, and automatic delivery by default where technically feasible with user opt-out capability. | ☐ Yes   ☐ No   ☐ Partial |   | Update architecture document; signing key management; rollback-prevention test records; automatic update configuration. |
| **6.1.4** | \[CRA REQUIREMENT\] End-of-support dates and associated security implications SHALL be communicated to customers and downstream integrators. Where feasible, at least 12 months advance notice SHOULD be given before the final security update (CRA Art. 13(8)). | ☐ Yes   ☐ No   ☐ Partial |   | Customer communication records; EoL announcement template; advance notice evidence. |
| **6.1.5** | \[GOOD PRACTICE\] Where a product reaches end-of-support during an active vulnerability's remediation window, the organization SHOULD maintain a documented escalation procedure to manage customer risk. | ☐ Yes   ☐ No   ☐ Partial |   | EoL vulnerability handling procedure; customer advisory template. |
| **6.1.6** | \[GOOD PRACTICE\] An end-of-support transition procedure SHOULD exist to guide customers through migration, including identification of supported alternatives and a timeline for ending security update delivery. | ☐ Yes   ☐ No   ☐ Partial |   | EoL transition guide; customer migration documentation; timeline for final security update. |
| **6.1.7** | \[GOOD PRACTICE\] At end-of-life, the organization SHOULD provide or document a procedure for secure deletion of user data held by the product and for secure data transfer to alternative solutions. | ☐ Yes   ☐ No   ☐ Partial |   | Data sanitization procedure; secure deletion test records; data portability documentation. |

 

 

# **Section 7: Technical File & Supply Chain Sharing**

CRA Articles 13(15) and 28 require manufacturers to prepare technical documentation and make it available to market surveillance authorities (MSAs) on request. Article 13(19) requires SBOMs to accompany products. This section ensures the organization can fulfill these obligations reliably.

 

## **7.1 Market Surveillance Deliverables**

Procedures for compiling and producing technical documentation and SBOMs upon request by market surveillance authorities under CRA Art. 13(15) and Annex VII.

 

| Ref | Requirement | Conformant? (Yes / No / Partial) | Evidence & Rationale | Guidance / Reference |
| :---- | :---- | :---- | :---- | :---- |
| **7.1.1** | \[CRA REQUIREMENT\] The organization SHALL maintain a Technical File for each in-scope product containing all elements required by CRA Annex VII: product description, design documents, cybersecurity risk assessment, SDL evidence, security test results, SBOM, connections audit, EU Declaration of Conformity, and EOL declaration. | ☐ Yes   ☐ No   ☐ Partial |   | Technical File index; storage location; access control. CRA Annex VII checklist. |
| **7.1.2** | \[CRA REQUIREMENT\] The organization SHALL perform and maintain a documented cybersecurity risk assessment including threat modelling (attack surface, threat actors, attack vectors) with a documented methodology. The assessment SHALL be performed before development begins and updated throughout the product lifecycle. | ☐ Yes   ☐ No   ☐ Partial |   | Risk assessment report; threat model document; update history reviewed at each major release. |
| **7.1.3** | \[CRA REQUIREMENT\] The Technical File SHALL be accessible to designated personnel and SHALL be capable of being produced to a market surveillance authority (MSA) within the legally required timeframe. | ☐ Yes   ☐ No   ☐ Partial |   | File retrieval SLA; named custodian. |
| **7.1.4** | \[CRA REQUIREMENT\] SBOMs included in the Technical File SHALL be the same machine-readable artifacts generated by the CI/CD pipeline (no manual transcription). | ☐ Yes   ☐ No   ☐ Partial |   | Pipeline artifact link to Technical File storage. |
| **7.1.5** | \[CRA REQUIREMENT\] Technical documentation SHALL be retained for at least 10 years after placement on the market, or for the expected product lifetime or support period if longer (CRA Art. 13(15) and Art. 31(3)). | ☐ Yes   ☐ No   ☐ Partial |   | Retention policy; archive location; destruction schedule. |
| **7.1.6** | \[GOOD PRACTICE\] The organization SHOULD maintain a documented MSA response workflow defining how a Technical File request from a market surveillance authority is received, processed, and fulfilled within the legally required timeframe. | ☐ Yes   ☐ No   ☐ Partial |   | MSA response SOP; named responsible contact; estimated fulfillment timeline. |

 

## **7.2 Downstream & Customer Provisioning**

Delivering accurate, timely security and SBOM documentation to customers and integrators alongside binary or source delivery.

 

| Ref | Requirement | Conformant? (Yes / No / Partial) | Evidence & Rationale | Guidance / Reference |
| :---- | :---- | :---- | :---- | :---- |
| **7.2.1** | \[CRA REQUIREMENT\] The SBOM SHALL be made available to market surveillance authorities upon reasoned request as part of the Technical File (CRA Annex VII). \[GOOD PRACTICE\] Making the SBOM available to customers and integrators alongside each product release is strongly recommended but is not a CRA legal obligation enforceable against the manufacturer. | ☐ Yes   ☐ No   ☐ Partial |   | SBOM delivery mechanism (portal, API, package metadata, attestation) where voluntarily provided; MSA Technical File access procedure. |
| **7.2.2** | \[GOOD PRACTICE\] Security advisories and vulnerability exploitability statements SHOULD be delivered to downstream integrators through a documented channel. | ☐ Yes   ☐ No   ☐ Partial |   | Advisory distribution list; portal URL; API endpoint. |
| **7.2.3** | \[GOOD PRACTICE\] Contractual or technical mechanisms SHOULD be used to ensure downstream integrators receive timely security updates for embedded components. | ☐ Yes   ☐ No   ☐ Partial |   | Contract clause or SLA; notification mechanism. |
| **7.2.4** | \[GOOD PRACTICE\] A process MAY exist to handle customer requests for additional SBOM detail or vulnerability information. Note: This is a good practice and is not a CRA legal obligation. | ☐ Yes   ☐ No   ☐ Partial |   | Customer-facing SBOM request procedure; support ticket template. |
| **7.2.5** | \[GOOD PRACTICE\] Where the product transmits telemetry, the organization SHOULD document and validate that telemetry data collection is limited to what is necessary and that outbound connections are audited. | ☐ Yes   ☐ No   ☐ Partial |   | Telemetry data inventory; outbound connections audit log; data minimisation policy. |

 

## **7.3 EU Declaration of Conformity & CE Marking (CRA Art. 28 & 30\)**

To legally place products on the EU market under CRA, manufacturers must draft an EU DoC aligned with Annex V and affix the CE marking. For software-only products distributed digitally, a digital CE marking accessible on the product website satisfies the affixing requirement.

 

| Ref | Requirement | Conformant? (Yes / No / Partial) | Evidence & Rationale | Guidance / Reference |
| :---- | :---- | :---- | :---- | :---- |
| **7.3.1** | \[CRA REQUIREMENT\] The organization SHALL draft an EU Declaration of Conformity (DoC) for each in-scope product in accordance with CRA Annex V, referencing the specific essential requirements met and the conformity assessment procedure used. | ☐ Yes   ☐ No   ☐ Partial |   | EU DoC template completed per Annex V; legal review sign-off. |
| **7.3.2** | \[CRA REQUIREMENT\] The EU DoC SHALL be kept up-to-date and SHALL be updated upon any significant product change affecting the conformity assessment basis. | ☐ Yes   ☐ No   ☐ Partial |   | DoC version history; update procedure documentation. |
| **7.3.3** | \[CRA REQUIREMENT\] The CE marking (or, for software-only products distributed digitally, a digital CE marking accessible on the product website) SHALL be affixed before EU market placement (CRA Art. 30). | ☐ Yes   ☐ No   ☐ Partial |   | CE mark placement evidence (screenshot, label photograph, or packaging proof); digital CE mark URL. |
| **7.3.4** | \[CRA REQUIREMENT\] The EU DoC SHALL be made available to market surveillance authorities and SHALL be retained for at least 10 years after last placement on the EU market. | ☐ Yes   ☐ No   ☐ Partial |   | DoC storage location; access control; retention policy entry. |

 

## **7.4 EU Authorized Representative (CRA Art. 22 / 25\)**

If a manufacturer is not established in the EU, it must ensure that one of the following is in place before placing any product on the EU market: (a) an appointed EU Authorized Representative (AR) under CRA Art. 22/25; (b) an EU-based importer who places the product on the market; or (c) an EU-based fulfillment service provider acting under a written mandate. An Authorized Representative is not the only option \- but one of these three must be in place. Items 7.4.2-7.4.5 apply only where the AR route is chosen; mark N/A with documented rationale if using the importer or fulfillment provider route instead.

 

| Ref | Requirement | Conformant? (Yes / No / Partial) | Evidence & Rationale | Guidance / Reference |
| :---- | :---- | :---- | :---- | :---- |
| **7.4.1** | \[CRA REQUIREMENT\] The organization SHALL determine whether it has an EU establishment as a manufacturer under CRA Art. 3(13). If not EU-established, one of the following SHALL be in place before any product is placed on the EU market: (a) an EU Authorized Representative (AR) under CRA Art. 22/25; (b) an EU-based importer who places the product on the market; or (c) an EU-based fulfillment service provider acting under a written mandate. | ☐ Yes   ☐ No   ☐ Partial |   | Legal determination memo; EU establishment confirmation or, where applicable, AR mandate, importer agreement, or fulfillment provider contract. |
| **7.4.2** | \[CRA REQUIREMENT\] Where the AR pathway is chosen, a written mandate SHALL be executed before placing any product on the EU market. The mandate SHALL specify at minimum the obligations defined in CRA Art. 18(3): (a) keeping the EU DoC and Technical File available to MSAs for at least 10 years or the support period whichever is longer; (b) providing MSAs with information and documentation necessary to demonstrate conformity upon reasoned request; (c) cooperating with MSAs on any action taken to eliminate risks posed by the product. | ☐ Yes   ☐ No   ☐ Partial |   | Signed AR mandate; mandate text confirming Art. 18(3)(a-c) obligations; AR's EU address and contact details. |
| **7.4.3** | \[CRA REQUIREMENT\] Where the AR pathway is chosen, the AR's name, address, and contact details SHALL be included on the product, its packaging, or accompanying documentation (CRA Art. 25). | ☐ Yes   ☐ No   ☐ Partial |   | Product label or documentation showing AR details. |
| **7.4.4** | \[CRA REQUIREMENT\] Where the AR pathway is chosen, the AR SHALL be provided with a copy of the EU DoC and Technical File and SHALL be empowered to act on behalf of the manufacturer in dealings with market surveillance authorities. | ☐ Yes   ☐ No   ☐ Partial |   | Document transmission record; access confirmation from AR. |
| **7.4.5** | \[GOOD PRACTICE\] Where the AR pathway is chosen, the organization SHOULD maintain documented operational procedures governing how the AR fulfills the Art. 18(3) obligations in practice, including escalation paths and communication protocols with MSAs. | ☐ Yes   ☐ No   ☐ Partial |   | AR operational procedure document; communication protocol; escalation path. |

 

 

# **Section 8: Cross-Framework Integration**

The CRA sits within a broader EU digital regulatory stack. Organizations treating CRA compliance as a standalone exercise will duplicate work across NIS2, the AI Act, DORA, and the Data Act. This section ensures the organization identifies where CRA conformity artifacts serve multiple regulatory obligations simultaneously.

 

## **8.1 CRA and NIS2**

 

| Ref | Requirement | Conformant? (Yes / No / Partial) | Evidence & Rationale | Guidance / Reference |
| :---- | :---- | :---- | :---- | :---- |
| **8.1.1** | \[GOOD PRACTICE\] The organization SHOULD determine whether it is subject to NIS2 (Directive (EU) 2022/2555) as an essential or important entity independently of its CRA manufacturer obligations. Where both apply, a mapping SHOULD exist showing how CRA product security artifacts satisfy NIS2 supply chain security assessment requirements (NIS2 Art. 21(2)(d)). | ☐ Yes   ☐ No   ☐ Partial |   | Dual-framework mapping document; NIS2 supply chain security procedure referencing CRA conformity artifacts. |
| **8.1.2** | \[GOOD PRACTICE\] For organizations subject to both NIS2 and CRA, governance, risk assessment, and incident response processes SHOULD be designed to serve both frameworks on shared rather than parallel tracks where the underlying obligation is equivalent. | ☐ Yes   ☐ No   ☐ Partial |   | Integrated GRC framework document; evidence that NIS2 incident reporting and CRA Art. 14 notification runbooks share escalation paths and RACI roles. |

 

## **8.2 CRA and AI Act**

 

| Ref | Requirement | Conformant? (Yes / No / Partial) | Evidence & Rationale | Guidance / Reference |
| :---- | :---- | :---- | :---- | :---- |
| **8.2.1** | \[GOOD PRACTICE\] For any product that is both a PDE under CRA and a high-risk AI system under the AI Act (Regulation (EU) 2024/1689), the organization SHOULD document that CRA Annex I compliance satisfies the AI Act Art. 15 cybersecurity requirements for that product, per CRA Art. 12\. | ☐ Yes   ☐ No   ☐ Partial |   | AI Act / CRA dual-scope determination per product; mapping from CRA Annex I to AI Act Art. 15\. |
| **8.2.2** | \[GOOD PRACTICE\] For Important or Critical CRA products that are also high-risk AI systems, the organization SHOULD document that CRA conformity assessment requirements take precedence over AI Act internal control provisions for cybersecurity aspects (per CRA Art. 12). This precedence SHOULD be recorded in the product conformity assessment plan. | ☐ Yes   ☐ No   ☐ Partial |   | Precedence determination in conformity assessment plan; legal review sign-off. |

 

## **8.3 CRA and DORA**

 

| Ref | Requirement | Conformant? (Yes / No / Partial) | Evidence & Rationale | Guidance / Reference |
| :---- | :---- | :---- | :---- | :---- |
| **8.3.1** | \[GOOD PRACTICE\] For organizations supplying digital products to financial entities subject to DORA (Regulation (EU) 2022/2554), CRA conformity documentation (Technical File, DoC, SBOM, vulnerability handling SLAs) SHOULD be identified as relevant input to DORA ICT third-party risk management due diligence and SHOULD be made available to financial entity customers on request. | ☐ Yes   ☐ No   ☐ Partial |   | Customer-facing documentation list including DORA-relevant CRA artifacts; reference to DORA Art. 28-30. |

 

## **8.4 CRA and Data Act**

 

| Ref | Requirement | Conformant? (Yes / No / Partial) | Evidence & Rationale | Guidance / Reference |
| :---- | :---- | :---- | :---- | :---- |
| **8.4.1** | \[GOOD PRACTICE\] For connected products that simultaneously qualify under the Data Act (Regulation (EU) 2023/2854), overlapping obligations around data access, documentation, and user transparency SHOULD be identified, and the compliance program SHOULD address both regulations in a coordinated manner. | ☐ Yes   ☐ No   ☐ Partial |   | Data Act / CRA product scope overlap assessment; coordinated documentation plan. |

 

## **8.5 CRA and eIDAS**

eIDAS 2.0 (Regulation (EU) 2024/1183) governs electronic identification and trust services. Where CRA products interact with eIDAS-governed identity services or where an Authorized Representative operates under eIDAS-regulated digital identity, the interaction between the two frameworks should be assessed. Note: the character of Authorized Representatives may change under eIDAS hybridization; legal counsel should be consulted for products at this intersection.

 

| Ref | Requirement | Conformant? (Yes / No / Partial) | Evidence & Rationale | Guidance / Reference |
| :---- | :---- | :---- | :---- | :---- |
| **8.5.1** | \[GOOD PRACTICE\] For products that interact with eIDAS-governed electronic identification or trust services, the organization SHOULD assess whether eIDAS 2.0 (Regulation (EU) 2024/1183) creates obligations in addition to CRA, particularly where the product functions as a relying party or issues electronic attestations. | ☐ Yes ☐ No ☐ Partial |   | Legal determination memo; eIDAS / CRA dual-scope assessment; reference to Regulation (EU) 2024/1183. |
| **8.5.2** | \[GOOD PRACTICE\] Where the organization appoints an EU Authorized Representative and that AR operates using eIDAS-regulated digital identity services, the organization SHOULD document how the eIDAS and CRA AR obligations interact, and SHOULD seek legal counsel given the evolving hybridization of these frameworks. | ☐ Yes ☐ No ☐ Partial |   | Legal counsel assessment; AR mandate review against eIDAS identity obligations; reference to CRA Art. 18 and eIDAS 2.0 Art. 45\. |

 

 

# **Section 9: Procurement & Buyer-Side Obligations**

The CRA does not create direct compliance obligations for enterprise buyers, but it changes what responsible procurement looks like. For organizations also subject to NIS2 as essential or important entities, these questions are simultaneously regulatory requirements.

 

## **9.1 Vendor CRA Qualification**

 

| Ref | Requirement | Conformant? (Yes / No / Partial) | Evidence & Rationale | Guidance / Reference |
| :---- | :---- | :---- | :---- | :---- |
| **9.1.1** | \[GOOD PRACTICE\] The vendor evaluation process SHOULD require suppliers of products with digital elements to confirm: (a) the CRA product classification; (b) the conformity pathway used; (c) the declared support period end date. Note: The notified body used is published on the EU DoC and need not be separately collected. | ☐ Yes   ☐ No   ☐ Partial |   | Updated vendor questionnaire or RFP template; example completed vendor response. |
| **9.1.2** | \[GOOD PRACTICE\] Procurement contracts for products with digital elements SHOULD include at minimum: (a) CRA conformity confirmation; (b) commitment to maintain vulnerability handling for the declared support period; (c) notification obligation to the buyer upon discovery of an actively exploited vulnerability in a supplied product. Note: Contractual access to Technical File or DoC is a good practice and not a CRA statutory obligation. | ☐ Yes   ☐ No   ☐ Partial |   | Updated standard contract template with CRA clauses; legal review sign-off. |
| **9.1.3** | \[GOOD PRACTICE\] The organization SHOULD ask suppliers whether they produce SBOMs for procured products, in what format, and whether they are available. For high-assurance procurement, SBOM availability SHOULD be a mandatory procurement criterion. | ☐ Yes   ☐ No   ☐ Partial |   | Supplier SBOM availability requirement in procurement policy; evidence of SBOM receipt or supplier declaration. |
| **9.1.4** | \[GOOD PRACTICE\] The organization SHOULD verify that suppliers have credible processes to detect and report actively exploited vulnerabilities in shipped components in a timely manner consistent with CRA Art. 14 obligations. | ☐ Yes   ☐ No   ☐ Partial |   | Supplier due-diligence question on vulnerability monitoring capability; documented assessment outcome per supplier. |
| **9.1.5** | \[GOOD PRACTICE\] The organization SHOULD implement a supplier risk tiering model classifying vendors by the criticality of the components they supply, the security maturity of their CRA compliance program, and their vulnerability response track record. | ☐ Yes   ☐ No   ☐ Partial |   | Supplier risk tier matrix; tiering criteria document; example tier assignment records. |

 

 

# **Implementation Roadmap**

The following phased model provides a structured approach to achieving self-certification. Organizations should scope Phase 1 narrowly (e.g., one product line) and expand incrementally.

 

| Phase | Key Action | Typical Owner | Target |
| :---- | :---- | :---- | :---- |
| **PRIORITY \- Art. 14 RACI (§4.4-4.5)** | Register EUVDB account; assign named owners for 24h / 72h / 14-day notification stages; document "severe security incident" definition; complete at least one test submission through the ENISA reporting platform before the deadline. |   | **Before 11 Sep 2026 \- IMMEDIATE** |
| **1 \- Scope & Categorization** | Determine organizational role (Manufacturer / Importer / Distributor / Steward) using §1 applicability table; define product scope; confirm PDE vs SaaS (§2.5.1); complete EU establishment determination (§2.5.2 / §7.4); complete risk classification (§2.5.3-2.5.8); confirm self-cert eligibility or engage Notified Body. | Legal \+ CISO | Month 1-2 |
| **2 \- Policy & Governance** | Draft and approve CRA policy (§2.1); assign all roles (§2.2); complete training (§2.3); set up exception management (§2.4.6-2.4.8); establish M/606 / PT1 / PT3 standards monitoring (§2.6). | Legal \+ CISO | Month 1-3 |
| **3 \- SBOM & SDLC** | Instrument CI/CD for SBOM; validate completeness (§3.1-3.2); document SBOM depth decision tied to 24h window (§3.1.5); establish provenance signing and secure build infrastructure (§3.3); implement SAST/DAST gates, threat modeling, release gate, secure coding standard (§3.4); complete importer/distributor checklist (§3.5). | Platform Eng. | Month 2-4 |
| **4 \- Vuln Pipeline** | Deploy continuous monitoring including EUVDB and KEV feeds (§4.1.1-4.1.7); define Patch SLA Matrix (§4.1.4); configure KEV as Art. 14 trigger; define triage SLAs (§4.2-4.3); publish CVD policy (§4.4); set up vulnerability metrics KPIs (§4.1.8). | SecOps | Month 3-5 |
| **5 \- VEX & Disclosure** | Implement VEX workflow (§4.2); integrate ENISA Art. 14 reporting runbook including CSIRT routing, SME fine-exemption scope, and CSIRT dissemination delay awareness (§4.4); train responders; run tabletop exercise (§4.5.6). | SecOps \+ Legal | Month 4-6 |
| **6 \- OSS Governance** | Complete Steward vs. manufacturer determination including commercial-activity test (§5.1.6); establish dependency approval gate (§5.1.5); publish SECURITY.md for stewarded projects (§5.2); establish upstream due-diligence procedure (§5.1.7). | OSS Program | Month 5-7 |
| **7 \- Support Period** | Define and publish support periods; document secure update mechanism; establish EoL transition procedure including data sanitization (§6.1.6-6.1.7). | Product \+ Legal | Month 5-7 |
| **8 \- Technical File & CE** | Compile Technical Files; establish MSA response workflow (§7.1.6); draft EU DoC per Annex V; affix CE marking; confirm AR / importer / fulfillment provider arrangement if non-EU (§7.4); implement downstream provisioning and telemetry validation (§7.2.5). | Compliance PM | Month 6-8 |
| **8A \- Cross-Framework** | Complete §8 cross-framework mapping: NIS2 (§8.1); AI Act Art. 15 / CRA Art. 12 (§8.2); DORA ICT third-party risk (§8.3); Data Act overlap (§8.4). | Legal \+ CISO | Month 7-9 |
| **8B \- Procurement** | Complete §9 vendor CRA qualification: update vendor questionnaire (§9.1.1); update procurement contracts (§9.1.2); add SBOM criterion (§9.1.3); Sept 2026 monitoring capability check (§9.1.4); implement supplier risk tiering (§9.1.5). | Legal \+ Procurement | Month 7-9 |
| **9 \- Self-Certification** | Complete this checklist; remediate gaps; conduct internal audit (§2.4.5); resolve or register all exceptions (§2.4.6-2.4.8); file conformance claim. Total checklist items: 156\. | CRA Program Mgr | Month 8-10 |
| **10 \- Continuous Ops** | Annual review cycle (§2.4); training refresh; SBOM quality tracking; advisory cadence; annual tabletop exercise; PT1/PT3 standards monitoring update. | All owners | Ongoing |

 

 

# **Self-Certification Summary**

**Legal notice:** Completion of this checklist does not by itself establish legal conformity under Regulation (EU) 2024/2847. Self-certification (Module A) is only valid for Default and eligible Important Class I products. A conformity claim requires: (a) completion of all applicable checklist items with supporting evidence; (b) issuance of an EU Declaration of Conformity per Annex V; (c) proper CE marking per Art. 30\. Organizations are advised to seek qualified legal counsel before making a formal conformity claim.

 

Upon completing all checklist items, complete the attestation below. This document may be retained as internal evidence of CRA readiness. Third-party certification is available through OpenChain certification partners.

 

| Organization | \[INSERT: Full legal entity name of manufacturer\] |
| :---- | :---- |
| **Organizational Role(s)** | \[INSERT: Manufacturer / Importer / Distributor / OSS Steward \- circle all that apply\] |
| **Product / Scope** | \[INSERT: Product name(s) and version(s) in scope\] |
| **Self-Certification Date** | \[Date\] |
| **CRA Program Manager** | \[INSERT: Name, Title \- Signature required for formal submission\] |
| **Next Review Date** | \[Date \- max 12 months from above\] |
| **Items answered Yes** | \[  \] of 156 total checklist items |
| **Items answered No/Partial** | \[  \] \- gap remediation plan attached: Yes / No |

 

 

# **Appendix B \- Definitions / Glossary**

The following terms are used throughout this document. Definitions align with CRA Regulation (EU) 2024/2847 and referenced standards unless otherwise noted.

 

| Term | Definition |
| :---- | :---- |
| **AR (Authorized Representative)** | An EU-established natural or legal person appointed by a non-EU manufacturer to act on its behalf for CRA obligations, including Technical File custody and MSA engagement (CRA Art. 22/25). Note: AR appointment is one of three options for non-EU manufacturers; the others are an EU importer or EU fulfillment service provider. |
| **CRA** | Cyber Resilience Act \- Regulation (EU) 2024/2847 establishing mandatory cybersecurity requirements for products with digital elements placed on the EU market. |
| **CSIRT** | Computer Security Incident Response Team \- a designated national authority responsible for receiving and processing CRA Article 14 vulnerability and incident notifications within EU member states. |
| **DoC (Declaration of Conformity)** | EU Declaration of Conformity \- a formal manufacturer declaration that a product meets all applicable CRA essential requirements, drafted per CRA Annex V and required before CE marking and EU market placement. |
| **EPSS** | Exploit Prediction Scoring System \- a probability score (0-1) estimating the likelihood that a CVE will be exploited in the wild within 30 days, used alongside CVSS to prioritize vulnerability remediation. |
| **KEV** | Known Exploited Vulnerabilities \- the CISA catalog of CVEs confirmed to have been actively exploited, used as a trigger for CRA Art. 14 Early Warning assessment in this document. |
| **MSA (Market Surveillance Authority)** | A national authority responsible for enforcing CRA compliance, with powers to request Technical Files, conduct audits, and impose corrective measures or market withdrawal (CRA Art. 58+). |
| **OSS Steward** | An entity that provides open-source software intended for integration into products with digital elements placed on the EU market, without qualifying as a manufacturer under the commercial-activity test (CRA Art. 3(14), Recital 18). Subject to lighter obligations under CRA Annex II. |
| **PDE (Product with Digital Elements)** | Any software or hardware product and its remote data processing solutions whose intended or reasonably foreseeable use includes a direct or indirect logical or physical data connection to a device or network (CRA Art. 3(1)). |
| **SBOM (Software Bill of Materials)** | A formal, machine-readable inventory of software components and dependencies in a product, including component names, versions, suppliers, and unique identifiers. Required under CRA Annex I Part II and Art. 13(19). |
| **VEX (Vulnerability Exploitability eXchange)** | A machine-readable document that communicates the exploitability status of known vulnerabilities in the context of a specific product, using status values: not\_affected, affected, fixed, under\_investigation. Supported formats: CycloneDX VEX, OpenVEX. |

 

 

# **Appendix A \- CRA Annex I Traceability Matrix**

This matrix maps each CRA Annex I essential requirement to the corresponding control(s) in this document, the evidence expected, and the document location. Use this appendix during conformity assessment to demonstrate that every Annex I obligation is addressed.

 

| CRA Annex I Requirement | Part | Control (Section Ref) | Evidence Expected | Location |
| :---- | :---- | :---- | :---- | :---- |
| No known exploitable vulnerabilities at time of placing on market | Part I, §1 | 3.4.5, 3.4.6, 3.4.7 | SAST/DAST results; pentest report; vulnerability register showing zero unresolved critical findings at release | §3.4 |
| Secure by default configuration | Part I, §2 | 3.4.1, 3.4.2 | Secure defaults checklist; no default credentials policy; attack surface map | §3.4 |
| Protection against unauthorized access | Part I, §3 | 3.4.1, 3.4.3 | Authentication policy; TLS configuration audit; access control documentation | §3.4 |
| Protection of confidentiality and integrity of data | Part I, §4 | 3.4.3 | Encryption policy; data classification map; TLS 1.2+ configuration evidence | §3.4 |
| Availability protection and resilience | Part I, §5 | 3.4.2, 4.3 | Attack surface minimization evidence; incident response plan; availability SLA | §3.4, §4.3 |
| Minimization of attack surface | Part I, §6 | 3.4.2 | Port/service inventory; hardening guide; network exposure map | §3.4 |
| Reduction of incident impact | Part I, §7 | 4.3, 4.4 | Escalation matrix; incident response runbook; Art. 14 RACI | §4.3, §4.4 |
| Security update mechanism | Part I, §8 | 6.1.2, 6.1.3 | Update architecture; signing key management; rollback-prevention test records | §6.1 |
| Vulnerability disclosure policy | Part II, §1 | 4.4.7 | CVD policy URL; security.txt; SECURITY.md; PGP key | §4.4 |
| Handling of known vulnerabilities | Part II, §2 | 4.1, 4.2, 4.3 | Vulnerability monitoring configuration; VEX process; triage SLA; patch SLA matrix | §4.1-4.3 |
| Regular security updates | Part II, §3 | 6.1.2 | Patch release history; update delivery mechanism | §6.1 |
| Coordinated vulnerability disclosure | Part II, §4 | 4.4.7, 4.4.8 | CVD policy; advisory publication records; researcher acknowledgements | §4.4 |
| Mandatory regulatory notification (Art. 14\) | Part II, §5 | 4.4.2-4.4.6, 4.5 | EUVDB submission runbook; RACI; test submission record; tabletop exercise record | §4.4, §4.5 |
| SBOM documentation | Part II, §6 | 3.1, 3.2 | Machine-readable SBOM per release; SBOM validation gate; NTIA field coverage | §3.1, §3.2 |
| Secure development lifecycle | Part I (general) | 3.3, 3.4 | Build provenance; secrets management; signing; SAST/DAST integration | §3.3-3.4 |
| Risk assessment documented | Annex VII | 7.1.1, 7.1.2 | Risk assessment report; methodology; scoring model; update history | §7.1 |
| Technical file compiled | Annex VII | 7.1 | Technical File index; storage location; MSA retrieval SLA | §7.1 |
| EU Declaration of Conformity | Annex V | 7.3.1-7.3.4 | Completed DoC per Annex V; CE mark evidence; retention record | §7.3 |

 

 

# **Appendix C \- ISO/IEC 18974 & OWASP SAMM Cross-Reference Mapping**

This mapping shows how ISO/IEC 18974 (Open Source Security Assurance) clauses and OWASP SAMM (Software Assurance Maturity Model) practices align with checklist sections. Organizations already operating ISO/IEC 18974-aligned programs can use this to identify which CRA obligations are already met and where gaps remain. PT1/PT3 (CEN/CENELEC harmonized standards under M/606) will be added to this mapping when public drafts become available.

 

| ISO/IEC 18974 Clause | Requirement Summary | CRA Checklist Section(s) | OWASP SAMM Reference |
| :---- | :---- | :---- | :---- |
| **§3.1.1** | Security policy for open source | §2.1 CRA Policy, §5.1 | SAMM: Governance \> Policy & Compliance |
| **§3.1.2** | Competence and awareness | §2.3 Competence & Training | SAMM: Governance \> Education & Guidance |
| **§3.2.1** | SBOM process and tooling | §3.1 SBOM Generation | SAMM: Implementation \> Secure Build |
| **§3.2.2** | SBOM completeness and data quality | §3.2 Data Quality | SAMM: Implementation \> Secure Build |
| **§3.2.3** | SBOM provenance and integrity | §3.3 Provenance & Integrity | SAMM: Implementation \> Secure Build |
| **§3.3.1** | Vulnerability identification process | §4.1 Vulnerability Monitoring | SAMM: Operations \> Vulnerability Management |
| **§3.3.2** | Vulnerability response and remediation | §4.2 VEX, §4.3 Decisions | SAMM: Operations \> Vulnerability Management |
| **§3.3.3** | Coordinated vulnerability disclosure | §4.4.7 CVD Policy | SAMM: Operations \> Vulnerability Management |
| **§3.4.1** | Roles and responsibilities | §2.2 Roles & Responsibilities | SAMM: Governance \> Strategy & Metrics |
| **§3.4.2** | Program review and continuous improvement | §2.4 Sustainability & Review | SAMM: Governance \> Strategy & Metrics |
| **§3.5.1** | Conformance documentation | §7.1 Technical File, §7.3 EU DoC | SAMM: Governance \> Policy & Compliance |
| **PT1 (pending)** | CRA horizontal cybersecurity requirements (harmonized standard \- draft) | §3.4 Secure Dev Properties | To be mapped when PT1 draft is published |
| **PT3 (pending)** | CRA vulnerability handling requirements (harmonized standard \- draft) | §4.1-4.5 Vuln Handling | To be mapped when PT3 draft is published |

 

 

 

# **Annex D \- Organizations Referencing This Checklist**

The following organizations have indicated that they reference or use this checklist in their CRA compliance programs. Listing here does not imply endorsement of any specific product or service, nor does it constitute a formal conformity certification.

 

| Organization | Description | Country |
| :---- | :---- | :---- |
| **Bitsea GmbH** | Open source security and compliance management; CRA compliance consulting and tooling. Active contributor to this checklist. | Germany |
| **Interlynk**  | SBOM lifecycle management and CRA compliance tooling; references this checklist as a resource on their EU Cyber Resilience Act solutions page at interlynk.io.  | United States |

 

To add your organization, contact the working group lead.

 

 

# **References & Implementation Resources**

Informational notice: References marked as "draft" or "pending" (including Commission draft guidance, PT1, PT3, and similar pre-publication materials) are informational only and non-binding until formally adopted or published. This applies to all such references in this document, including those cited in §2.5.1, §2.6, §5.1.6, and Annex C.

 

**Regulatory & Legal**

 

●  EU Cyber Resilience Act (full text) \- [eur-lex.europa.eu/eli/reg/2024/2847/oj/eng](https://eur-lex.europa.eu/eli/reg/2024/2847/oj/eng)

●  ENISA EU Vulnerability Database (EUVDB) \- [euvdb.enisa.europa.eu](https://euvdb.enisa.europa.eu)

●  CRA Compliance Matrix (independent) \- [cyberresilienceact.eu/compliance-matrix.html](https://www.cyberresilienceact.eu/compliance-matrix.html)

●  Delegated Regulation (EU) 2026/881 \- CSIRT dissemination rules under CRA Art. 14

●  NIS2 Directive (EU) 2022/2555 \- [eur-lex.europa.eu/legal-content/EN/TXT/?uri=CELEX:32022L2555](https://eur-lex.europa.eu/legal-content/EN/TXT/?uri=CELEX:32022L2555)

●  EU AI Act \- Regulation (EU) 2024/1689 \- [eur-lex.europa.eu/legal-content/EN/TXT/?uri=CELEX:32024R1689](https://eur-lex.europa.eu/legal-content/EN/TXT/?uri=CELEX:32024R1689)

●  Digital Operational Resilience Act (DORA) \- Regulation (EU) 2022/2554

●  Data Act \- Regulation (EU) 2023/2854

 

**Standards**

 

●  ISO/IEC 18974:2023 \- Open Source Security Assurance Specification (OpenChain)

●  ISO/IEC 5230:2020 \- OpenChain Specification (License Compliance)

●  CEN/CENELEC PT1 \- CRA horizontal cybersecurity requirements (harmonized standard, draft \- monitor via CEN/CENELEC portal)

●  CEN/CENELEC PT3 \- CRA vulnerability handling requirements (harmonized standard, draft \- monitor via CEN/CENELEC portal)

●  M/606 Mandate \- ETSI / CEN / CENELEC harmonized standards for CRA Annex I

 

**SBOM & Tooling**

 

●  SPDX Specification 3.x \- [spdx.github.io/spdx-spec](https://spdx.github.io/spdx-spec)

●  CycloneDX Specification 1.6+ \- [cyclonedx.org/specification](https://cyclonedx.org/specification)

●  NTIA Minimum Elements for an SBOM \- [ntia.gov/sbom](https://www.ntia.gov/report/2021/minimum-elements-software-bill-materials-sbom)

●  CISA VEX Use Case Minimum Viable Guidelines \- [cisa.gov/resources-tools/resources/minimum-requirements-vulnerability-exploitability-exchange-vex](https://www.cisa.gov/resources-tools/resources/minimum-requirements-vulnerability-exploitability-exchange-vex)

●  SLSA Provenance Framework \- [slsa.dev](https://slsa.dev)

●  OpenSSF Scorecard \- [securityscorecards.dev](https://securityscorecards.dev)

●  CISA Known Exploited Vulnerabilities Catalog \- [cisa.gov/known-exploited-vulnerabilities-catalog](https://www.cisa.gov/known-exploited-vulnerabilities-catalog)

 

**Community & Implementation Guidance**

 

●  OpenChain Project \- [openchainproject.org/get-started](https://openchainproject.org/get-started)

●  OpenChain CRA Compliance GitHub \- [github.com/OpenChain-Project/CRA-Compliance](https://github.com/OpenChain-Project/CRA-Compliance)

●  OpenSSF SBOM Everywhere SIG \- [github.com/ossf/sbom-everywhere](https://github.com/ossf/sbom-everywhere)

●  OWASP SAMM (Software Assurance Maturity Model) \- [owaspsamm.org](https://owaspsamm.org)

●  Eclipse ORC (Open Regulatory Compliance) \- [eclipse.org/orc](https://eclipse.org/orc)

●  EC Commission draft guidance (March 2026), §3.2.3 \- commercial activity test criteria

●  Implementing Regulation (EU) 2025/2392 \- product category technical descriptions

