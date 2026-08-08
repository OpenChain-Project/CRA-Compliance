

| OpenChain-Aligned Cyber Resilience Act (CRA) Compliance Requirements & Checklist Self-Certification Document   \-   ISO/IEC 18974 Aligned   \-   EU Regulation 2024/2847 |
| :---- |

   
 

 

| Document Title | CRA Compliance Requirements & Checklist |
| :---- | :---- |
| **Document Type** | Self-Certification / Governance Framework |
| **Current Version** | PA5 |
| **Date** | 5 Aug 2026 |
| **Status** | DRAFT \- Pre-Approval (PA) |
| **Review Cycle** | Annual; additionally triggered by major releases, significant dependency changes, or regulatory guidance updates (see §2.4.2) |
| **Document Owner** | Devashri Datta (Chairman) |
| **Standards Alignment** | ISO/IEC 18974 \- EU CRA (Reg. 2024/2847) \- OpenChain ISO/IEC 5230 |
| **CRA Art. 14 Reporting Deadline** | 11 Sep 2026 \- see §4.4-4.5 for mandatory actions |

   
**Abstract**

**This document defines the organizational compliance framework for the EU Cyber Resilience Act (CRA, Regulation 2024/2847), structured in alignment with the OpenChain Project adoption framework and ISO/IEC 18974\. It serves simultaneously as a policy framework and a self-certification checklist, covering program governance, SBOM quality, vulnerability handling, regulatory reporting (including the CRA Article 14 three-stage cascade), OSS stewardship, and technical file obligations.**

**Completing or signing this checklist does not in itself constitute a CRA conformity assessment, an EU Declaration of Conformity, or evidence of lawful CE marking. This document is a readiness and evidence-management tool supporting the applicable conformity-assessment procedure. This document does not constitute legal advice; consult qualified legal counsel before formal regulatory submission.**

   
 

   
**License:** CC-BY-4.0.  **OpenChain page:** [openchainproject.org/cracompliance](https://openchainproject.org/cracompliance)   **GitHub:** [github.com/OpenChain-Project/CRA-Compliance](https://github.com/OpenChain-Project/CRA-Compliance)

**Community comments:** [Google Doc (open for comments)](https://docs.google.com/document/d/1Wog28BZ9NQhY3tN9Wc2NDml2phBDuvYu9zkXSON5z5o/edit?usp=sharing)

   
**Important:** All bracketed \[INSERT ...\] fields throughout this document must be completed with organization-specific information before any compliance claim or self-certification is made.

 

# **Revision History**

 

| Version / Date | Description | Author |
| :---- | :---- | :---- |
| PA1 / 21 Jul 2026 | 1st draft \- 5-section structure, Art. 14 cascade, RACI | Devashri Datta |
| PA3 / 29 Jul 2026 | Full normative rewrite (must/should/may); all Bitsea and Daniel Thompson-Yvetot corrections; §8.5 eIDAS; Annex D Adopters. Total items: 156\. | Devashri Datta |
| PA4 / 31 Jul 2026 | All Maarten Aertsen, Madalin Neag, Ryan Tao community feedback incorporated; new item 2.5.9 Art. 32(5) FOSS pathway; full contributor table with 11 contributors; 3 adopters in Annex D. Total items: 157\. | Devashri Datta |
| PA5 / 5 Aug 2026 | Norio Kobota (Sony/OpenChain SBOM WG Chair) corrections: §7.3 reverted to Art. 13(18)/Annex II; §3.1.6 license information added to SBOM metadata fields; §3.1.6 CRA Annex I precedence note added; §5.2.2 Art. 24(1) reference added; applicability table §4 corrected for Stewards (Art. 14(1)(3)(8) conditional); §5 intro updated with Art. 3(14), Recitals 18 and 19, Art. 24\. Marcel Scholze (PwC Germany) and Adrian O'Sullivan corrections: §4.5.4 SRP wording updated; §7.2.1 changed to may for customer SBOM delivery. Contributors expanded to 15\. Total items: 157\. | Devashri Datta |
| 1.0 / TBD | Initial approved release |   |

 

# **Contributors**

   
We would like to express our sincere gratitude to the following contributors and organizations, whose efforts and insights have been invaluable to this document.

 

| Name | Email | Company | GitHub ID | Key Contribution |
| :---- | :---- | :---- | :---- | :---- |
| **Devashri Datta (Chairman)** | devashri.datta@gmail.com |   | devashridatta-dotcom | Document author; all versions PA1-PA5 |
| **Daniel Thompson-Yvetot** | \[confirm\] | CrabNebula / Comply.Land | \[confirm\] | ETSI CYBER-EUSR Rapporteur; normative language; AR/Art.18; Art.14 cascade; eIDAS §8.5 |
| **Andreas Kotulla** | \[andreas@bitsea.de \] | Bitsea GmbH | \[GitHub ID \- confirm\] | SBOM format; 72h clock; Art.14(8); BSI TR-03183; SRP; VEX/CSAF |
| **Maarten Aertsen** | \[confirm\] | NLnet Labs | maertsen | Steward applicability; Art.32(5); role-neutral language; §3.5 Art.24; §5.1.6; §7.3 |
| **Madalin Neag** | \[confirm\] | OpenSSF / Linux Foundation Europe | \[confirm\] | PT1/PT3 links; C(2026) 5252; Art.32(5) FOSS; IR 2025/2392; Annex VIII Part 1; §2.6.3 |
| **Norio Kobota** | \[confirm\] | Sony Group Corporation | \[confirm\] | §7.3 Art.13(18) correction; §3.1.6 license fields; §5 legal basis; §4 Steward applicability; Art.24(1) |
| **Marcel Scholze** | \[confirm\] | PwC Germany | \[confirm\] | §4.5.4 SRP wording; AR three-option framing; §6.1.1 rolling release; case study callout |
| **Roman Zhukov** | \[confirm\] | OpenSSF GCP | \[confirm\] | ISO/IEC 18974 mapping; OWASP SAMM; PT1/PT3 alignment; implementation references |
| **Ummo Schwarting** | \[confirm\] | \[confirm\] | umm0 | VEX/CSAF status vocabulary; §4.2.3 format-native rewrite |
| **Adrian O'Sullivan** | \[confirm\] | \[confirm\] | \[confirm\] | §7.2.1 SBOM may wording correction |
| **Marcel Kurzmann** | \[confirm\] | Bosch | \[confirm\] | Evidence & Rationale column; hyperlinks throughout |
| **Ryan Tao** | \[confirm\] | \[confirm\] | \[confirm\] | §3.1.1 SBOM wording; §3.1.5 actively exploited CVE correction |
| **Mary (Meixia) Wang** | \[confirm\] | Linux Foundation | \[confirm\] | Column order; title; OpenChain CRA website page; community announcement |
| **Shin Hashizume** | \[confirm\] | \[confirm\] | \[confirm\] | Font and formatting feedback |
| **eaglei15** | \[confirm\] | \[confirm\] | eaglei15 | §4.2.3 CycloneDX false_positive VEX status contribution (GitHub PR #3) |

 

To add your name as a contributor, open a pull request or GitHub issue at github.com/OpenChain-Project/CRA-Compliance, or contact the working group lead.

 

# **Section 1: Introduction & Scope**

This document defines the organization compliance program for the EU Cyber Resilience Act (CRA), structured in alignment with the OpenChain Project adoption framework and ISO/IEC 18974 (Open Source Security Assurance). It serves as both a policy framework and a self-certification checklist.

The CRA (Regulation (EU) 2024/2847) establishes mandatory cybersecurity requirements for products with digital elements (PDEs) placed on the EU market. The following role definitions are drawn from CRA Art. 3:

 

**Role definitions (CRA Art. 3):**

●  Manufacturer (Art. 3(13)): a natural or legal person who develops or manufactures a PDE, or has a PDE designed or manufactured, and markets it under their name or trademark, whether for payment, free of charge, or as a monetary revenue-generating service.

●  Importer (Art. 3(17)): a natural or legal person established in the Union who places on the market a PDE bearing the name or trademark of a natural or legal person established outside the Union.

●  Distributor (Art. 3(18)): a natural or legal person in the supply chain, other than the manufacturer or importer, that makes a PDE available on the Union market.

●  OSS Steward (Art. 3(14)): a legal person, other than a manufacturer, who provides support on a sustained basis for the development of products qualifying as FOSS and ensures the viability of those products. The definition, scope, and obligations of OSS Stewards are established in CRA Art. 3(14), Recitals 18 and 19, and Art. 24\.

 

**Scope of this document:**

●  All software products with digital elements placed on the EU market by \[INSERT: Full legal entity name of manufacturer\]

●  Open-source components included in released products

●  Software supply chain processes including SBOM generation, vulnerability management, and disclosure

●  Personnel and processes involved in development, security operations, legal, and compliance

 

Hardware scope note: Hardware-specific requirements (including §3.1.7 Hardware Bill of Materials) apply only to products containing physical hardware components. Software-only organizations may mark hardware-specific items N/A with documented rationale.

 

**Applicability by Organizational Role**

The CRA creates distinct obligations for different organizational roles. Determine which role(s) apply before completing this checklist. A single organization may occupy multiple roles simultaneously. Complete all sections that apply to each role held.

 

| Section | Manufacturer | Importer | Distributor | OSS Steward | Both Mfr+Steward | Notes |
| :---- | :---- | :---- | :---- | :---- | :---- | :---- |
| **§2.1-2.4 Governance** | Required | Required | Required | Recommended | Required | All roles need basic governance |
| **§2.5-2.6 Categorization** | Required | Required | Required | N/A | Required | Stewards are not manufacturers; conformity assessment does not apply |
| **§3.1-3.4 SBOM & SDLC** | Required | N/A | N/A | N/A | Required | Manufacturer builds the product |
| **§3.5 Importer/Distributor** | N/A | Required | Required | See note\* | N/A | \*Art. 24 may bring stewards into scope depending on activities |
| **§4 Vuln Handling** | Required | Partial (§4.4 only) | Partial (§4.4 only) | Partial (see note\*\*) | Required | \*\*Art. 14(1) applies where steward is involved in development; Art. 14(3) and 14(8) apply where severe incidents affect network/information systems provided by the steward |
| **§5 OSS Stewardship** | Optional | Optional | Optional | Required | Required | Core for steward role |
| **§6 Support Period** | Required | N/A | N/A | N/A | Required | Manufacturer sets support period |
| **§7.1-7.4 Technical File** | Required | Verify only | Verify only | N/A | Required | Importers check, not produce |
| **§8 Cross-Framework** | As applicable | As applicable | As applicable | N/A | As applicable | Based on NIS2/DORA/AI Act scope |
| **§9 Procurement** | Optional | Optional | Optional | N/A | Optional | Buyer-side obligation |

 

Note on OSS Steward column: "Optional" indicates the section is not typically required by CRA obligations for stewards but may be adopted voluntarily. "Recommended" indicates good practice. OSS Stewards must maintain a security policy and vulnerability handling process (CRA Art. 24 and Annex II). Note: under Art. 24, stewards may also fall within scope of §3.5 importer/distributor obligations depending on their activities. For Section 4 (Vulnerability Handling), Art. 14(1) applies to stewards to the extent they are involved in development; Art. 14(3) and 14(8) apply where severe incidents affect network and information systems provided by the steward for development of the relevant FOSS.

 

**Section Deadline & Standards Coverage Reference**

The table below shows which sections contain items subject to the 11 Sep 2026 Art. 14 reporting deadline, the 11 Dec 2027 full CRA compliance deadline, and ISO/IEC 18974 coverage.

 

| Ref | Section Title | Art. 14 Reporting Deadline (11 Sep 2026\) | CRA Full Compliance Deadline (11 Dec 2027\) | Covered by ISO/IEC 18974? |
| :---- | :---- | :---- | :---- | :---- |
| **2.1** | CRA Policy | No | No | Partial \- §3.1.1 security policy |
| **2.2** | Roles & Responsibilities | No | No | Yes \- §3.4.1 |
| **2.3** | Competence & Training | No | No | Yes \- §3.1.2 |
| **2.4** | Sustainability & Review | No | No | Yes \- §3.4.2 |
| **2.5** | Product Risk Categorization (incl. Art. 32(5) FOSS) | No | Yes \- 11 Dec 2027 | No \- CRA-specific |
| **2.6** | Harmonized Standards Tracking | No | Yes \- 11 Dec 2027 | No \- CRA-specific |
| **3.1** | SBOM Generation | Partial \- §3.1.5 SBOM depth tied to 24h window | Yes \- 11 Dec 2027 | Yes \- §3.2.1-3.2.3 |
| **3.2** | SBOM Data Quality | No | Yes \- 11 Dec 2027 | Yes \- §3.2.2 |
| **3.3** | Provenance & Integrity | No | Yes \- 11 Dec 2027 | Yes \- §3.2.3 |
| **3.4** | Secure Development Properties | No | Yes \- 11 Dec 2027 | Partial \- SDL not fully in 18974 |
| **3.5** | Importer & Distributor Obligations | No | Yes \- 11 Dec 2027 | No \- CRA-specific |
| **4.1** | Vulnerability Ingestion & Monitoring | Yes \- EUVD/KEV feeds required | No | Yes \- §3.3.1 |
| **4.2** | Risk Adjudication & Vulnerability Exchange | Yes \- exploitability informs Art. 14 | No | Yes \- §3.3.2 |
| **4.3** | Actionable Decisions | Yes \- decisions trigger Art. 14 clock | No | Yes \- §3.3.2 |
| **4.4** | Disclosure & Regulatory Reporting | **YES \- §4.4.2-4.4.5 11 Sep 2026** | No | Partial \- CVD only; ENISA cascade not in 18974 |
| **4.5** | Art. 14 Notification RACI | **YES \- all items 11 Sep 2026** | No | No \- CRA Art. 14 specific |
| **5.1** | OSS Contribution & Engagement | No | Yes \- 11 Dec 2027 | Partial \- §3.1.1 |
| **5.2** | Steward vs. Maintainer Boundaries | No | Yes \- 11 Dec 2027 | No \- CRA Steward concept not in 18974 |
| **6.1** | Support Period & Update Obligations | No | Yes \- 11 Dec 2027 | Partial \- patching yes; 5-year period not in 18974 |
| **7.1** | Market Surveillance Deliverables | No | Yes \- 11 Dec 2027 | Partial \- §3.5.1 |
| **7.2** | Downstream Customer Provisioning | No | Yes \- 11 Dec 2027 | Partial \- §3.2.1 |
| **7.3** | User-Facing Docs (Art. 13(18)/Annex II) | No | Yes \- 11 Dec 2027 | Partial \- §3.5.1 |
| **7.4** | EU DoC & CE Marking | No | Yes \- 11 Dec 2027 | Partial \- §3.5.1 |
| **7.5** | EU Authorized Representative | No | Yes \- 11 Dec 2027 if non-EU | No \- CRA-specific |
| **8.1** | CRA and NIS2 | Partial \- NIS2 incident aligns with Art. 14 | No | No \- regulatory mapping not in 18974 |
| **8.2** | CRA and AI Act | No | Yes \- 11 Dec 2027 | No |
| **8.3** | CRA and DORA | No | No | No |
| **8.4** | CRA and Data Act | No | No | No |
| **8.5** | CRA and eIDAS | No | No | No |
| **9.1** | Vendor CRA Qualification | Partial \- §9.1.4 Sep 2026 check | No | No |

   
**Important:** All bracketed \[INSERT ...\] fields throughout this document must be completed with organization-specific information before any compliance claim or self-certification is made. Unsigned or incomplete checklists do not constitute a valid conformity claim under CRA Regulation (EU) 2024/2847.

 

# **Section 2: Program Architecture & Governance**

This section establishes the organizational foundation for CRA compliance. Note: §2.1-2.4 apply to all roles including Stewards (as Recommended). §2.5 and §2.6 apply only to Manufacturers and Importers/Distributors; they are N/A for OSS Stewards.

 

## **2.1 CRA Policy**

A documented cybersecurity policy for CRA compliance defines the organization commitment and obligations. Note: §2.1 is targeted primarily at Manufacturers. The policy obligations for OSS Stewards are lighter and governed by CRA Art. 24 and Annex II.

 

| Ref | Requirement | Conformant? (Yes / No / Partial) | Evidence & Rationale | Guidance / Reference |
| :---- | :---- | :---- | :---- | :---- |
| **2.1.1** | \[CRA REQUIREMENT\] The organization must maintain a documented cybersecurity policy for CRA compliance. The policy should be formally approved by senior management or an equivalent governing body. | ☐&nbsp;Yes   ☐&nbsp;No   ☐&nbsp;Partial |   | Policy document; approval signature or board/exec minute. |
| **2.1.2** | \[GOOD PRACTICE\] The policy should be published and accessible to all relevant personnel. Per CRA Recital 76, manufacturers are encouraged to make their security policies publicly available, including in machine-readable format. | ☐&nbsp;Yes   ☐&nbsp;No   ☐&nbsp;Partial |   | URL or intranet link; screenshot or acknowledgement log. |
| **2.1.3** | \[CRA REQUIREMENT\] The policy must explicitly reference the organization's obligations under CRA Articles 13, 14, and 15 and Annex I Part II(5), which requires a policy on coordinated vulnerability disclosure. This is further detailed in Art. 13(8). PT3 additionally recommends a standalone vulnerability handling policy. | ☐&nbsp;Yes   ☐&nbsp;No   ☐&nbsp;Partial |   | Policy text mapped to CRA articles. |
| **2.1.4** | \[CRA REQUIREMENT\] The policy must cover the full product lifecycle: design, development, release, m aintenance, and end-of-support, consistent with the product lifetime obligations in CRA Art. 13(2) and the vulnerability handling obligations in Art. 13(6). | ☐&nbsp;Yes   ☐&nbsp;No   ☐&nbsp;Partial |   | Lifecycle phase coverage section in policy. |

 

## **2.2 Roles & Responsibilities**

Clear assignment of CRA compliance responsibilities across the organization.

 

| Ref | Requirement | Conformant? (Yes / No / Partial) | Evidence & Rationale | Guidance / Reference |
| :---- | :---- | :---- | :---- | :---- |
| **2.2.1** | \[CRA REQUIREMENT\] The organization must designate a named individual or function with documented authority over CRA compliance program decisions. | ☐&nbsp;Yes   ☐&nbsp;No   ☐&nbsp;Partial |   | RACI chart or org chart with role highlighted. |
| **2.2.2** | \[CRA REQUIREMENT\] Legal or regulatory counsel must have a defined role for interpreting CRA obligations, essential requirements, and regulatory changes. | ☐&nbsp;Yes   ☐&nbsp;No   ☐&nbsp;Partial |   | Legal review sign-off records. |
| **2.2.3** | \[GOOD PRACTICE\] The organization should assign responsibility for SBOM generation, dependency management, and secure-by-design requirements. This may be assigned to a product engineering function or equivalent. Note: assigning these responsibilities is good practice but is not itself a CRA requirement. | ☐&nbsp;Yes   ☐&nbsp;No   ☐&nbsp;Partial |   | Ticket/backlog owner assignments; job description excerpts. |
| **2.2.4** | \[GOOD PRACTICE\] The organization should assign responsibility for vulnerability monitoring, exploitability assessment, and security incident response activities required under CRA. These responsibilities may be distributed across functions as appropriate to the organization's size and structure. | ☐&nbsp;Yes   ☐&nbsp;No   ☐&nbsp;Partial |   | SecOps runbook referencing CRA. |
| **2.2.5** | \[GOOD PRACTICE\] Role assignments should be reviewed and updated at least annually or upon significant organizational change. | ☐&nbsp;Yes   ☐&nbsp;No   ☐&nbsp;Partial |   | Change-log or version history of the RACI document. |

 

## **2.3 Competence & Training**

Requirements for ensuring personnel dealing with CRA compliance, SBOMs, and vulnerability handling maintain current knowledge.

 

| Ref | Requirement | Conformant? (Yes / No / Partial) | Evidence & Rationale | Guidance / Reference |
| :---- | :---- | :---- | :---- | :---- |
| **2.3.1** | \[GOOD PRACTICE\] The organization should define a training curriculum covering CRA obligations, SBOM tooling, and vulnerability handling. | ☐&nbsp;Yes   ☐&nbsp;No   ☐&nbsp;Partial |   | Training plan document; LMS catalog entry. |
| **2.3.2** | \[GOOD PRACTICE\] Personnel with CRA compliance responsibilities should complete required training within a defined review cycle. | ☐&nbsp;Yes   ☐&nbsp;No   ☐&nbsp;Partial |   | Training completion records; LMS export. |
| **2.3.3** | \[GOOD PRACTICE\] Competence requirements (knowledge, skills, experience) should be documented for each CRA-relevant role. | ☐&nbsp;Yes   ☐&nbsp;No   ☐&nbsp;Partial |   | Role competency matrix. |
| **2.3.4** | \[GOOD PRACTICE\] A mechanism should exist to keep training current as CRA implementing acts and harmonized standards evolve. | ☐&nbsp;Yes   ☐&nbsp;No   ☐&nbsp;Partial |   | Curriculum review schedule; owner assignment. |

 

## **2.4 Sustainability & Review**

Periodic review processes to ensure CRA compliance mechanisms remain active and up-to-date across release cycles. This subsection also covers compliance exception management (§2.4.6-2.4.8).

 

| Ref | Requirement | Conformant? (Yes / No / Partial) | Evidence & Rationale | Guidance / Reference |
| :---- | :---- | :---- | :---- | :---- |
| **2.4.1** | \[GOOD PRACTICE\] The CRA compliance program should be reviewed at least once per calendar year. | ☐&nbsp;Yes   ☐&nbsp;No   ☐&nbsp;Partial |   | Review meeting minutes or audit report dated within 12 months. |
| **2.4.2** | \[GOOD PRACTICE\] Reviews should be triggered by major product releases, significant dependency changes, or changes to regulatory guidance. | ☐&nbsp;Yes   ☐&nbsp;No   ☐&nbsp;Partial |   | Event-driven review trigger list in governance document. |
| **2.4.3** | \[GOOD PRACTICE\] Review outcomes should be formally recorded and assigned to responsible owners with target resolution dates. | ☐&nbsp;Yes   ☐&nbsp;No   ☐&nbsp;Partial |   | Issue tracker or action log with owner and due date fields. |
| **2.4.4** | \[CRA REQUIREMENT\] The organization must maintain a process to retire or archive compliance records for end-of-life products. Technical documentation must be retained for at least 10 years after market placement, or for the duration of the support period or end of support, whichever is longer (CRA Art. 13(15)). | ☐&nbsp;Yes   ☐&nbsp;No   ☐&nbsp;Partial |   | EoL / archival procedure documentation. |
| **2.4.5** | \[GOOD PRACTICE\] The organization should conduct periodic internal audits of CRA compliance program effectiveness. | ☐&nbsp;Yes   ☐&nbsp;No   ☐&nbsp;Partial |   | Internal audit plan; audit report; finding tracker. |
| **2.4.6** | \[GOOD PRACTICE\] A compliance exception register should be maintained to document temporary deviations from controls, including rationale and expiry. | ☐&nbsp;Yes   ☐&nbsp;No   ☐&nbsp;Partial |   | Exception register template; approval workflow. |
| **2.4.7** | \[GOOD PRACTICE\] Each exception should be assigned a risk owner, a compensating control, and a defined review date. | ☐&nbsp;Yes   ☐&nbsp;No   ☐&nbsp;Partial |   | Exception record with owner, compensating control, and expiry date. |
| **2.4.8** | \[GOOD PRACTICE\] Expired exceptions should be reviewed and either resolved, renewed with updated justification, or escalated. | ☐&nbsp;Yes   ☐&nbsp;No   ☐&nbsp;Partial |   | Exception renewal procedure; escalation log. |

 

## **2.5 Product Risk Categorization & Conformity Assessment Route**

Before executing self-certification, the organization must determine the CRA product classification per CRA Art. 6, 24, and 32 and Annexes III-IV. Technical descriptions of product categories are specified in Implementing Regulation (EU) 2025/2392. Self-certification (Module A, per CRA Annex VIII Part 1\) is only lawful for Default products and certain Class I products using harmonized standards. Art. 32(5) provides an additional pathway for FOSS manufacturers; see item 2.5.9. Note: §2.5 and §2.6 are N/A for OSS Stewards.

 

| Ref | Requirement | Conformant? (Yes / No / Partial) | Evidence & Rationale | Guidance / Reference |
| :---- | :---- | :---- | :---- | :---- |
| **2.5.1** | \[CRA REQUIREMENT\] The organization must document whether each in-scope product constitutes a product with digital elements (PDE) under CRA Art. 3(1), distinguishing it from standalone SaaS excluded under Recital 12\. Products whose primary function is remote data processing for a PDE are in CRA scope; standalone SaaS not providing such processing falls under NIS2, not CRA. | ☐&nbsp;Yes   ☐&nbsp;No   ☐&nbsp;Partial |   | Scope determination memo referencing Recital 12 and Commission guidance C(2026) 5252; product-by-product classification table. |
| **2.5.2** | \[CRA REQUIREMENT\] Before selecting a conformity pathway, the organization must determine whether it has an EU establishment. If not EU-established, one of the following must be in place before market placement: (a) an EU Authorized Representative, (b) an EU-based importer, or (c) an EU-based fulfillment service provider. Cross-reference §7.4. | ☐&nbsp;Yes   ☐&nbsp;No   ☐&nbsp;Partial |   | EU establishment confirmation or, where applicable, signed AR mandate, importer agreement, or fulfillment provider contract. |
| **2.5.3** | \[CRA REQUIREMENT\] The organization must formally evaluate each in-scope product against CRA Annex III (Important Class I and II) and Annex IV (Critical) and record a product classification decision with supporting rationale. The technical descriptions of product categories are specified in Implementing Regulation (EU) 2025/2392. | ☐&nbsp;Yes   ☐&nbsp;No   ☐&nbsp;Partial |   | Classification register with product name, classification outcome, and decision date. Reference: CRA Annex III, Annex IV, and Implementing Regulation (EU) 2025/2392 (eur-lex.europa.eu/legal-content/EN/TXT/?uri=CELEX:32025R2392). |
| **2.5.4** | \[CRA REQUIREMENT\] For Default products, the organization may use self-certification (Internal Control \- Module A, per CRA Annex VIII Part 1\) provided the assessment basis is documented. Art. 32(5) provides an additional pathway for manufacturers of products qualifying as FOSS under the commercial-activity test; legal counsel should be consulted on applicability. | ☐&nbsp;Yes   ☐&nbsp;No   ☐&nbsp;Partial |   | Self-assessment record referencing applicable harmonized standard or essential requirements mapped to design. Reference: CRA Annex VIII Part 1 for Module A procedure. |
| **2.5.5** | \[CRA REQUIREMENT\] For Important Class I products, the organization must either: (a) apply a harmonized standard in full and use self-certification, or (b) engage a Notified Body. The decision must be documented and justified. | ☐&nbsp;Yes   ☐&nbsp;No   ☐&nbsp;Partial |   | Notified Body engagement letter OR harmonized standard coverage analysis; classification rationale memo. |
| **2.5.6** | \[CRA REQUIREMENT\] For Important Class II or Critical products, the organization must engage a Notified Body assessment or European Cybersecurity Certification Scheme and track it to completion before EU market placement. | ☐&nbsp;Yes   ☐&nbsp;No   ☐&nbsp;Partial |   | Notified Body contract; assessment status; EU type-examination certificate where required. |
| **2.5.7** | \[CRA REQUIREMENT\] Product classification must be reviewed upon any substantial modification (as defined in CRA Art. 3(32)) and at minimum annually. A substantial modification may change the product classification and trigger a new conformity assessment obligation. | ☐&nbsp;Yes   ☐&nbsp;No   ☐&nbsp;Partial |   | Classification review log; change-triggered review records. |
| **2.5.8** | \[GOOD PRACTICE\] The organization should maintain a documented classification decision procedure to ensure consistent classification of new products and substantial modifications. While not explicitly required by CRA text, this procedure supports demonstrable compliance with the classification obligations in Art. 6 and Art. 32\. | ☐&nbsp;Yes   ☐&nbsp;No   ☐&nbsp;Partial |   | Classification decision procedure; examples of classification decisions applied. |
| **2.5.9** | \[CRA REQUIREMENT\] For manufacturers of products qualifying as Free and Open Source Software (FOSS) under the commercial-activity test (§5.1.5), Art. 32(5) provides a specific conformity pathway. The organization must determine whether this pathway applies and document the determination with legal rationale. Where it applies, the organization must fulfill the applicable obligations under Art. 32(5) in lieu of the standard Module A or Notified Body routes. | ☐&nbsp;Yes   ☐&nbsp;No   ☐&nbsp;Partial |   | Legal determination memo on Art. 32(5) applicability; reference to Commission guidance C(2026) 5252 on commercial-activity test criteria. |

 

## **2.6 Harmonized Standards Tracking**

CRA conformity depends on harmonized standards under Standardisation Request M/606, developed by ETSI, CEN, and CENELEC. As of August 2026, PT1 and PT3 drafts have been updated significantly since their public inquiry versions; final versions are not yet publicly available but are expected imminently. PT1 public inquiry draft and PT3 public inquiry draft are accessible via the NBN portal. ISO 27001 and IEC 62443 do not automatically create a presumption of CRA Annex I conformity, though they may be used as supporting evidence per EC FAQ 6.1 and Annex VIII Part 1\. Commission guidance final published version: C(2026) 5252, published 27 Jul 2026\.

 

| Ref | Requirement | Conformant? (Yes / No / Partial) | Evidence & Rationale | Guidance / Reference |
| :---- | :---- | :---- | :---- | :---- |
| **2.6.1** | \[GOOD PRACTICE\] The organization should identify which harmonized standards under Standardisation Request M/606 are relevant to its product categories and actively monitor their publication status via ETSI, CEN, and CENELEC. | ☐&nbsp;Yes   ☐&nbsp;No   ☐&nbsp;Partial |   | Standards tracking register; assigned owner. PT1 public inquiry draft: app.nbn.be (search CEN PT1 CRA); PT3 public inquiry draft: app.nbn.be (search CEN PT3 CRA). Note: both drafts have been significantly updated since public inquiry; final versions are not yet publicly available. Monitor via CEN/CENELEC portal. |
| **2.6.2** | \[CRA REQUIREMENT\] Where harmonized standards relevant to the product are not yet available, the organization must document the gap and record whether a Notified Body has been engaged (required for Class I products absent harmonized standards). | ☐&nbsp;Yes   ☐&nbsp;No   ☐&nbsp;Partial |   | Conformity pathway decision log; Notified Body engagement record or written rationale. |
| **2.6.3** | \[GOOD PRACTICE\] The organization should be aware that ISO 27001, IEC 62443, and similar general security standards do not automatically create a presumption of CRA Annex I conformity. CRA conformity must be assessed against Annex I requirements directly. However, per EC FAQ chapter 6.1 and Annex VIII, existing certifications under such standards may be used as supporting evidence within a broader conformity assessment, provided all Annex I essential requirements are explicitly addressed. | ☐&nbsp;Yes   ☐&nbsp;No   ☐&nbsp;Partial |   | Written acknowledgement in conformity documentation. |
| **2.6.4** | \[GOOD PRACTICE\] A trigger should exist to update the conformity pathway and re-run self-certification when a relevant M/606 harmonized standard is published. | ☐&nbsp;Yes   ☐&nbsp;No   ☐&nbsp;Partial |   | Standards publication monitoring procedure; update trigger defined in program governance. |

 

 

# **Section 3: Component Management & SBOM Quality**

This section governs the quality and integrity of SBOMs. CRA Article 13 requires manufacturers to document components with sufficient granularity to identify known vulnerabilities. OpenChain ISO/IEC 18974 requires a documented process for component identification and vulnerability tracking.

 

## **3.1 Software Identification & Bill of Materials**

Processes for generating machine-readable SBOMs for all released products. CRA requires SBOMs covering at the very least the top-level dependencies of those products.

 

| Ref | Requirement | Conformant? (Yes / No / Partial) | Evidence & Rationale | Guidance / Reference |
| :---- | :---- | :---- | :---- | :---- |
| **3.1.1** | \[CRA REQUIREMENT\] The organization must maintain a documented process for generating machine-readable SBOMs for all released products, covering at the very least the top-level dependencies of those products. | ☐&nbsp;Yes   ☐&nbsp;No   ☐&nbsp;Partial |   | SBOM generation procedure; tool configuration (e.g., Syft, Trivy, CycloneDX CLI). Reference: BSI TR-03183. |
| **3.1.2** | \[CRA REQUIREMENT\] SBOMs must be produced in a commonly used, machine-readable format, such as a currently supported version of SPDX or CycloneDX, and must comply with any applicable implementing acts, harmonized standards, or common specifications. | ☐&nbsp;Yes   ☐&nbsp;No   ☐&nbsp;Partial |   | Sample SBOM file; format validation report. Reference: BSI TR-03183-2 for SBOM content requirements. |
| **3.1.3** | \[GOOD PRACTICE\] SBOM generation should be integrated into the CI/CD pipeline and produce an artifact on every release build. | ☐&nbsp;Yes   ☐&nbsp;No   ☐&nbsp;Partial |   | Pipeline configuration excerpt; build artifact manifest. |
| **3.1.4** | \[CRA REQUIREMENT\] SBOMs must cover, at minimum, top-level dependencies and must include transitive and embedded dependencies to the depth necessary to identify, assess, and remediate vulnerabilities affecting the product. Any components or dependency levels not covered shall be documented together with a risk-based justification and the alternative measures used to ensure effective vulnerability management. | ☐&nbsp;Yes   ☐&nbsp;No   ☐&nbsp;Partial |   | Tooling depth configuration; documented exclusions with risk-based justification; sample SBOM component count vs. dependency graph audit. |
| **3.1.5** | ⚠ DEADLINE: 11 Sep 2026 \- ⚠  \[GOOD PRACTICE\] The organization should document a target SBOM depth decision with operational rationale tied to the ability to determine within 24 hours whether an actively exploited CVE affects any shipped product. A top-level-only SBOM may be insufficient for transitive-dependency scenarios. | ☐&nbsp;Yes   ☐&nbsp;No   ☐&nbsp;Partial |   | SBOM depth policy; operational rationale linking depth to 24-hour window; evidence of automated CVE-to-SBOM matching test. |
| **3.1.6** | \[CRA REQUIREMENT\] Each SBOM must include product-level metadata (product name, version, supplier, release date, unique product identifier) and component-level metadata (component name, version, supplier, unique component identifier such as PURL or CPE, cryptographic hash, and license information including declared and concluded license) for each component. Since this is an OpenChain Project document, inclusion of license information aligns with ISO/IEC 18974 and ISO/IEC 5230 obligations. | ☐&nbsp;Yes   ☐&nbsp;No   ☐&nbsp;Partial |   | SBOM field mapping to CRA Annex I (primary requirement), NTIA minimum elements (informational reference), and BSI TR-03183-2 (implementation guidance for German market). Where these references differ, CRA Annex I takes precedence. Reference: https://www.[bsi.bund.de](https://www.bsi.bund.de/EN/Themen/Unternehmen-und-Organisationen/Standards-und-Zertifizierung/Technische-Richtlinien/TR-nach-Thema-sortiert/tr03183/TR-03183_node.html)/TR03183 |
| **3.1.7** | \[GOOD PRACTICE\] For products containing physical hardware components, a Hardware Bill of Materials (HBOM) should be maintained alongside the SBOM to identify hardware components and their firmware dependencies. Software-only organizations may mark this item N/A with documented rationale. | ☐&nbsp;Yes   ☐&nbsp;No   ☐&nbsp;Partial |   | HBOM in a machine-readable format; hardware component inventory; firmware version register. |
| **3.1.8** | \[GOOD PRACTICE\] The organization should maintain a dependency registry with pinned versions and approved component entries to ensure SBOM reproducibility across builds. | ☐&nbsp;Yes   ☐&nbsp;No   ☐&nbsp;Partial |   | Dependency lock files; package registry configuration; approved component list. |

 

## **3.2 Data Quality & Completeness**

Criteria for validating SBOM completeness, component granularity, and handling Known Unknowns.

 

| Ref | Requirement | Conformant? (Yes / No / Partial) | Evidence & Rationale | Guidance / Reference |
| :---- | :---- | :---- | :---- | :---- |
| **3.2.1** | \[GOOD PRACTICE\] A completeness validation gate should be applied to SBOMs before release, using automated or manual review. | ☐&nbsp;Yes   ☐&nbsp;No   ☐&nbsp;Partial |   | SBOM linting tool output (e.g., sbom-scorecard, ort); CI gate pass/fail log. |
| **3.2.2** | \[CRA REQUIREMENT\] The organization must maintain a defined policy for handling Known Unknowns \- components whose identity cannot be fully determined \- distinguishing them from intentionally withheld proprietary code. | ☐&nbsp;Yes   ☐&nbsp;No   ☐&nbsp;Partial |   | Policy text or SBOM annotation convention for unknown components. |
| **3.2.3** | \[CRA REQUIREMENT\] Minimum required SBOM fields per CRA Annex I and BSI TR-03183-2 must be validated for every component before SBOM sign-off. | ☐&nbsp;Yes   ☐&nbsp;No   ☐&nbsp;Partial |   | Validation rule set; example of a rejected SBOM and remediation. |
| **3.2.4** | \[GOOD PRACTICE\] Quality metrics for SBOMs (e.g., completeness score, field population rate) should be tracked and reviewed periodically. | ☐&nbsp;Yes   ☐&nbsp;No   ☐&nbsp;Partial |   | Dashboard screenshot or metrics report. |

 

## **3.3 Provenance & Integrity**

Mechanisms for verifying software origins, tamper prevention, change tracking, and secure build infrastructure.

 

| Ref | Requirement | Conformant? (Yes / No / Partial) | Evidence & Rationale | Guidance / Reference |
| :---- | :---- | :---- | :---- | :---- |
| **3.3.1** | \[CRA REQUIREMENT\] All components in released products must have a verified source (upstream repository URL, commit hash, or verified package registry coordinates). | ☐&nbsp;Yes   ☐&nbsp;No   ☐&nbsp;Partial |   | SBOM externalRef fields; PURL entries; reproducible-build artifacts. |
| **3.3.2** | \[CRA REQUIREMENT\] Cryptographic checksums (SHA-256 or stronger) must be recorded for all binary and source artifacts included in releases. | ☐&nbsp;Yes   ☐&nbsp;No   ☐&nbsp;Partial |   | Artifact manifest with hash values; signing key documentation. |
| **3.3.3** | \[GOOD PRACTICE\] A change-tracking mechanism should record component additions, removals, and version updates between releases. | ☐&nbsp;Yes   ☐&nbsp;No   ☐&nbsp;Partial |   | SBOM diff report between consecutive releases; changelog integration. |
| **3.3.4** | \[GOOD PRACTICE\] Software signing or attestation (e.g., Sigstore, in-toto, SLSA provenance) should be applied to release artifacts. | ☐&nbsp;Yes   ☐&nbsp;No   ☐&nbsp;Partial |   | Signing workflow; verification command for customers. SLSA framework: [slsa.dev](https://slsa.dev). |
| **3.3.5** | \[GOOD PRACTICE\] The organization should maintain a documented secure build infrastructure policy covering build environment isolation, reproducibility, and integrity verification. | ☐&nbsp;Yes   ☐&nbsp;No   ☐&nbsp;Partial |   | Build environment configuration; reproducible build evidence; infrastructure-as-code repository. |
| **3.3.6** | \[GOOD PRACTICE\] Build pipelines should be isolated from development environments and access to production build systems must be restricted to authorized personnel. | ☐&nbsp;Yes   ☐&nbsp;No   ☐&nbsp;Partial |   | Access control policy for build systems; audit log of build system access. |
| **3.3.7** | \[GOOD PRACTICE\] Build artifacts should be generated in a clean, reproducible environment and verified before promotion to release. | ☐&nbsp;Yes   ☐&nbsp;No   ☐&nbsp;Partial |   | Build verification procedure; clean-room build evidence. |
| **3.3.8** | \[GOOD PRACTICE\] Secrets (API keys, signing keys, credentials) must NOT be embedded in source code or build artifacts. A secrets management solution should be used. | ☐&nbsp;Yes   ☐&nbsp;No   ☐&nbsp;Partial |   | Secrets scanning tool configuration; secrets management policy; tool output showing no embedded secrets. |
| **3.3.9** | \[GOOD PRACTICE\] Signing keys used for release artifact attestation should be stored in a hardware security module (HSM) or equivalent key management system. | ☐&nbsp;Yes   ☐&nbsp;No   ☐&nbsp;Partial |   | Key management policy; HSM or KMS configuration evidence. |
| **3.3.10** | \[GOOD PRACTICE\] The organization should document the full chain of custody from source code commit to released artifact, enabling post-incident provenance analysis. | ☐&nbsp;Yes   ☐&nbsp;No   ☐&nbsp;Partial |   | Build provenance attestation (e.g., SLSA provenance); artifact lineage documentation. |
| **3.3.11** | \[GOOD PRACTICE\] Third-party build tools, compilers, and dependencies used in the build pipeline should be inventoried, version-pinned, and monitored for vulnerabilities. | ☐&nbsp;Yes   ☐&nbsp;No   ☐&nbsp;Partial |   | Build tool inventory; version pinning configuration; vulnerability monitoring scope including build tools. |
| **3.3.12** | \[GOOD PRACTICE\] The integrity of the build pipeline itself should be verified periodically through pipeline audits or automated integrity checks. | ☐&nbsp;Yes   ☐&nbsp;No   ☐&nbsp;Partial |   | Pipeline audit records; integrity check configuration; anomaly detection evidence. |

 

## **3.4 Secure Development Properties & Security Testing (CRA Annex I, Part I)**

CRA Annex I Part I mandates products are designed and produced with security by default. Items here supply required content for the Technical File (§7.1).

 

| Ref | Requirement | Conformant? (Yes / No / Partial) | Evidence & Rationale | Guidance / Reference |
| :---- | :---- | :---- | :---- | :---- |
| **3.4.1** | \[CRA REQUIREMENT\] Products must be delivered without default credentials. Where authentication is required, users must be prompted to set unique credentials on first use and default-deny network exposure must apply (CRA Annex I Part I). | ☐&nbsp;Yes   ☐&nbsp;No   ☐&nbsp;Partial |   | Secure configuration policy; product startup flow documentation; credential policy test records. |
| **3.4.2** | \[CRA REQUIREMENT\] Attack surface minimization must be applied: unnecessary ports, services, and interfaces must be disabled by default and documented in an inbound connections register. | ☐&nbsp;Yes   ☐&nbsp;No   ☐&nbsp;Partial |   | Secure defaults checklist; inbound connections register; network exposure map; hardening guide. |
| **3.4.3** | \[CRA REQUIREMENT\] Data in transit must be encrypted using current standards (TLS 1.2 or higher or equivalent). Data at rest must be encrypted where the cybersecurity risk assessment identifies sensitivity. | ☐&nbsp;Yes   ☐&nbsp;No   ☐&nbsp;Partial |   | Encryption policy; TLS configuration audit; data classification map. |
| **3.4.4** | \[CRA REQUIREMENT\] Memory-safety mechanisms must be applied where technically feasible (e.g., memory-safe languages, compiler mitigations such as ASLR, stack canaries, CFI). Any exceptions must be documented with compensating controls. | ☐&nbsp;Yes   ☐&nbsp;No   ☐&nbsp;Partial |   | Build flag configuration; language or runtime selection rationale; exception register. |
| **3.4.5** | \[CRA REQUIREMENT\] Static Application Security Testing (SAST) must be integrated into the CI/CD pipeline and executed on every release candidate. Critical and high findings must be resolved or formally risk-accepted before release. | ☐&nbsp;Yes   ☐&nbsp;No   ☐&nbsp;Partial |   | SAST tool configuration; scan results summary; finding disposition records. |
| **3.4.6** | \[CRA REQUIREMENT\] Dynamic Application Security Testing (DAST) or fuzzing must be applied at minimum on each major release and results must be documented. | ☐&nbsp;Yes   ☐&nbsp;No   ☐&nbsp;Partial |   | DAST or fuzzing tool output; results triage records; remediation evidence. |
| **3.4.7** | \[CRA REQUIREMENT\] Penetration testing or a structured threat-model-based security review must be performed at minimum annually or upon significant architectural change. An independent assessment should be used periodically. Findings must be tracked to remediation. | ☐&nbsp;Yes   ☐&nbsp;No   ☐&nbsp;Partial |   | Pentest report or security review record; finding tracker; remediation sign-off. |
| **3.4.8** | \[CRA REQUIREMENT\] Security testing evidence (SAST results, pentest reports, DAST outputs) must be retained as part of the Technical File. Retention period: at least 10 years after market placement, or the support period if longer (CRA Art. 13(15)). | ☐&nbsp;Yes   ☐&nbsp;No   ☐&nbsp;Partial |   | Technical File index entry for security testing artifacts; retention policy. |
| **3.4.9** | \[CRA REQUIREMENT\] A threat model must be produced for each product, covering the attack surface, threat actors, attack vectors, and mitigating controls. The threat model must be updated upon significant architectural change. | ☐&nbsp;Yes   ☐&nbsp;No   ☐&nbsp;Partial |   | Threat model document; methodology used (e.g., STRIDE, PASTA); update history. |
| **3.4.10** | \[CRA REQUIREMENT\] A documented release security gate must exist and must be passed before any product version is placed on the EU market. The gate must verify that all critical and high security findings are resolved or formally risk-accepted. | ☐&nbsp;Yes   ☐&nbsp;No   ☐&nbsp;Partial |   | Release gate checklist; sign-off evidence; exception log for accepted risks. |
| **3.4.11** | \[GOOD PRACTICE\] The organization should maintain a documented secure coding standard covering input validation, authentication, session management, error handling, and cryptographic usage, and must train developers on its application. | ☐&nbsp;Yes   ☐&nbsp;No   ☐&nbsp;Partial |   | Secure coding standard document; developer training records. |

 

## **3.5 Importer and Distributor Obligations**

CRA Art. 19 and Art. 20 place independent obligations on importers and distributors. Note: under Art. 24, OSS Stewards may also fall within scope of these obligations depending on their specific activities; legal determination is recommended.

 

| Ref | Requirement | Conformant? (Yes / No / Partial) | Evidence & Rationale | Guidance / Reference |
| :---- | :---- | :---- | :---- | :---- |
| **3.5.1** | \[CRA REQUIREMENT\] Before placing an imported product on the EU market, the organization must verify: (a) the manufacturer has completed the appropriate conformity assessment; (b) required technical documentation exists; (c) the product bears CE marking and includes the EU Declaration of Conformity; (d) the manufacturer has a vulnerability handling process in place for the declared support period (CRA Art. 19). Note: OSS Stewards may also fall within scope of these obligations under CRA Art. 24 depending on their activities; legal determination is recommended. | ☐&nbsp;Yes   ☐&nbsp;No   ☐&nbsp;Partial |   | Importer due-diligence checklist per product; manufacturer conformity evidence on file; CE mark verification record. |
| **3.5.2** | \[CRA REQUIREMENT\] If the organization has reason to believe an imported product is not in conformity with the CRA, it must NOT place it on the market until conformity is achieved, and must inform the manufacturer and, where appropriate, market surveillance authorities (CRA Art. 19). | ☐&nbsp;Yes   ☐&nbsp;No   ☐&nbsp;Partial |   | Non-conformity hold procedure; example record of a hold or escalation. |
| **3.5.3** | \[CRA REQUIREMENT\] As a distributor, the organization must verify the product bears CE marking, includes required instructions and information, and meets essential requirements before making it available. If the distributor becomes aware of a vulnerability or cybersecurity risk in a distributed product, it must notify the manufacturer and cooperate with market surveillance authorities (CRA Art. 20). | ☐&nbsp;Yes   ☐&nbsp;No   ☐&nbsp;Partial |   | Distributor due-diligence checklist; vulnerability notification procedure to manufacturer; market surveillance cooperation record. |
| **3.5.4** | \[CRA REQUIREMENT\] System integrators who combine components from multiple manufacturers into a solution placed on the EU market must formally determine whether they are acting as a manufacturer under the CRA. If so, the full conformity assessment obligation applies to the integrated system. | ☐&nbsp;Yes   ☐&nbsp;No   ☐&nbsp;Partial |   | System integrator role determination memo; legal sign-off; conformity assessment plan for the integrated system if applicable. |

 

 

# **Section 4: Vulnerability Handling & Vulnerability Exchange (VEX / CSAF)**

CRA Article 13(6) requires manufacturers to address vulnerabilities without undue delay. Article 14 establishes a mandatory three-stage reporting cascade to the CRA Single Reporting Platform (SRP). This section defines the end-to-end vulnerability lifecycle from ingestion through disclosure and regulatory notification.

 

## **4.1 Vulnerability Ingestion & Monitoring**

Process for continuously monitoring all identified software components in supported products against vulnerability databases and advisory feeds.

 

| Ref | Requirement | Conformant? (Yes / No / Partial) | Evidence & Rationale | Guidance / Reference |
| :---- | :---- | :---- | :---- | :---- |
| **4.1.1** | \[CRA REQUIREMENT\] During the support period, the organization must continuously monitor all identified software components contained in supported products against relevant vulnerability databases, supplier advisories, and other reliable vulnerability sources. Monitoring must be performed at a documented, risk-based frequency and at least daily where automated monitoring is available. Known gaps in component coverage must be documented and addressed through supplementary identification and monitoring measures. | ☐&nbsp;Yes   ☐&nbsp;No   ☐&nbsp;Partial |   | Tool configuration; EUVD ([euvd.enisa.europa.eu](https://euvd.enisa.europa.eu)) feed; NVD, OSV, GitHub Advisory feeds; example alert triggered by a new CVE. |
| **4.1.2** | \[GOOD PRACTICE\] Monitoring results should be logged and retained for audit purposes. | ☐&nbsp;Yes   ☐&nbsp;No   ☐&nbsp;Partial |   | Scan schedule configuration; log retention policy. |
| **4.1.3** | \[GOOD PRACTICE\] A defined intake process should triage new vulnerability alerts within a documented, risk-based SLA. | ☐&nbsp;Yes   ☐&nbsp;No   ☐&nbsp;Partial |   | Triage SLA table in vulnerability management policy. |
| **4.1.4** | \[GOOD PRACTICE\] Vulnerability data should be enriched with contextual scoring (e.g., EPSS, KEV catalog status) to support risk-based prioritization. A documented Patch SLA Matrix should define response timelines by severity tier. | ☐&nbsp;Yes   ☐&nbsp;No   ☐&nbsp;Partial |   | Enrichment pipeline documentation; Patch SLA Matrix; example enriched alert record. |
| **4.1.5** | \[CRA REQUIREMENT\] The EU Vulnerability Database (EUVD, operated by ENISA at euvd.enisa.europa.eu) must be included as a monitored ingestion feed. EUVD is the authoritative CRA source and may publish actively-exploited status ahead of other sources. | ☐&nbsp;Yes   ☐&nbsp;No   ☐&nbsp;Partial |   | EUVD feed configuration; monitoring tool screenshot showing EUVD as an ingestion source. |
| **4.1.6** | \[GOOD PRACTICE\] The CISA Known Exploited Vulnerabilities (KEV) catalog should be monitored as a trigger for immediate CRA reporting assessment. A KEV listing for any component in a shipped product should automatically initiate the Art. 14 Early Warning evaluation workflow. | ☐&nbsp;Yes   ☐&nbsp;No   ☐&nbsp;Partial |   | KEV monitoring configuration; documented linkage between KEV listing event and Art. 14 RACI trigger. |
| **4.1.7** | \[GOOD PRACTICE\] Vulnerability monitoring should extend to third-party and open-source components for which the manufacturer has not received an SBOM from the upstream supplier, using supplementary identification methods. | ☐&nbsp;Yes   ☐&nbsp;No   ☐&nbsp;Partial |   | Supplementary monitoring procedure for components without upstream SBOM; tooling configuration. |
| **4.1.8** | \[GOOD PRACTICE\] Vulnerability management KPIs (e.g., mean time to detect, mean time to remediate by severity tier, percentage of components with confirmed monitoring coverage) should be tracked and reviewed periodically. | ☐&nbsp;Yes   ☐&nbsp;No   ☐&nbsp;Partial |   | KPI dashboard or metrics report; review cadence documentation. |

 

## **4.2 Risk Adjudication & Vulnerability Exchange (VEX / CSAF)**

Evaluating vulnerability exploitability in context and issuing machine-readable exploitability statements conforming to a recognized standard (CSAF v2.0 VEX profile, CycloneDX VEX, or OpenVEX).

 

| Ref | Requirement | Conformant? (Yes / No / Partial) | Evidence & Rationale | Guidance / Reference |
| :---- | :---- | :---- | :---- | :---- |
| **4.2.1** | \[CRA REQUIREMENT\] The organization must maintain a documented vulnerability exploitability assessment process covering reachability analysis, exploitability in context, and environmental factors. | ☐&nbsp;Yes   ☐&nbsp;No   ☐&nbsp;Partial |   | Vulnerability exploitability assessment process document; assessment criteria checklist. Reference: CISA VEX minimum viable guidelines. |
| **4.2.2** | \[GOOD PRACTICE\] Vulnerability exploitability statements should be issued in a machine-readable format conforming to a recognised vulnerability exchange standard. Accepted formats include CSAF v2.0 VEX profile, CycloneDX 1.4+ VEX, or OpenVEX. | ☐&nbsp;Yes   ☐&nbsp;No   ☐&nbsp;Partial |   | Sample exploitability statement; tooling used (e.g., Interlynk vexctl, CycloneDX CLI, OpenVEX tooling). |
| **4.2.3** | \[GOOD PRACTICE\] Exploitability statements should conform to the native status vocabulary and justification fields of the chosen standard without modification. The chosen standard's status values must be used as defined (e.g., CSAF: fixed, known\_affected, known\_not\_affected, under\_investigation; CycloneDX: not\_affected, affected, fixed, under\_investigation, false\_positive). | ☐&nbsp;Yes   ☐&nbsp;No   ☐&nbsp;Partial |   | Exploitability statement status mapping table; sample justified statements per chosen standard. |
| **4.2.4** | \[GOOD PRACTICE\] Exploitability statements should be versioned, timestamped, and retained as part of the product's technical documentation. | ☐&nbsp;Yes   ☐&nbsp;No   ☐&nbsp;Partial |   | Exploitability statement archive; version control history. |
| **4.2.5** | \[GOOD PRACTICE\] A Safety Relevance classification should be applied to components where functional safety or AI/autonomous system context applies (e.g., SRIL/SRAP framework or equivalent). Organizations without safety-critical products may mark this item N/A with documented rationale. | ☐&nbsp;Yes   ☐&nbsp;No   ☐&nbsp;Partial |   | Safety relevance scoring methodology; component classification register. |

 

## **4.3 Actionable Decisions**

Defined criteria for four operational outcomes: Immediate Remediation, Monitored Deferral, Formal Risk Acceptance, and Escalation.

 

| Ref | Requirement | Conformant? (Yes / No / Partial) | Evidence & Rationale | Guidance / Reference |
| :---- | :---- | :---- | :---- | :---- |
| **4.3.1** | \[CRA REQUIREMENT\] The organization must document decision criteria for immediate remediation (e.g., actively exploited vulnerability confirmed, CVSS base score meeting a defined threshold, or safety-critical component affected). | ☐&nbsp;Yes   ☐&nbsp;No   ☐&nbsp;Partial |   | Decision matrix or policy text defining remediation triggers. |
| **4.3.2** | \[GOOD PRACTICE\] Decision criteria for monitored deferral should be documented, including maximum deferral window and re-assessment trigger. | ☐&nbsp;Yes   ☐&nbsp;No   ☐&nbsp;Partial |   | Deferral SLA table; re-assessment schedule. |
| **4.3.3** | \[GOOD PRACTICE\] Formal risk acceptance must require documented business justification, a named risk owner, and a defined expiry date. | ☐&nbsp;Yes   ☐&nbsp;No   ☐&nbsp;Partial |   | Risk acceptance form template; approval workflow. |
| **4.3.4** | \[CRA REQUIREMENT\] The organization must define escalation criteria and escalation paths, including when regulatory notification under CRA Art. 14 is triggered. | ☐&nbsp;Yes   ☐&nbsp;No   ☐&nbsp;Partial |   | Escalation matrix; contact list with roles. |
| **4.3.5** | \[GOOD PRACTICE\] All vulnerability disposition outcomes should be tracked in a vulnerability register with current status, owner, and resolution date. | ☐&nbsp;Yes   ☐&nbsp;No   ☐&nbsp;Partial |   | Vulnerability register schema; sample populated record. |

 

## **4.4 Disclosure & Regulatory Reporting (CRA Art. 14 Three-Stage Cascade)**

Standard operating procedures for publicly disclosing fixes, providing mitigation guidance, and meeting the three-stage CRA Article 14 regulatory reporting cascade: Early Warning (24h), Full Notification (72h), and Final Report. Items marked with a deadline are required before 11 Sep 2026\.

 

| Ref | Requirement | Conformant? (Yes / No / Partial) | Evidence & Rationale | Guidance / Reference |
| :---- | :---- | :---- | :---- | :---- |
| **4.4.1** | \[CRA REQUIREMENT\] The organization must maintain a security advisory process to notify affected customers and users without undue delay regarding actively exploited vulnerabilities or severe security incidents, including available mitigations and corrective actions (CRA Art. 14(8)). | ☐&nbsp;Yes   ☐&nbsp;No   ☐&nbsp;Partial |   | Advisory template; distribution channel list (CVE.org, product portal, mailing list). |
| **4.4.2** | ⚠ DEADLINE: 11 Sep 2026 \- ⚠  \[CRA REQUIREMENT\] Actively exploited vulnerabilities must be reported to ENISA via the CRA Single Reporting Platform (SRP) within 24 hours of the organization becoming aware of active exploitation (CRA Art. 14(2)(a) \- Early Warning). | ☐&nbsp;Yes   ☐&nbsp;No   ☐&nbsp;Partial |   | SRP submission runbook; on-call contact for SRP platform access; test submission record. |
| **4.4.3** | ⚠ DEADLINE: 11 Sep 2026 \- ⚠  \[CRA REQUIREMENT\] A full vulnerability notification must be submitted to the CRA Single Reporting Platform (SRP) without undue delay and, in any event, within 72 hours after the manufacturer becomes aware of the actively exploited vulnerability, including severity assessment, affected versions, and interim mitigations (CRA Art. 14(2)(b) \- Full Notification). | ☐&nbsp;Yes   ☐&nbsp;No   ☐&nbsp;Partial |   | Full notification template mapped to SRP required fields; 72-hour SLA documented in runbook. |
| **4.4.4** | ⚠ DEADLINE: 11 Sep 2026 \- ⚠  \[CRA REQUIREMENT\] A final report must be submitted to the CRA Single Reporting Platform (SRP) within 14 days after a corrective or mitigating measure becomes available, including root-cause analysis, remediation details, and disclosure timeline information (CRA Art. 14(2)(c) \- Final Report). | ☐&nbsp;Yes   ☐&nbsp;No   ☐&nbsp;Partial |   | Final report template; post-incident review procedure; 14-day SLA clock definition. |
| **4.4.5** | ⚠ DEADLINE: 11 Sep 2026 \- ⚠  \[CRA REQUIREMENT\] Severe security incidents impacting the availability, integrity, or confidentiality of a product with digital elements must be reported to ENISA via the CRA Single Reporting Platform (SRP) following the same three-stage cascade (CRA Art. 14(3)). The final report for severe incidents must be submitted within one month of the initial notification. | ☐&nbsp;Yes   ☐&nbsp;No   ☐&nbsp;Partial |   | Severe security incident definition document (aligns with NIS2 thresholds); incident triage criteria; one-month final report template. |
| **4.4.6** | \[CRA REQUIREMENT\] Affected customers and users must be notified without undue delay regarding actively exploited vulnerabilities or severe security incidents, including available mitigations and corrective actions (CRA Art. 14(8)). | ☐&nbsp;Yes   ☐&nbsp;No   ☐&nbsp;Partial |   | Customer advisory template; notification runbook; mailing list, portal, or security advisory feed evidence. |
| **4.4.7** | \[CRA REQUIREMENT\] The organization must publish a Coordinated Vulnerability Disclosure (CVD) policy covering researcher contact channel, response SLA, and safe harbor statement. | ☐&nbsp;Yes   ☐&nbsp;No   ☐&nbsp;Partial |   | CVD policy URL; security.txt file. Reference: ISO/IEC 30111 and 29147\. |
| **4.4.8** | \[CRA REQUIREMENT\] Where a security update is not immediately available, the organization must issue mitigation guidance (workarounds, configuration changes) to affected users without undue delay. | ☐&nbsp;Yes   ☐&nbsp;No   ☐&nbsp;Partial |   | Example advisory with mitigation section. |
| **4.4.9** | \[CRA REQUIREMENT\] The organization must formally identify the national CSIRT to which CRA Art. 14 reports are addressed. Where no EU establishment exists, the CSIRT is determined by where key cybersecurity decisions are made within the Union. This determination must be documented and reviewed annually. Note: CSIRT routing via an Authorized Representative is not among the formal AR obligations defined in CRA Art. 18(3) and should not be assumed as a standard pathway. | ☐&nbsp;Yes   ☐&nbsp;No   ☐&nbsp;Partial |   | CSIRT routing determination memo; reference to Delegated Regulation (EU) 2026/881. |
| **4.4.10** | \[CRA REQUIREMENT\] The organization must document that the SME fine exemption under CRA Art. 14 covers only the financial penalty for missing the 24-hour Early Warning window and does NOT exempt the organization from the reporting obligation itself. | ☐&nbsp;Yes   ☐&nbsp;No   ☐&nbsp;Partial |   | Written acknowledgement in compliance program documentation; Art. 14 RACI maintained regardless of SME status. |
| **4.4.11** | \[CRA REQUIREMENT\] The organization must be aware that under Delegated Regulation (EU) 2026/881, the receiving CSIRT may delay dissemination to other member state CSIRTs on justified cybersecurity grounds. Any delay must be strictly limited and ENISA must be informed immediately. The Art. 14 runbook must reference this mechanism. | ☐&nbsp;Yes   ☐&nbsp;No   ☐&nbsp;Partial |   | Art. 14 runbook section on CSIRT dissemination delay; reference to Delegated Regulation (EU) 2026/881. |

 

## **4.5 Art. 14 Notification RACI \- Roles & Trigger Ownership**

CRA Article 14 imposes hard time-based obligations requiring pre-assigned, tested role ownership. All deadline items must be completed before 11 Sep 2026\.

 

| Ref | Requirement | Conformant? (Yes / No / Partial) | Evidence & Rationale | Guidance / Reference |
| :---- | :---- | :---- | :---- | :---- |
| **4.5.1** | ⚠ DEADLINE: 11 Sep 2026 \- ⚠  \[CRA REQUIREMENT\] The organization must designate a named individual (by role) as the Art. 14 Notification Owner responsible for initiating the Early Warning submission to the CRA Single Reporting Platform (SRP) within the 24-hour clock. | ☐&nbsp;Yes   ☐&nbsp;No   ☐&nbsp;Partial |   | RACI table entry; named backup; on-call schedule. |
| **4.5.2** | ⚠ DEADLINE: 11 Sep 2026 \- ⚠  \[CRA REQUIREMENT\] The organization must designate a named individual (by role) responsible for completing and submitting the 72-hour Full Notification to the CRA Single Reporting Platform (SRP), empowered to escalate to legal or executive if additional approvals are required. | ☐&nbsp;Yes   ☐&nbsp;No   ☐&nbsp;Partial |   | RACI table entry; escalation path documented. |
| **4.5.3** | ⚠ DEADLINE: 11 Sep 2026 \- ⚠  \[CRA REQUIREMENT\] The organization must designate a named individual (by role) to own the 14-day Final Report for actively exploited vulnerabilities and the one-month final report for severe incidents, coordinate post-incident review inputs, and sign off on the submission. | ☐&nbsp;Yes   ☐&nbsp;No   ☐&nbsp;Partial |   | RACI table entry; final report review workflow. |
| **4.5.4** | ⚠ DEADLINE: 11 Sep 2026 \- \[CRA REQUIREMENT\] The organization must confirm the current CRA Single Reporting Platform (SRP) registration process directly with ENISA and the national CSIRT or market surveillance authority, since the platform account-registration mechanics were not yet publicly finalized as of mid-2026. The organization must complete at least one test submission or equivalent preparatory contact prior to 11 Sep 2026\. | ☐&nbsp;Yes   ☐&nbsp;No   ☐&nbsp;Partial |   | SRP account registration confirmation or national CSIRT contact record; test submission record or interim procedure documentation. |
| **4.5.5** | \[CRA REQUIREMENT\] The organization must maintain a documented procedure recording when awareness of an incident or actively exploited vulnerability first occurred, to establish the Art. 14 reporting clock start time. | ☐&nbsp;Yes   ☐&nbsp;No   ☐&nbsp;Partial |   | Incident log with awareness timestamp; governance documentation. |
| **4.5.6** | \[CRA REQUIREMENT\] The Art. 14 RACI must be reviewed and re-confirmed upon any relevant personnel change and at minimum annually. | ☐&nbsp;Yes   ☐&nbsp;No   ☐&nbsp;Partial |   | RACI version history; review record. |

 

 

# **Section 5: Open Source Software (OSS) Stewardship**

The definition, scope, and obligations of Open Source Software Stewards are established in CRA Art. 3(14), Recitals 18 and 19, and Art. 24\. This section governs upstream engagement, license compliance, and steward vs. maintainer boundaries.

 

## **5.1 Open Source Contribution & Engagement**

Policy for engaging with upstream open-source communities while maintaining CRA compliance.

 

| Ref | Requirement | Conformant? (Yes / No / Partial) | Evidence & Rationale | Guidance / Reference |
| :---- | :---- | :---- | :---- | :---- |
| **5.1.1** | \[GOOD PRACTICE\] The organization should maintain a documented policy governing how personnel contribute to upstream open-source projects, including CLA/DCO requirements and IP assignment rules. | ☐&nbsp;Yes   ☐&nbsp;No   ☐&nbsp;Partial |   | OSS contribution policy; CLA tool configuration. OpenChain ISO/IEC 5230 as reference. |
| **5.1.2** | \[CRA REQUIREMENT\] Security vulnerabilities discovered during product work must be responsibly disclosed to upstream maintainers before public disclosure (CRA Art. 13 manufacturer responsibility for third-party components). | ☐&nbsp;Yes   ☐&nbsp;No   ☐&nbsp;Partial |   | Upstream disclosure procedure; example disclosure record. |
| **5.1.3** | \[GOOD PRACTICE\] The organization should engage with relevant security working groups (e.g., OpenSSF, CISA, CycloneDX community) to improve OSS supply chain security. Note: This is a recommended good practice and is not a published CRA legal requirement. | ☐&nbsp;Yes   ☐&nbsp;No   ☐&nbsp;Partial |   | Membership records; meeting participation log; issue/PR contributions. |
| **5.1.4** | \[GOOD PRACTICE\] OSS dependencies should be assessed for community health (maintenance status, contributor diversity, EOL date) before adoption. Components whose EOL falls within the product support lifetime should be avoided or formally risk-accepted. | ☐&nbsp;Yes   ☐&nbsp;No   ☐&nbsp;Partial |   | Dependency health assessment checklist; tooling (e.g., OpenSSF Scorecard: [securityscorecards.dev](https://securityscorecards.dev)). |
| **5.1.5** | \[CRA REQUIREMENT\] For any OSS project where the manufacturer vs. steward classification is non-obvious, the organization must apply a formal commercial-activity test using criteria from Commission guidance C(2026) 5252: (a) charging a fee for the software; (b) charging for technical support exceeding cost recovery; (c) intending to monetize through a platform; (d) collecting personal data beyond security/compatibility purposes; (e) accepting donations exceeding operational costs. If any criterion is met, manufacturer obligations apply. | ☐&nbsp;Yes   ☐&nbsp;No   ☐&nbsp;Partial |   | Commercial-activity test worksheet per project; legal sign-off on borderline cases; reference to Commission guidance C(2026) 5252\. |
| **5.1.6** | \[CRA REQUIREMENT\] The organization must maintain a documented process for managing integration risk from upstream OSS components whose maintainers are not directly CRA-obligated. This process must cover how the organization assesses component security hygiene, monitors for vulnerabilities in those components, and documents its findings. Where upstream projects provide SBOM artifacts, CVD policies, or patch timelines, the organization should use them. Where they do not, the organization must document its compensating measures. The organization should support upstream projects in improving security transparency over time rather than treating the absence of these artifacts as a blocker. | ☐&nbsp;Yes   ☐&nbsp;No   ☐&nbsp;Partial |   | Upstream due-diligence checklist; criteria for accepting or rejecting components; reference to CRA Art. 13 manufacturer responsibility. |
| **5.1.7** | \[GOOD PRACTICE\] A dependency approval gate should exist requiring security review of new dependencies before they are introduced into supported products. | ☐&nbsp;Yes   ☐&nbsp;No   ☐&nbsp;Partial |   | Dependency approval procedure; approval workflow; example approved and rejected dependency records. |

 

## **5.2 Steward vs. Maintainer Boundaries**

Guidelines clarifying the distinct obligations of OSS Stewards under CRA Art. 3(14), Recitals 18 and 19, and Art. 24(1), versus individual project maintainers.

 

| Ref | Requirement | Conformant? (Yes / No / Partial) | Evidence & Rationale | Guidance / Reference |
| :---- | :---- | :---- | :---- | :---- |
| **5.2.1** | \[CRA REQUIREMENT\] The organization must document whether it meets the definition of an OSS Steward under CRA Art. 3(14) and record this determination with supporting rationale. | ☐&nbsp;Yes   ☐&nbsp;No   ☐&nbsp;Partial |   | Legal determination memo; CRA Art. 3(14) criteria checklist. |
| **5.2.2** | \[CRA REQUIREMENT\] For projects where the organization acts as Steward, a lightweight security policy must be published meeting the obligations in CRA Art. 24(1) and Annex II steward requirements. | ☐&nbsp;Yes   ☐&nbsp;No   ☐&nbsp;Partial |   | SECURITY.md or equivalent policy for each steward project. Reference: CRA Art. 24(1) and Annex II. |
| **5.2.3** | \[GOOD PRACTICE\] Internal maintainers should understand their distinct obligations vs. the organization's steward-level obligations and should receive appropriate guidance. | ☐&nbsp;Yes   ☐&nbsp;No   ☐&nbsp;Partial |   | Training or guidance document; maintainer role definition. |
| **5.2.4** | \[GOOD PRACTICE\] A registry of projects where the organization acts as Steward (vs. Manufacturer) should be maintained and reviewed annually. | ☐&nbsp;Yes   ☐&nbsp;No   ☐&nbsp;Partial |   | Steward registry document; review record. |

 

 

# **Section 6: Security Updates & Support Period**

CRA Article 13(2) requires manufacturers to formally document the expected support period and provide security updates throughout that period.

 

## **6.1 Support Period Definition & Update Obligations**

 

| Ref | Requirement | Conformant? (Yes / No / Partial) | Evidence & Rationale | Guidance / Reference |
| :---- | :---- | :---- | :---- | :---- |
| **6.1.1** | \[CRA REQUIREMENT\] The organization must define and publish the expected support period for each product with digital elements placed on the EU market. The support period must be at least five years unless the expected product lifetime is shorter. A rolling-release model is also a valid approach, provided the end of support is clearly communicated and security updates are provided throughout (CRA Art. 13(2)). | ☐&nbsp;Yes   ☐&nbsp;No   ☐&nbsp;Partial |   | Product lifecycle documentation; public-facing support statement; legal justification if period is less than 5 years; rolling-release policy if applicable. |
| **6.1.2** | \[CRA REQUIREMENT\] Security updates addressing vulnerabilities must be provided free of charge throughout the declared support period (CRA Art. 13(9)). | ☐&nbsp;Yes   ☐&nbsp;No   ☐&nbsp;Partial |   | Patch management policy; release history showing security updates issued within support window. |
| **6.1.3** | \[CRA REQUIREMENT\] The organization must document, implement, and test a secure software update mechanism including integrity verification of update packages, protection against rollback attacks, and automatic delivery by default where technically feasible with user opt-out capability. | ☐&nbsp;Yes   ☐&nbsp;No   ☐&nbsp;Partial |   | Update architecture document; signing key management; rollback-prevention test records; automatic update configuration. |
| **6.1.4** | \[CRA REQUIREMENT\] End-of-support dates and associated security implications must be communicated to customers and downstream integrators. Where feasible, at least 12 months advance notice should be given before the final security update (CRA Art. 13(8)). | ☐&nbsp;Yes   ☐&nbsp;No   ☐&nbsp;Partial |   | Customer communication records; EoL announcement template; advance notice evidence. |
| **6.1.5** | \[GOOD PRACTICE\] Where a product reaches end-of-support during an active vulnerability's remediation window, the organization should maintain a documented escalation procedure to manage customer risk. | ☐&nbsp;Yes   ☐&nbsp;No   ☐&nbsp;Partial |   | EoL vulnerability handling procedure; customer advisory template. |
| **6.1.6** | \[GOOD PRACTICE\] An end-of-support transition procedure should exist to guide customers through migration, including identification of supported alternatives and a timeline for ending security update delivery. | ☐&nbsp;Yes   ☐&nbsp;No   ☐&nbsp;Partial |   | EoL transition guide; customer migration documentation; timeline for final security update. |
| **6.1.7** | \[GOOD PRACTICE\] At end-of-life, the organization should provide or document a procedure for secure deletion of user data held by the product and for secure data transfer to alternative solutions. | ☐&nbsp;Yes   ☐&nbsp;No   ☐&nbsp;Partial |   | Data sanitization procedure; secure deletion test records; data portability documentation. |

 

 

# **Section 7: Technical File & Supply Chain Sharing**

CRA Articles 13(15) and 28 require manufacturers to prepare technical documentation and make it available to MSAs on request. This section ensures all legal documentation obligations are met.

 

## **7.1 Market Surveillance Deliverables**

 

| Ref | Requirement | Conformant? (Yes / No / Partial) | Evidence & Rationale | Guidance / Reference |
| :---- | :---- | :---- | :---- | :---- |
| **7.1.1** | \[CRA REQUIREMENT\] The organization must maintain a Technical File for each in-scope product containing all elements required by CRA Annex VII: product description, design documents, cybersecurity risk assessment, SDL evidence, security test results, SBOM, connections audit, EU Declaration of Conformity, and EOL declaration. | ☐&nbsp;Yes   ☐&nbsp;No   ☐&nbsp;Partial |   | Technical File index; storage location; access control. CRA Annex VII checklist. |
| **7.1.2** | \[CRA REQUIREMENT\] The organization must perform and maintain a documented cybersecurity risk assessment including threat modelling (attack surface, threat actors, attack vectors) with a documented methodology. The assessment must be performed before development begins and updated throughout the product lifecycle. | ☐&nbsp;Yes   ☐&nbsp;No   ☐&nbsp;Partial |   | Risk assessment report; threat model document; update history reviewed at each major release. |
| **7.1.3** | \[CRA REQUIREMENT\] The Technical File must be accessible to designated personnel and must be capable of being produced to a market surveillance authority (MSA) within the legally required timeframe. | ☐&nbsp;Yes   ☐&nbsp;No   ☐&nbsp;Partial |   | File retrieval SLA; named custodian. |
| **7.1.4** | \[CRA REQUIREMENT\] SBOMs included in the Technical File must be the same machine-readable artifacts generated by the CI/CD pipeline (no manual transcription). | ☐&nbsp;Yes   ☐&nbsp;No   ☐&nbsp;Partial |   | Pipeline artifact link to Technical File storage. |
| **7.1.5** | \[CRA REQUIREMENT\] Technical documentation must be retained for at least 10 years after placement on the market, or for the expected product lifetime or support period if longer (CRA Art. 13(15) and Art. 31(3)). | ☐&nbsp;Yes   ☐&nbsp;No   ☐&nbsp;Partial |   | Retention policy; archive location; destruction schedule. |
| **7.1.6** | \[GOOD PRACTICE\] The organization should maintain a documented MSA response workflow defining how a Technical File request from a market surveillance authority is received, processed, and fulfilled within the legally required timeframe. | ☐&nbsp;Yes   ☐&nbsp;No   ☐&nbsp;Partial |   | MSA response SOP; named responsible contact; estimated fulfillment timeline. |

 

## **7.2 Downstream & Customer Provisioning**

 

| Ref | Requirement | Conformant? (Yes / No / Partial) | Evidence & Rationale | Guidance / Reference |
| :---- | :---- | :---- | :---- | :---- |
| **7.2.1** | \[CRA REQUIREMENT\] The SBOM must be made available to market surveillance authorities upon reasoned request as part of the Technical File (CRA Annex VII). \[GOOD PRACTICE\] SBOMs may be made available to customers and integrators alongside each product release; this is strongly recommended practice but is not a CRA legal obligation enforceable against the manufacturer. | ☐&nbsp;Yes   ☐&nbsp;No   ☐&nbsp;Partial |   | SBOM delivery mechanism (portal, API, package metadata, attestation) where voluntarily provided; MSA Technical File access procedure. |
| **7.2.2** | \[GOOD PRACTICE\] Security advisories and vulnerability exploitability statements should be delivered to downstream integrators through a documented channel. | ☐&nbsp;Yes   ☐&nbsp;No   ☐&nbsp;Partial |   | Advisory distribution list; portal URL; API endpoint. |
| **7.2.3** | \[GOOD PRACTICE\] Contractual or technical mechanisms should be used to ensure downstream integrators receive timely security updates for embedded components. | ☐&nbsp;Yes   ☐&nbsp;No   ☐&nbsp;Partial |   | Contract clause or SLA; notification mechanism. |
| **7.2.4** | \[GOOD PRACTICE\] A process may exist to handle customer requests for additional SBOM detail or vulnerability information. Note: This is a good practice and is not a CRA legal obligation. | ☐&nbsp;Yes   ☐&nbsp;No   ☐&nbsp;Partial |   | Customer-facing SBOM request procedure; support ticket template. |
| **7.2.5** | \[GOOD PRACTICE\] Where the product transmits telemetry, the organization should document and validate that telemetry data collection is limited to what is necessary and that outbound connections are audited. | ☐&nbsp;Yes   ☐&nbsp;No   ☐&nbsp;Partial |   | Telemetry data inventory; outbound connections audit log; data minimisation policy. |

 

## **7.3 User-Facing Documentation (CRA Art. 13(18) / Annex II)**

CRA Art. 13(18) and Annex II require manufacturers to provide clear and understandable information and instructions to users. Note: CRA Art. 24 governs OSS Steward obligations, not manufacturer user-facing documentation.

 

| Ref | Requirement | Conformant? (Yes / No / Partial) | Evidence & Rationale | Guidance / Reference |
| :---- | :---- | :---- | :---- | :---- |
| **7.3.1** | \[CRA REQUIREMENT\] The organization must provide information and instructions to users in a language easily understood by them, covering: intended use, cybersecurity properties, how to configure security settings, the declared end-of-support date, and how to report vulnerabilities (CRA Art. 13(18) / Annex II). | ☐&nbsp;Yes   ☐&nbsp;No   ☐&nbsp;Partial |   | User manual or README; Annex II compliance checklist; language coverage evidence. |
| **7.3.2** | \[CRA REQUIREMENT\] The EU DoC must be kept up-to-date and must be updated upon any significant product change affecting the conformity assessment basis. | ☐&nbsp;Yes   ☐&nbsp;No   ☐&nbsp;Partial |   | DoC version history; update procedure documentation. |
| **7.3.3** | \[CRA REQUIREMENT\] The CE marking (or, for software-only products distributed digitally, a digital CE marking accessible on the product website) must be affixed before EU market placement (CRA Art. 30). | ☐&nbsp;Yes   ☐&nbsp;No   ☐&nbsp;Partial |   | CE mark placement evidence (screenshot, label photograph, or packaging proof); digital CE mark URL. |
| **7.3.4** | \[CRA REQUIREMENT\] The EU DoC must be made available to market surveillance authorities and must be retained for at least 10 years after last placement on the EU market. | ☐&nbsp;Yes   ☐&nbsp;No   ☐&nbsp;Partial |   | DoC storage location; access control; retention policy entry. |

 

## **7.4 EU Declaration of Conformity & CE Marking (CRA Art. 28 & 30\)**

 

| Ref | Requirement | Conformant? (Yes / No / Partial) | Evidence & Rationale | Guidance / Reference |
| :---- | :---- | :---- | :---- | :---- |
| **7.4.1** | \[CRA REQUIREMENT\] The organization must determine whether it has an EU establishment as a manufacturer under CRA Art. 3(13). If not EU-established, one of the following must be in place before any product is placed on the EU market: (a) an EU Authorized Representative (AR) under CRA Art. 22/25; (b) an EU-based importer who places the product on the market; or (c) an EU-based fulfillment service provider acting under a written mandate. | ☐&nbsp;Yes   ☐&nbsp;No   ☐&nbsp;Partial |   | Legal determination memo; EU establishment confirmation or, where applicable, AR mandate, importer agreement, or fulfillment provider contract. |
| **7.4.2** | \[CRA REQUIREMENT\] Where the AR pathway is chosen, a written mandate must be executed before placing any product on the EU market. The mandate must specify at minimum the obligations defined in CRA Art. 18(3): (a) keeping the EU DoC and Technical File available to MSAs for at least 10 years or the support period whichever is longer; (b) providing MSAs with information and documentation necessary to demonstrate conformity upon reasoned request; (c) cooperating with MSAs on any action taken to eliminate risks posed by the product. | ☐&nbsp;Yes   ☐&nbsp;No   ☐&nbsp;Partial |   | Signed AR mandate; mandate text confirming Art. 18(3)(a-c) obligations; AR's EU address and contact details. |
| **7.4.3** | \[CRA REQUIREMENT\] Where the AR pathway is chosen, the AR's name, address, and contact details must be included on the product, its packaging, or accompanying documentation (CRA Art. 25). | ☐&nbsp;Yes   ☐&nbsp;No   ☐&nbsp;Partial |   | Product label or documentation showing AR details. |
| **7.4.4** | \[CRA REQUIREMENT\] Where the AR pathway is chosen, the AR must be provided with a copy of the EU DoC and Technical File and must be empowered to act on behalf of the manufacturer in dealings with market surveillance authorities. | ☐&nbsp;Yes   ☐&nbsp;No   ☐&nbsp;Partial |   | Document transmission record; access confirmation from AR. |
| **7.4.5** | \[GOOD PRACTICE\] Where the AR pathway is chosen, the organization should maintain documented operational procedures governing how the AR fulfills the Art. 18(3) obligations in practice, including escalation paths and communication protocols with MSAs. | ☐&nbsp;Yes   ☐&nbsp;No   ☐&nbsp;Partial |   | AR operational procedure document; communication protocol; escalation path. |

 

## **7.5 EU Authorized Representative (CRA Art. 22 / 25\)**

If not EU-established, one of three options is required before market placement: (a) EU Authorized Representative, (b) EU-based importer, or (c) EU-based fulfillment service provider. Items 7.5.2-7.5.5 apply only where the AR route is chosen.

 

| Ref | Requirement | Conformant? (Yes / No / Partial) | Evidence & Rationale | Guidance / Reference |
| :---- | :---- | :---- | :---- | :---- |

 

 

# **Section 8: Cross-Framework Integration**

The CRA sits within a broader EU digital regulatory stack. This section ensures the organization identifies where CRA conformity artifacts serve multiple regulatory obligations simultaneously.

 

## **8.1 CRA and NIS2**

 

| Ref | Requirement | Conformant? (Yes / No / Partial) | Evidence & Rationale | Guidance / Reference |
| :---- | :---- | :---- | :---- | :---- |
| **8.1.1** | \[GOOD PRACTICE\] The organization should determine whether it is subject to NIS2 (Directive (EU) 2022/2555) as an essential or important entity independently of its CRA manufacturer obligations. Where both apply, a mapping should exist showing how CRA product security artifacts satisfy NIS2 supply chain security assessment requirements (NIS2 Art. 21(2)(d)). | ☐&nbsp;Yes   ☐&nbsp;No   ☐&nbsp;Partial |   | Dual-framework mapping document; NIS2 supply chain security procedure referencing CRA conformity artifacts. |
| **8.1.2** | \[GOOD PRACTICE\] For organizations subject to both NIS2 and CRA, governance, risk assessment, and incident response processes should be designed to serve both frameworks on shared rather than parallel tracks where the underlying obligation is equivalent. | ☐&nbsp;Yes   ☐&nbsp;No   ☐&nbsp;Partial |   | Integrated GRC framework document; evidence that NIS2 incident reporting and CRA Art. 14 notification runbooks share escalation paths and RACI roles. |

 

## **8.2 CRA and AI Act**

 

| Ref | Requirement | Conformant? (Yes / No / Partial) | Evidence & Rationale | Guidance / Reference |
| :---- | :---- | :---- | :---- | :---- |
| **8.2.1** | \[GOOD PRACTICE\] For any product that is both a PDE under CRA and a high-risk AI system under the AI Act (Regulation (EU) 2024/1689), the organization should document that CRA Annex I compliance satisfies the AI Act Art. 15 cybersecurity requirements for that product, per CRA Art. 12\. | ☐&nbsp;Yes   ☐&nbsp;No   ☐&nbsp;Partial |   | AI Act / CRA dual-scope determination per product; mapping from CRA Annex I to AI Act Art. 15\. |
| **8.2.2** | \[GOOD PRACTICE\] For Important or Critical CRA products that are also high-risk AI systems, the organization should document that CRA conformity assessment requirements take precedence over AI Act internal control provisions for cybersecurity aspects (per CRA Art. 12). This precedence should be recorded in the product conformity assessment plan. | ☐&nbsp;Yes   ☐&nbsp;No   ☐&nbsp;Partial |   | Precedence determination in conformity assessment plan; legal review sign-off. |

 

## **8.3 CRA and DORA**

 

| Ref | Requirement | Conformant? (Yes / No / Partial) | Evidence & Rationale | Guidance / Reference |
| :---- | :---- | :---- | :---- | :---- |
| **8.3.1** | \[GOOD PRACTICE\] For organizations supplying digital products to financial entities subject to DORA (Regulation (EU) 2022/2554), CRA conformity documentation (Technical File, DoC, SBOM, vulnerability handling SLAs) should be identified as relevant input to DORA ICT third-party risk management due diligence and should be made available to financial entity customers on request. | ☐&nbsp;Yes   ☐&nbsp;No   ☐&nbsp;Partial |   | Customer-facing documentation list including DORA-relevant CRA artifacts; reference to DORA Art. 28-30. |

 

## **8.4 CRA and Data Act**

 

| Ref | Requirement | Conformant? (Yes / No / Partial) | Evidence & Rationale | Guidance / Reference |
| :---- | :---- | :---- | :---- | :---- |
| **8.4.1** | \[GOOD PRACTICE\] For connected products that simultaneously qualify under the Data Act (Regulation (EU) 2023/2854), overlapping obligations around data access, documentation, and user transparency should be identified, and the compliance program should address both regulations in a coordinated manner. | ☐&nbsp;Yes   ☐&nbsp;No   ☐&nbsp;Partial |   | Data Act / CRA product scope overlap assessment; coordinated documentation plan. |

 

## **8.5 CRA and eIDAS**

eIDAS 2.0 (Regulation (EU) 2024/1183) governs electronic identification and trust services. Where CRA products interact with eIDAS-governed identity services or where an Authorized Representative operates under eIDAS-regulated digital identity, the interaction between the two frameworks should be assessed.

 

| Ref | Requirement | Conformant? (Yes / No / Partial) | Evidence & Rationale | Guidance / Reference |
| :---- | :---- | :---- | :---- | :---- |
| **8.5.1** | \[GOOD PRACTICE\] For products that interact with eIDAS-governed electronic identification or trust services, the organization should assess whether eIDAS 2.0 (Regulation (EU) 2024/1183) creates obligations in addition to CRA, particularly where the product functions as a relying party or issues electronic attestations. | ☐&nbsp;Yes   ☐&nbsp;No   ☐&nbsp;Partial |   | Legal determination memo; eIDAS / CRA dual-scope assessment; reference to Regulation (EU) 2024/1183. |
| **8.5.2** | \[GOOD PRACTICE\] Where the organization appoints an EU Authorized Representative and that AR operates using eIDAS-regulated digital identity services, the organization should document how the eIDAS and CRA AR obligations interact and should seek legal counsel given the evolving hybridization of these frameworks. | ☐&nbsp;Yes   ☐&nbsp;No   ☐&nbsp;Partial |   | Legal counsel assessment; AR mandate review against eIDAS identity obligations; reference to CRA Art. 18 and eIDAS 2.0 Art. 45\. |

 

 

# **Section 9: Procurement & Buyer-Side Obligations**

The CRA changes what responsible procurement looks like. For organizations subject to NIS2, these questions are simultaneously regulatory requirements.

 

## **9.1 Vendor CRA Qualification**

 

| Ref | Requirement | Conformant? (Yes / No / Partial) | Evidence & Rationale | Guidance / Reference |
| :---- | :---- | :---- | :---- | :---- |
| **9.1.1** | \[GOOD PRACTICE\] The vendor evaluation process should require suppliers of products with digital elements to confirm: (a) the CRA product classification; (b) the conformity pathway used; (c) the declared support period end date. Note: The notified body used is published on the EU DoC and need not be separately collected. | ☐&nbsp;Yes   ☐&nbsp;No   ☐&nbsp;Partial |   | Updated vendor questionnaire or RFP template; example completed vendor response. |
| **9.1.2** | \[GOOD PRACTICE\] Procurement contracts for products with digital elements should include at minimum: (a) CRA conformity confirmation; (b) commitment to maintain vulnerability handling for the declared support period; (c) notification obligation to the buyer upon discovery of an actively exploited vulnerability in a supplied product. Note: Contractual access to Technical File or DoC is a good practice and not a CRA statutory obligation. | ☐&nbsp;Yes   ☐&nbsp;No   ☐&nbsp;Partial |   | Updated standard contract template with CRA clauses; legal review sign-off. |
| **9.1.3** | \[GOOD PRACTICE\] The organization should ask suppliers whether they produce SBOMs for procured products, in what format, and whether they are available. For high-assurance procurement, SBOM availability should be a mandatory procurement criterion. | ☐&nbsp;Yes   ☐&nbsp;No   ☐&nbsp;Partial |   | Supplier SBOM availability requirement in procurement policy; evidence of SBOM receipt or supplier declaration. |
| **9.1.4** | \[GOOD PRACTICE\] The organization should verify that suppliers have credible processes to detect and report actively exploited vulnerabilities in shipped components in a timely manner consistent with CRA Art. 14 obligations. | ☐&nbsp;Yes   ☐&nbsp;No   ☐&nbsp;Partial |   | Supplier due-diligence question on vulnerability monitoring capability; documented assessment outcome per supplier. |
| **9.1.5** | \[GOOD PRACTICE\] The organization should implement a supplier risk tiering model classifying vendors by the criticality of the components they supply, the security maturity of their CRA compliance program, and their vulnerability response track record. | ☐&nbsp;Yes   ☐&nbsp;No   ☐&nbsp;Partial |   | Supplier risk tier matrix; tiering criteria document; example tier assignment records. |

 

 

# **Implementation Roadmap**

The following phased model provides a structured approach to achieving self-certification.

 

| Phase | Key Action | Typical Owner | Target |
| :---- | :---- | :---- | :---- |
| **PRIORITY \- Art. 14 RACI (§4.4-4.5)** | Confirm current CRA Single Reporting Platform (SRP) registration process directly with ENISA and national CSIRT or MSA; assign named owners for 24h/72h/14-day notification stages; document severe security incident definition; complete at least one test submission or equivalent preparatory contact before the deadline. |   | **Before 11 Sep 2026 \- IMMEDIATE** |
| **1 \- Scope & Categorization** | Determine organizational role using §1 applicability table; confirm PDE vs SaaS (§2.5.1); complete EU establishment determination (§2.5.2/§7.5); complete risk classification including Art. 32(5) FOSS determination (§2.5.3-2.5.9). | Legal \+ CISO | Month 1-2 |
| **2 \- Policy & Governance** | Draft and approve CRA policy (§2.1); assign responsibilities (§2.2); training (§2.3); M/606/PT1/PT3 monitoring (§2.6). | Legal \+ CISO | Month 1-3 |
| **3 \- SBOM & SDLC** | Generate SBOMs per CRA original text covering at the very least top-level dependencies (§3.1); validate completeness including license information fields (§3.2); establish provenance signing (§3.3); implement SAST/DAST, threat modeling, release gate (§3.4); importer/distributor checklist (§3.5). | Platform Eng. | Month 2-4 |
| **4 \- Vuln Pipeline** | Deploy continuous monitoring including EUVD and KEV feeds (§4.1); exploitability assessment (§4.2); decision criteria (§4.3); CVD policy (§4.4). | SecOps | Month 3-5 |
| **5 \- Vulnerability Exchange & Disclosure** | Implement exploitability exchange workflow (§4.2); integrate SRP Art. 14 reporting runbook (§4.4); train responders; run tabletop exercise (§4.5). | SecOps \+ Legal | Month 4-6 |
| **6 \- OSS Governance** | Steward vs manufacturer determination per Art. 3(14), Recitals 18 and 19, Art. 24 (§5.1); upstream due-diligence (§5.1.6); publish SECURITY.md per Art. 24(1) (§5.2). | OSS Program | Month 5-7 |
| **7 \- Support Period** | Define and publish support periods; document secure update mechanism; EoL comms (§6.1). | Product \+ Legal | Month 5-7 |
| **8 \- Technical File & CE** | Compile Technical Files; draft EU DoC; affix CE marking; confirm AR/importer/fulfillment arrangement (§7.1-7.5). | Compliance PM | Month 6-8 |
| **8A \- Cross-Framework** | NIS2 (§8.1); AI Act (§8.2); DORA (§8.3); Data Act (§8.4); eIDAS (§8.5). | Legal \+ CISO | Month 7-9 |
| **8B \- Procurement** | Vendor CRA qualification (§9.1). | Legal \+ Procurement | Month 7-9 |
| **9 \- Self-Certification** | Complete this checklist; remediate gaps; conduct internal audit (§2.4.5); file conformance claim. Total items: 157\. | CRA Program Mgr | Month 8-10 |
| **10 \- Continuous Ops** | Annual review (§2.4); training refresh; SBOM quality; advisory cadence; annual tabletop exercise; PT1/PT3 monitoring. | All owners | Ongoing |

 

 

# **Self-Certification Summary**

**Legal notice:** Completing or signing this checklist does not in itself constitute a CRA conformity assessment, an EU Declaration of Conformity, or evidence of lawful CE marking. Self-certification (Module A) is only valid for Default and eligible Important Class I products. A conformity claim requires: (a) completion of all applicable checklist items with supporting evidence; (b) issuance of an EU Declaration of Conformity per Annex V; (c) proper CE marking per Art. 30\. Organizations are advised to seek qualified legal counsel before making a formal conformity claim.

 

Upon completing all checklist items, complete the attestation below.

 

| Organization | \[INSERT: Full legal entity name of manufacturer\] |
| :---- | :---- |
| **Organizational Role(s)** | \[INSERT: Manufacturer / Importer / Distributor / OSS Steward \- circle all that apply\] |
| **Product / Scope** | \[INSERT: Product name(s) and version(s) in scope\] |
| **Self-Certification Date** | \[Date\] |
| **CRA Program Manager** | \[INSERT: Name, Title \- Signature required for formal submission\] |
| **Next Review Date** | \[Date \- max 12 months from above\] |
| **Items answered Yes** | \[  \] of 157 total checklist items |
| **Items answered No/Partial** | \[  \] \- gap remediation plan attached: Yes / No |

 

 

# **Appendix B \- Definitions / Glossary**

The following terms are used throughout this document. Definitions align with CRA Regulation (EU) 2024/2847 Art. 3 unless otherwise noted.

 

| Term | Definition |
| :---- | :---- |
| **AR (Authorized Representative)** | An EU-established natural or legal person appointed by a non-EU manufacturer to act on its behalf for CRA obligations per Art. 18(3): (a) keeping DoC and Technical File available to MSAs; (b) providing MSAs with conformity information on reasoned request; (c) cooperating with MSAs on risk elimination. Note: AR is one of three options for non-EU market placement; the others are an EU importer or EU fulfillment service provider. |
| **CRA** | Cyber Resilience Act \- Regulation (EU) 2024/2847. |
| **CRA Single Reporting Platform (SRP)** | The platform operated by ENISA for receiving Art. 14 notifications of actively exploited vulnerabilities and severe security incidents. Note: the SRP account-registration mechanics were not yet publicly finalized as of mid-2026; organizations should confirm current process directly with ENISA and their national CSIRT or MSA. |
| **CSIRT** | Computer Security Incident Response Team \- a designated national authority responsible for receiving CRA Article 14 notifications. |
| **DoC (Declaration of Conformity)** | EU Declaration of Conformity per CRA Annex V \- required before CE marking and EU market placement. |
| **EPSS** | Exploit Prediction Scoring System \- probability score estimating likelihood of CVE exploitation within 30 days. |
| **EUVD** | EU Vulnerability Database \- operated by ENISA at euvd.enisa.europa.eu; distinct from the CRA Single Reporting Platform (SRP). |
| **KEV** | Known Exploited Vulnerabilities \- CISA catalog of CVEs confirmed actively exploited. |
| **MSA** | Market Surveillance Authority \- national authority enforcing CRA compliance (CRA Art. 58+). |
| **OSS Steward** | A legal person providing sustained support for FOSS development without qualifying as a manufacturer under the commercial-activity test. Definition, scope, and obligations established in CRA Art. 3(14), Recitals 18 and 19, and Art. 24\. |
| **PDE (Product with Digital Elements)** | Any software or hardware product whose intended use includes a direct or indirect data connection to a device or network (CRA Art. 3(1)). |
| **SBOM (Software Bill of Materials)** | A machine-readable inventory of software components in a product, covering at the very least the top-level dependencies, including component identifiers, versions, suppliers, and license information (CRA Annex I Part II; ISO/IEC 18974; ISO/IEC 5230). |
| **Substantial Modification** | A modification to a product after market placement that affects compliance with essential requirements or changes the intended purpose (CRA Art. 3(32)). |
| **Vulnerability Exchange (VEX / CSAF)** | A machine-readable statement communicating exploitability status of known vulnerabilities using the native status vocabulary of a recognised standard (CSAF v2.0 VEX profile, CycloneDX VEX, or OpenVEX). |

 

 

# **Appendix A \- CRA Annex I Traceability Matrix**

This matrix maps each CRA Annex I essential requirement to the corresponding control(s) in this document.

 

| CRA Annex I Requirement | Part | Control (Section Ref) | Evidence Expected |
| :---- | :---- | :---- | :---- |
| No known exploitable vulnerabilities at time of placing on market | Part I, §1 | 3.4.5, 3.4.6, 3.4.7 | SAST/DAST results; pentest report; vulnerability register showing zero unresolved critical findings at release |
| Secure by default configuration | Part I, §2 | 3.4.1, 3.4.2 | Secure defaults checklist; no default credentials policy; attack surface map |
| Protection against unauthorized access | Part I, §3 | 3.4.1, 3.4.3 | Authentication policy; TLS configuration audit; access control documentation |
| Protection of confidentiality and integrity of data | Part I, §4 | 3.4.3 | Encryption policy; data classification map; TLS 1.2+ configuration evidence |
| Availability protection and resilience | Part I, §5 | 3.4.2, 4.3 | Attack surface minimization evidence; incident response plan |
| Minimization of attack surface | Part I, §6 | 3.4.2 | Port/service inventory; hardening guide; network exposure map |
| Reduction of incident impact | Part I, §7 | 4.3, 4.4 | Escalation matrix; incident response runbook; Art. 14 RACI |
| Security update mechanism | Part I, §8 | 6.1.2, 6.1.3 | Update architecture; signing key management; rollback-prevention test records |
| Vulnerability disclosure policy | Part II, §1 (Annex I Part II(5)) | 4.4.7 | CVD policy URL; security.txt; SECURITY.md |
| Handling of known vulnerabilities | Part II, §2 | 4.1, 4.2, 4.3 | Vulnerability monitoring; exploitability exchange; triage SLA; patch SLA |
| Regular security updates | Part II, §3 | 6.1.2 | Patch release history; update delivery mechanism |
| Coordinated vulnerability disclosure | Part II, §4 | 4.4.7, 4.4.8 | CVD policy; advisory publication records |
| Mandatory regulatory notification (Art. 14\) | Part II, §5 | 4.4.2-4.4.6, 4.5 | SRP submission runbook; RACI; test submission record |
| SBOM documentation (covering at least top-level dependencies) | Part II, §6 | 3.1, 3.2 | Machine-readable SBOM; NTIA field coverage; license information fields (ISO/IEC 18974/5230) |
| Secure development lifecycle | Part I (general) | 3.3, 3.4 | Build provenance; secrets management; signing; SAST/DAST |
| Risk assessment documented | Annex VII | 7.1.1, 7.1.2 | Risk assessment report; threat model; update history |
| Technical file compiled | Annex VII | 7.1 | Technical File index; storage location; MSA retrieval SLA |
| EU Declaration of Conformity (Module A per Annex VIII Part 1\) | Annex V \+ Annex VIII Part 1 | 7.3.1-7.3.4 | Completed DoC per Annex V; CE mark evidence; retention record |

 

 

# **Appendix C \- ISO/IEC 18974 & OWASP SAMM Cross-Reference Mapping**

This mapping shows how ISO/IEC 18974 clauses and OWASP SAMM practices align with checklist sections. PT1/PT3 placeholder rows will be updated when final versions are published.

 

| ISO/IEC 18974 Clause | Requirement Summary | CRA Checklist Section(s) | OWASP SAMM Reference |
| :---- | :---- | :---- | :---- |
| **§3.1.1** | Security policy for open source | §2.1 CRA Policy, §5.1 | SAMM: Governance \> Policy & Compliance |
| **§3.1.2** | Competence and awareness | §2.3 Competence & Training | SAMM: Governance \> Education & Guidance |
| **§3.2.1** | SBOM process and tooling | §3.1 SBOM Generation | SAMM: Implementation \> Secure Build |
| **§3.2.2** | SBOM completeness and data quality (incl. license information per ISO/IEC 5230\) | §3.2 Data Quality | SAMM: Implementation \> Secure Build |
| **§3.2.3** | SBOM provenance and integrity | §3.3 Provenance & Integrity | SAMM: Implementation \> Secure Build |
| **§3.3.1** | Vulnerability identification process | §4.1 Vulnerability Monitoring | SAMM: Operations \> Vulnerability Management |
| **§3.3.2** | Vulnerability response and remediation | §4.2 Vuln Exchange, §4.3 Decisions | SAMM: Operations \> Vulnerability Management |
| **§3.3.3** | Coordinated vulnerability disclosure | §4.4.7 CVD Policy | SAMM: Operations \> Vulnerability Management |
| **§3.4.1** | Roles and responsibilities | §2.2 Roles & Responsibilities | SAMM: Governance \> Strategy & Metrics |
| **§3.4.2** | Program review and continuous improvement | §2.4 Sustainability & Review | SAMM: Governance \> Strategy & Metrics |
| **§3.5.1** | Conformance documentation | §7.1 Technical File, §7.3 EU DoC | SAMM: Governance \> Policy & Compliance |
| **PT1 (pending)** | CRA horizontal cybersecurity requirements | §3.4 Secure Dev Properties | To be mapped when final standard is published |
| **PT3 (pending)** | CRA vulnerability handling requirements | §4.1-4.5 Vuln Handling | To be mapped when final standard is published |

 

Community contribution: OpenSSF GCP and Eclipse ORC have offered to contribute implementation guidance for specific sections. Contributions welcome via GitHub pull request.

 

The working group welcomes anonymized implementation case studies from adopting organizations. If your organization has implemented this checklist and is willing to share your experience (anonymized), please contact the working group lead or open a GitHub issue at github.com/OpenChain-Project/CRA-Compliance.

 

 

# **Annex D \- Organizations Referencing This Checklist**

The following organizations have indicated that they reference or use this checklist in their CRA compliance programs. Listing here does not imply endorsement of any specific product or service, nor does it constitute a formal conformity certification.

 

| Organization | Description | Country | Reference Link |
| :---- | :---- | :---- | :---- |
| **Bitsea GmbH** | Open source security and compliance management; CRA compliance consulting and tooling. Active contributor to this checklist. | Germany | \[pending\] |
| **Interlynk** | SBOM lifecycle management and CRA compliance tooling; references this checklist as a resource on their EU CRA solutions page at interlynk.io. | United States | \[pending\] |
| **Lineaje** | Continuous software supply chain security and SBOM management platform; references this checklist as a CRA compliance resource on their Global Regulations page at lineaje.com. | United States | \[pending\] |
| **Revenera (Flexera)**  | SBOM management and CRA compliance tooling;  | United States  |  |
| **PwC Germany**  | CRA compliance advisory and assurance services.  | Germany  |  |
| **Anchore**  | Container and software supply chain security platform; SBOM generation, vulnerability monitoring, and CRA compliance tooling.  | United States  | https://anchore.com/sbom/eu-cra/ |

 

To add your organization, open a pull request or GitHub issue at github.com/OpenChain-Project/CRA-Compliance, or contact the working group lead.

 

 

# **References & Implementation Resources**

References marked as "draft" or "pending" are informational only and non-binding until formally adopted or published. This applies to all such references including those cited in §2.5.1, §2.6, §5.1.6, and Annex C.

 

**Regulatory & Legal**

 

●  EU Cyber Resilience Act (full text) \- [eur-lex.europa.eu/eli/reg/2024/2847/oj/eng](https://eur-lex.europa.eu/eli/reg/2024/2847/oj/eng)

●  Commission guidance C(2026) 5252 (final, 27 Jul 2026\) \- [digital-strategy.ec.europa.eu](https://digital-strategy.ec.europa.eu/en/library/commission-publishes-new-guidance-support-timely-cyber-resilience-act-implementation)

●  Implementing Regulation (EU) 2025/2392 \- Product category technical descriptions \- [eur-lex.europa.eu/legal-content/EN/TXT/?uri=CELEX:32025R2392](https://eur-lex.europa.eu/legal-content/EN/TXT/?uri=CELEX:32025R2392)

●  CRA Compliance Matrix (independent) \- [cyberresilienceact.eu/compliance-matrix.html](https://www.cyberresilienceact.eu/compliance-matrix.html)

●  ENISA EU Vulnerability Database (EUVD) \- [euvd.enisa.europa.eu](https://euvd.enisa.europa.eu)

●  Delegated Regulation (EU) 2026/881 \- CSIRT dissemination rules

●  NIS2 Directive (EU) 2022/2555

●  EU AI Act \- Regulation (EU) 2024/1689

●  DORA \- Regulation (EU) 2022/2554

●  Data Act \- Regulation (EU) 2023/2854

●  eIDAS 2.0 \- Regulation (EU) 2024/1183

 

**Standards**

 

●  ISO/IEC 18974:2023 \- Open Source Security Assurance Specification (OpenChain)

●  ISO/IEC 5230:2020 \- OpenChain Specification (License Compliance)

●  BSI TR-03183 \- Technical Guideline for Cyber Resilience \- [bsi.bund.de](https://www.bsi.bund.de/EN/Themen/Unternehmen-und-Organisationen/Standards-und-Zertifizierung/Technische-Richtlinien/TR-nach-Thema-sortiert/tr03183/TR-03183_node.html)

●  CEN/CENELEC PT1 \- CRA horizontal cybersecurity requirements (public inquiry draft via NBN portal; final version pending)

●  CEN/CENELEC PT3 \- CRA vulnerability handling requirements (public inquiry draft via NBN portal; final version pending)

●  M/606 Mandate \- ETSI/CEN/CENELEC harmonized standards for CRA Annex I

●  CRA Annex VIII Part 1 \- Module A Internal Control conformity assessment procedure

 

**SBOM & Tooling**

 

●  SPDX Specification 3.x \- [spdx.github.io/spdx-spec](https://spdx.github.io/spdx-spec)

●  CycloneDX Specification 1.6+ \- [cyclonedx.org](https://cyclonedx.org/specification)

●  NTIA Minimum Elements for an SBOM (informational reference) \- [ntia.gov](https://www.ntia.gov/report/2021/minimum-elements-software-bill-materials-sbom)

●  CISA VEX Minimum Viable Guidelines \- [cisa.gov](https://www.cisa.gov/resources-tools/resources/minimum-requirements-vulnerability-exploitability-exchange-vex)

●  SLSA Provenance Framework \- [slsa.dev](https://slsa.dev)

●  OpenSSF Scorecard \- [securityscorecards.dev](https://securityscorecards.dev)

●  CISA KEV Catalog \- [cisa.gov](https://www.cisa.gov/known-exploited-vulnerabilities-catalog)

 

**Community & Implementation Guidance**

 

●  OpenChain CRA Compliance page \- [openchainproject.org](https://openchainproject.org/cracompliance)

●  OpenChain CRA Compliance GitHub \- [github.com/OpenChain-Project/CRA-Compliance](https://github.com/OpenChain-Project/CRA-Compliance)

●  Community comments Google Doc \- [Google Doc (open for comments)](https://docs.google.com/document/d/1Wog28BZ9NQhY3tN9Wc2NDml2phBDuvYu9zkXSON5z5o/edit?usp=sharing)

●  OpenSSF SBOM Everywhere SIG \- [github.com/ossf/sbom-everywhere](https://github.com/ossf/sbom-everywhere)

●  OWASP SAMM \- [owaspsamm.org](https://owaspsamm.org)

●  Eclipse ORC (Open Regulatory Compliance) \- [eclipse.org/orc](https://eclipse.org/orc)

