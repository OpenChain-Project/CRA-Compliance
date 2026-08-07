

| OpenChain-Aligned Cyber Resilience Act (CRA) Compliance Requirements & Checklist Self-Certification Document   \-   ISO/IEC 18974 Aligned   \-   EU Regulation 2024/2847 |
| :---- |

   
 

 

| Document Title | CRA Compliance Requirements & Checklist |
| :---- | :---- |
| **Document Type** | Self-Certification / Governance Framework |
| **Current Version** | PA2 |
| **Date** | July 28, 2026 |
| **Status** | DRAFT \- Pre-Approval (PA) |
| **Review Cycle** | Annual; additionally triggered by major releases, significant dependency changes, or regulatory guidance updates (see §2.4.2) |
| **Document Owner** | Devashri Datta (Chairman) |
| **Standards Alignment** | ISO/IEC 18974 \- EU CRA (Reg. 2024/2847) \- OpenChain ISO/IEC 5230 |
| **CRA Art. 14 Reporting Deadline** | September 11, 2026 \- see §4.4-4.5 for mandatory actions |

   
**Abstract**

**This document defines the organizational compliance framework for the EU Cyber Resilience Act (CRA, Regulation 2024/2847), structured in alignment with the OpenChain Project's adoption framework and ISO/IEC 18974\. It serves simultaneously as a policy framework and a self-certification checklist, covering program governance, SBOM quality, vulnerability handling, regulatory reporting (including the CRA Article 14 three-stage cascade), OSS stewardship, and technical file obligations. This document does not constitute legal advice; consult qualified legal counsel before formal regulatory submission.**

   
 

   
**License:** CC-BY-4.0.  **Community:** OpenChain Project / Linux Foundation  **GitHub:** [github.com/OpenChain-Project/CRA-Compliance](https://github.com/OpenChain-Project/CRA-Compliance)

   
**Important:** All bracketed \[INSERT ...\] fields must be completed with organization-specific information before any compliance claim or self-certification is made.

 

# **Revision History**

 

| Version / Date | Description | Author |
| :---- | :---- | :---- |
| PA1 / Jul 21, 2026 | 1st draft \- full 5-section structure, Art. 14 cascade, §4.5 RACI | Devashri Datta |
| PA2 / Jul 28, 2026 | Incorporated community feedback: §7.4 AR wording corrected (AR is one of three options per Daniel Thompson-Yvetot); §1 applicability table by org role added; ISO/IEC 18974 \+ OWASP SAMM mapping added as Annex C; PT1/PT3 reference added to §2.6 and References; hyperlinks added throughout Guidance column and References section. Total items: 156\. | Devashri Datta |
| 1.0 / TBD | Initial approved release |   |

 

# **Contributors**

   
We would like to express our sincere gratitude to the following contributors and organizations, whose efforts and insights have been invaluable.

| Name | Email | Company | GitHub ID |
| :---- | :---- | :---- | :---- |
| **Devashri Datta (Chairman)** | devashri.datta@gmail.com |   | devashridatta-dotcom |

 

 

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

The table below shows, for each checklist section: (1) whether it contains items subject to the September 11, 2026 Art. 14 reporting deadline; (2) whether it contains items subject to the December 11, 2027 full CRA compliance deadline; and (3) whether the section is covered by ISO/IEC 18974\. Use this table to prioritize implementation effort.

 

| Ref | Section Title | Art. 14 Reporting Deadline (Sep 11, 2026\) | CRA Full Compliance Deadline (Dec 11, 2027\) | Covered by ISO/IEC 18974? |
| :---- | :---- | :---- | :---- | :---- |
| **2.1** | CRA Policy | No | No | Partial \- §3.1.1 security policy for open source |
| **2.2** | Roles & Responsibilities | No | No | Yes \- §3.4.1 roles and responsibilities |
| **2.3** | Competence & Training | No | No | Yes \- §3.1.2 competence and awareness |
| **2.4** | Sustainability & Review | No | No | Yes \- §3.4.2 program review and continuous improvement |
| **2.5** | Product Risk Categorization | No | Yes \- Dec 11, 2027 | No \- CRA-specific; no 18974 equivalent |
| **2.6** | Harmonized Standards Tracking | No | Yes \- Dec 11, 2027 | No \- CRA-specific regulatory requirement |
| **3.1** | SBOM Generation | Partial \- §3.1.5 SBOM depth required to meet 24h window | Yes \- Dec 11, 2027 | Yes \- §3.2.1-3.2.3 SBOM process and tooling |
| **3.2** | SBOM Data Quality | No | Yes \- Dec 11, 2027 | Yes \- §3.2.2 SBOM completeness and data quality |
| **3.3** | Provenance & Integrity | No | Yes \- Dec 11, 2027 | Yes \- §3.2.3 SBOM provenance and integrity |
| **3.4** | Secure Development Properties | No | Yes \- Dec 11, 2027 | Partial \- §3.3 covers vuln handling; full SDL not in 18974 |
| **3.5** | Importer & Distributor Obligations | No | Yes \- Dec 11, 2027 | No \- CRA-specific legal obligation |
| **4.1** | Vulnerability Ingestion & Monitoring | Yes \- EUVDB and KEV feeds required to detect exploited vulnerabilities before Sep 11, 2026 | No | Yes \- §3.3.1 vulnerability identification process |
| **4.2** | Risk Adjudication & VEX | Yes \- VEX output informs Art. 14 exploitability decisions | No | Yes \- §3.3.2 vulnerability response and remediation |
| **4.3** | Actionable Decisions | Yes \- remediation decisions trigger Art. 14 reporting clock | No | Yes \- §3.3.2 vulnerability remediation process |
| **4.4** | Disclosure & Regulatory Reporting | **YES \- §4.4.2-4.4.5 all subject to Sep 11, 2026 deadline** | No | Partial \- §3.3.3 CVD policy only; ENISA Art. 14 cascade not in 18974 |
| **4.5** | Art. 14 Notification RACI | **YES \- all six items subject to Sep 11, 2026 deadline** | No | No \- CRA Art. 14 regulatory obligation; not covered by 18974 |
| **5.1** | OSS Contribution & Engagement | No | Yes \- Dec 11, 2027 | Partial \- §3.1.1 security policy for open source |
| **5.2** | Steward vs. Maintainer Boundaries | No | Yes \- Dec 11, 2027 | No \- CRA Steward concept is not addressed in 18974 |
| **6.1** | Support Period & Update Obligations | No | Yes \- Dec 11, 2027 | Partial \- §3.3.2 covers patching; 5-year support period not in 18974 |
| **7.1** | Market Surveillance Deliverables | No | Yes \- Technical File required Dec 11, 2027 | Partial \- §3.5.1 conformance documentation |
| **7.2** | Downstream Customer Provisioning | No | Yes \- SBOM delivery required Dec 11, 2027 | Partial \- §3.2.1 SBOM process |
| **7.3** | EU DoC & CE Marking | No | Yes \- required Dec 11, 2027 | Partial \- §3.5.1 conformance documentation; CE marking not in 18974 |
| **7.4** | EU Authorized Representative | No | Yes \- required Dec 11, 2027 if non-EU | No \- CRA-specific legal requirement; not in 18974 |
| **8.1** | CRA and NIS2 | Partial \- NIS2 incident reporting aligns with Art. 14 cascade | No | No \- regulatory cross-mapping not in 18974 |
| **8.2** | CRA and AI Act | No | Yes \- Dec 11, 2027 | No \- regulatory cross-mapping not in 18974 |
| **8.3** | CRA and DORA | No | No | No \- regulatory cross-mapping not in 18974 |
| **8.4** | CRA and Data Act | No | No | No \- regulatory cross-mapping not in 18974 |
| **9.1** | Vendor CRA Qualification | Partial \- §9.1.4 supplier Sep 2026 monitoring capability check | No | No \- procurement obligations not covered by 18974 |

 

# **Section 2: Program Architecture & Governance**

This section establishes the organizational foundation for CRA compliance. Effective governance requires a documented policy commitment, clear role assignments, trained personnel, and a sustainable review cadence to ensure the program remains current across all release cycles.

 

## **2.1 CRA Policy**

A documented, published policy defining the organization's commitment to Cyber Resilience Act compliance and security assurance.

 

| Ref | Requirement | Conformant? (Yes / No / Partial) | Evidence & Rationale | Guidance / Reference |
| :---- | :---- | :---- | :---- | :---- |
| **2.1.1** | A written CRA compliance policy exists and has been formally approved by senior management. | ☐ Yes   ☐ No   ☐ Partial |   | Policy document reference; approval signature or board/exec minute. |
| **2.1.2** | The policy is published and accessible to all relevant personnel (internal) and publicly available on the organization's website or product portal. | ☐ Yes   ☐ No   ☐ Partial |   | URL or intranet link; screenshot or acknowledgement log. |
| **2.1.3** | The policy explicitly references obligations under EU CRA Articles 13, 14, and 15 (security requirements, vulnerability handling, reporting). | ☐ Yes   ☐ No   ☐ Partial |   | Policy text mapping to CRA articles. |
| **2.1.4** | The policy covers the full product lifecycle: design, development, release, maintenance, and end-of-support. | ☐ Yes   ☐ No   ☐ Partial |   | Lifecycle phase coverage section in policy. |

 

## **2.2 Roles & Responsibilities**

Clear assignment of CRA compliance roles across management, legal, product engineering, and security operations.

 

| Ref | Requirement | Conformant? (Yes / No / Partial) | Evidence & Rationale | Guidance / Reference |
| :---- | :---- | :---- | :---- | :---- |
| **2.2.1** | A named CRA Program Manager (or equivalent) is designated with documented authority over compliance program decisions. | ☐ Yes   ☐ No   ☐ Partial |   | RACI chart or org chart with role highlighted. |
| **2.2.2** | Legal/Regulatory counsel has a defined role for interpreting CRA obligations, essential requirements, and regulatory changes. | ☐ Yes   ☐ No   ☐ Partial |   | Legal review sign-off records. |
| **2.2.3** | Product Engineering has assigned owners for SBOM generation, dependency management, and secure-by-design requirements. | ☐ Yes   ☐ No   ☐ Partial |   | Ticket/backlog owner assignments; job description excerpts. |
| **2.2.4** | Security Operations has defined responsibilities for vulnerability monitoring, VEX issuance, and incident response under CRA. | ☐ Yes   ☐ No   ☐ Partial |   | SecOps runbook or on-call rotation referencing CRA. |
| **2.2.5** | Role assignments are reviewed and updated at least annually or upon significant organizational change. | ☐ Yes   ☐ No   ☐ Partial |   | Change-log or version history of the RACI document. |

 

## **2.3 Competence & Training**

Requirements for ensuring personnel dealing with CRA compliance, SBOMs, and vulnerability handling are properly trained and maintain current knowledge.

 

| Ref | Requirement | Conformant? (Yes / No / Partial) | Evidence & Rationale | Guidance / Reference |
| :---- | :---- | :---- | :---- | :---- |
| **2.3.1** | A training curriculum covering CRA obligations, SBOM tooling, and vulnerability handling is defined. | ☐ Yes   ☐ No   ☐ Partial |   | Training plan document; LMS catalog entry. |
| **2.3.2** | All personnel with CRA compliance responsibilities have completed required training within the last 12 months. | ☐ Yes   ☐ No   ☐ Partial |   | Training completion records; LMS export. |
| **2.3.3** | Competence requirements (knowledge, skills, experience) are documented for each CRA-relevant role. | ☐ Yes   ☐ No   ☐ Partial |   | Role competency matrix. |
| **2.3.4** | A mechanism exists to keep training current as CRA implementing acts and standards evolve. | ☐ Yes   ☐ No   ☐ Partial |   | Curriculum review schedule; owner assignment. |

 

## **2.4 Sustainability & Review**

Periodic review processes to ensure CRA compliance mechanisms remain active and up-to-date across release cycles. This subsection also covers compliance exception management (§2.4.6-2.4.8) for recording and governing temporary deviations from controls.

 

| Ref | Requirement | Conformant? (Yes / No / Partial) | Evidence & Rationale | Guidance / Reference |
| :---- | :---- | :---- | :---- | :---- |
| **2.4.1** | The CRA compliance program is reviewed at least once per calendar year. | ☐ Yes   ☐ No   ☐ Partial |   | Review meeting minutes or audit report dated within 12 months. |
| **2.4.2** | Reviews are triggered by major product releases, significant dependency changes, or changes to regulatory guidance. | ☐ Yes   ☐ No   ☐ Partial |   | Event-driven review trigger list in program governance document. |
| **2.4.3** | Review outcomes are formally recorded and assigned to responsible owners with target resolution dates. | ☐ Yes   ☐ No   ☐ Partial |   | Issue tracker or action log with owner and due date fields. |
| **2.4.4** | A process exists to retire or archive compliance records for end-of-life products in accordance with CRA retention requirements. | ☐ Yes   ☐ No   ☐ Partial |   | EoL / archival procedure documentation. Retention period: at least 10 years after market placement, or for the duration of the support period if longer (CRA Art. 13(15)) |
| **2.4.5** | An internal CRA compliance audit is conducted at least annually, prior to self-certification attestation. The audit must cover: (a) completeness of checklist responses; (b) evidence currency and accessibility; (c) open findings from the prior audit cycle. Results are documented in an audit report with a findings register, and management sign-off is obtained before attestation. | ☐ Yes   ☐ No   ☐ Partial |   | Audit report with scope and methodology; findings register with owner and target resolution date; management sign-off record. |
| **2.4.6** | A compliance exception register exists. Any temporary deviation from a CRA control must be formally recorded with: (a) the control reference being deviated from; (b) business rationale; (c) named owner; (d) risk assessment; (e) approval by the CRA Program Manager or delegate; (f) expiry date (maximum 90 days without re-approval). | ☐ Yes   ☐ No   ☐ Partial |   | Exception register template; example completed exception entry; approval workflow evidence. |
| **2.4.7** | Open exceptions are reviewed at minimum monthly by the CRA Program Manager and included as a standing agenda item at governance reviews (§2.4). Exceptions that cannot be remediated within the approval window are escalated to executive sign-off. | ☐ Yes   ☐ No   ☐ Partial |   | Exception review log; governance meeting minutes referencing exception status. |
| **2.4.8** | Expired or unresolved exceptions are flagged in the internal audit (§2.4.5) and included in the self-certification summary as open gaps. | ☐ Yes   ☐ No   ☐ Partial |   | Audit report section referencing exception register; self-certification gap list. |

 

## **2.5 Product Risk Categorization & Conformity Assessment Route**

Before executing self-certification, the organization must determine the CRA product classification (Default, Important Class I, Important Class II, or Critical) per CRA Art. 6, 24, and 32 and Annexes III-IV. Self-certification (Internal Control \- Module A) is only lawful for Default products and certain Class I products using harmonized standards. CRA Annex III lists Important product categories including identity and access management software, password managers, firewalls, network management software, VPNs, and intrusion detection systems.

 

| Ref | Requirement | Conformant? (Yes / No / Partial) | Evidence & Rationale | Guidance / Reference |
| :---- | :---- | :---- | :---- | :---- |
| **2.5.1** | The organization has documented whether each product in scope constitutes a "product with digital elements" (PDE) under CRA Art. 3(1) vs. standalone SaaS excluded under Recital 12\\. Products whose primary function is remote data processing for a PDE are in CRA scope; standalone SaaS not providing remote data processing for a PDE falls under NIS2, not CRA. | ☐ Yes   ☐ No   ☐ Partial |   | Scope determination memo referencing Recital 12 and Commission draft guidance (March 2026, §3.2.3); product-by-product classification table. |
| **2.5.2** | Before selecting a conformity pathway in §2.5, the organization has completed §7.4 (EU establishment determination and Authorized Representative appointment if required). If the organization is not EU-established and §7.4 is not yet complete, this gate must be resolved before proceeding.If the organization is EU-established, this item is N/A | ☐ Yes   ☐ No   ☐ Partial |   | Cross-reference: completed §7.4 checklist items (7.4.1-7.4.4); EU establishment confirmation or signed AR mandate. |
| **2.5.3** | The organization has formally evaluated each in-scope product against CRA Annex III (Important Class I & II) and Annex IV (Critical) criteria and recorded a product classification decision with supporting rationale. | ☐ Yes   ☐ No   ☐ Partial |   | Classification register with product name, classification outcome (Default / Important Class I / Important Class II / Critical), and decision date. |
| **2.5.4** | For products classified as Default, self-certification (Internal Control Module A) is used and the assessment basis is documented. | ☐ Yes   ☐ No   ☐ Partial |   | Self-assessment record referencing applicable harmonized standard(s) or essential requirements mapped to design. |
| **2.5.5** | For products classified as Important Class I, either (a) a harmonized standard is applied in full and self-certification is used, or (b) third-party conformity assessment by a Notified Body is engaged. This decision is documented and justified. | ☐ Yes   ☐ No   ☐ Partial |   | Notified Body engagement letter OR harmonized standard coverage analysis; classification rationale memo. |
| **2.5.6** | For products classified as Important Class II or Critical, a Notified Body assessment or European Cybersecurity Certification Scheme is engaged and tracked to completion before EU market placement. | ☐ Yes   ☐ No   ☐ Partial |   | Notified Body contract; assessment status; EU type-examination certificate (where required). |
| **2.5.7** | Product classification is reviewed upon significant product changes (new attack surfaces, new deployment contexts, new customer segments) and at minimum annually. | ☐ Yes   ☐ No   ☐ Partial |   | Classification review log; change-triggered review records. |
| **2.5.8** | The organization uses a structured product classification decision flow to determine CRA category. The decision sequence is: Step 1 \- Is the product a PDE under CRA Art. 3(1)? If No: CRA does not apply. If Yes: proceed. Step 2 \- Is the product listed in CRA Annex IV (Critical)? If Yes: Critical category, Notified Body mandatory. If No: proceed. Step 3 \- Is the product listed in CRA Annex III (Important Class II)? If Yes: Important Class II, Notified Body mandatory. If No: proceed. Step 4 \- Is the product listed in CRA Annex III (Important Class I)? If Yes: Important Class I, harmonized standard or Notified Body required. If No: Default category, self-certification (Module A) eligible. The classification outcome and each decision step are recorded with supporting rationale. | ☐ Yes   ☐ No   ☐ Partial |   | Completed classification decision flow per product; classification register with step-by-step rationale; reference to CRA Annexes III and IV criteria; legal review sign-off for non-obvious cases. |

 

## **2.6 Harmonized Standards Tracking**

CRA conformity for Default and Important Class I products depends on harmonized standards under Mandate M/606, being developed by ETSI, CEN, and CENELEC. As of mid-2026, first drafts are emerging but full Annex I coverage is not yet available. The CEN/CENELEC working group standards PT1 (horizontal cybersecurity requirements) and PT3 (vulnerability handling) are advancing toward publication; when published, they will provide the primary harmonized standard basis for Module A self-certification. ISO 27001 and IEC 62443 do not create a presumption of CRA conformity. Monitor PT1/PT3 public drafts via the CEN/CENELEC portal. This section ensures the organization tracks standard development and adjusts its conformity pathway as standards mature.

Informational notice: References in this document to Commission draft guidance (March 2026), PT1, and PT3 are informational and non-binding until formally adopted by the European Commission or published as official harmonized standards under Mandate M/606. Organizations should monitor official publication channels and update their conformity documentation accordingly.

 

| Ref | Requirement | Conformant? (Yes / No / Partial) | Evidence & Rationale | Guidance / Reference |
| :---- | :---- | :---- | :---- | :---- |
| **2.6.1** | The organization has identified which M/606 harmonized standards under development are relevant to its product categories and is actively monitoring their publication status via ETSI / CEN / CENELEC. | ☐ Yes   ☐ No   ☐ Partial |   | Standards tracking register; assigned owner; reference to ENISA standards mapping document. |
| **2.6.2** | Where harmonized standards relevant to the product are not yet available, the conformity pathway documentation acknowledges this gap and records whether a notified body has been engaged (required for Class I products absent harmonized standards). | ☐ Yes   ☐ No   ☐ Partial |   | Conformity pathway decision log; notified body engagement record or written rationale. |
| **2.6.3** | The organization does not rely on ISO 27001, IEC 62443, or equivalent general security standards as a basis for CRA conformity assessment. CRA conformity is assessed against Annex I requirements directly, pending M/606 finalization. | ☐ Yes   ☐ No   ☐ Partial |   | Written acknowledgement in conformity documentation; no reference to ISO 27001 / IEC 62443 as CRA conformity basis. |
| **2.6.4** | A trigger exists to update the conformity pathway and re-run self-certification when a relevant M/606 harmonized standard is published, allowing transition from notified-body-assisted to Module A self-certification where eligible. | ☐ Yes   ☐ No   ☐ Partial |   | Standards publication monitoring procedure; update trigger defined in program governance. |

 

 

# **Section 3: Component Management & SBOM Quality**

This section governs the quality and integrity of Software Bills of Materials (SBOMs). CRA Article 13 requires manufacturers to document components with sufficient granularity to identify known vulnerabilities. OpenChain ISO/IEC 18974 requires a documented process for component identification and vulnerability tracking.

 

## **3.1 Software Identification & Bill of Materials**

Processes for automatically generating and managing machine-readable SBOMs for all released products and dependencies.

 

| Ref | Requirement | Conformant? (Yes / No / Partial) | Evidence & Rationale | Guidance / Reference |
| :---- | :---- | :---- | :---- | :---- |
| **3.1.1** | A documented process exists for generating machine-readable SBOMs for all released products and major dependencies. | ☐ Yes   ☐ No   ☐ Partial |   | SBOM generation procedure; tool configuration (e.g., Syft, Trivy, CycloneDX CLI). |
| **3.1.2** | SBOMs are produced in at least one CRA-recognized format: SPDX 2.3+/3.x or CycloneDX 1.4+. | ☐ Yes   ☐ No   ☐ Partial |   | Sample SBOM file; format validation report. Note: CycloneDX 1.5+ recommended where native VEX embedding is required |
| **3.1.3** | SBOM generation is integrated into the CI/CD pipeline and produces an artifact on every release build. | ☐ Yes   ☐ No   ☐ Partial |   | Pipeline configuration excerpt; build artifact manifest. |
| **3.1.4** | SBOMs cover at minimum top-level dependencies and, where feasible, transitive dependencies sufficient to support vulnerability identification and remediation. | ☐ Yes   ☐ No   ☐ Partial |   | Tooling depth configuration; sample SBOM component count vs. dependency graph audit. |
| **3.1.5** | ⚠ DEADLINE: September 11, 2026 \- The organization recognizes that meeting the 24-hour Art. 14 reporting obligation requires component-level visibility beyond top-level dependencies. A documented decision exists on target SBOM depth, with the operational rationale tied to the ability to answer: "does a newly published CVE affect any shipped product within 24 hours?" A top-level-only SBOM is insufficient for transitive-dependency scenarios (e.g., log4shell-type events). | ☐ Yes   ☐ No   ☐ Partial |   | SBOM depth policy; operational rationale linking depth to 24h window; evidence of automated CVE-to-SBOM matching test run. |
| **3.1.6** | Each SBOM includes a timestamp, supplier, product name, version, and unique identifier for each component. | ☐ Yes   ☐ No   ☐ Partial |   | SBOM field mapping to NTIA minimum elements or CRA Annex I. |
| **3.1.7** | For products that include physical hardware components (embedded devices, integrated hardware-software products, IoT devices): a Hardware Bill of Materials (HBOM) is maintained alongside the SBOM. The HBOM must document at minimum: (a) hardware component name, manufacturer, and part number; (b) firmware version embedded in each hardware component; (c) known CVEs applicable to hardware components (where a hardware-specific NVD/CVE feed exists); (d) component supply chain provenance and country of origin where determinable. The HBOM is included in the Technical File (§7.1) and updated on each hardware revision. For software-only products with no hardware components, this item is N/A \- documented as such. | ☐ Yes   ☐ No   ☐ Partial |   | HBOM document in machine-readable format (CycloneDX hardware component type or equivalent); HBOM-to-SBOM linkage; CVE feed configuration for hardware components; Technical File index entry; N/A declaration for software-only products. |
| **3.1.8** | Dependencies for all CRA-scope products are retrieved from a defined set of approved registries or internal mirrors, and are version-pinned where technically feasible. A policy defines: (a) the list of approved package registries and internal mirrors; (b) the requirement to pin dependency versions (exact version or hash) in build manifests; (c) the process for approving exceptions where pinning is not feasible; (d) a procedure to detect and alert on unexpected registry sources in CI/CD pipeline artifact logs. This control reduces supply-chain substitution and typosquatting risk. | ☐ Yes   ☐ No   ☐ Partial |   | Approved registry list; build manifest showing pinned versions (e.g., lock files, hash pinning); exception register for unpinned dependencies; CI/CD registry-source validation log. |

 

## **3.2 Data Quality & Completeness**

Criteria for validating SBOM completeness, component granularity, and handling Known Unknowns, distinguishing genuinely unknown components from intentionally withheld proprietary code.

 

| Ref | Requirement | Conformant? (Yes / No / Partial) | Evidence & Rationale | Guidance / Reference |
| :---- | :---- | :---- | :---- | :---- |
| **3.2.1** | A completeness validation gate (automated or manual) is applied to SBOMs before release. | ☐ Yes   ☐ No   ☐ Partial |   | SBOM linting tool output (e.g., sbom-scorecard, ort); CI gate pass/fail log. |
| **3.2.2** | The organization has a defined policy for handling "Known Unknowns" components whose identity cannot be fully determined distinguishing them from intentionally withheld proprietary code. | ☐ Yes   ☐ No   ☐ Partial |   | Policy text or SBOM annotation convention for unknown components. |
| **3.2.3** | Minimum required SBOM fields (per NTIA or CRA Annex I) are validated for every component before SBOM sign-off. | ☐ Yes   ☐ No   ☐ Partial |   | Validation rule set; example of a rejected SBOM and remediation. |
| **3.2.4** | Quality metrics for SBOMs (e.g., completeness score, field population rate) are tracked and reviewed quarterly. | ☐ Yes   ☐ No   ☐ Partial |   | Dashboard screenshot or metrics report. |

 

## **3.3 Provenance & Integrity**

Mechanisms for verifying software origins, tamper prevention, change tracking across release cycles, and secure build infrastructure. Items 3.3.5-3.3.12 cover secure build infrastructure and secrets management requirements.

 

| Ref | Requirement | Conformant? (Yes / No / Partial) | Evidence & Rationale | Guidance / Reference |
| :---- | :---- | :---- | :---- | :---- |
| **3.3.1** | All components in released products have a verified source (upstream repository URL, commit hash, or verified package registry coordinates). | ☐ Yes   ☐ No   ☐ Partial |   | SBOM externalRef fields; PURL entries; reproducible-build artifacts. |
| **3.3.2** | Cryptographic checksums (SHA-256 or stronger) are recorded for all binary and source artifacts included in releases. | ☐ Yes   ☐ No   ☐ Partial |   | Artifact manifest with hash values; signing key documentation. |
| **3.3.3** | A change-tracking mechanism records component additions, removals, and version updates between releases. | ☐ Yes   ☐ No   ☐ Partial |   | SBOM diff report between consecutive releases; changelog integration. |
| **3.3.4** | Software signing or attestation (e.g., Sigstore, in-toto, SLSA provenance) is applied to release artifacts. | ☐ Yes   ☐ No   ☐ Partial |   | Signing workflow; verification command for customers. |
| **3.3.5** | Secure Build Infrastructure. Build systems are hardened: unnecessary services disabled, OS patched, and configuration baselined against a documented secure build standard. | ☐ Yes   ☐ No   ☐ Partial |   | Build system hardening checklist; configuration baseline document; last audit date. |
| **3.3.6** | Access to build infrastructure is restricted to authorized personnel via role-based access control; access reviews are conducted at least annually. | ☐ Yes   ☐ No   ☐ Partial |   | Access control policy; RBAC configuration; access review records. |
| **3.3.7** | CI/CD pipelines enforce segregation of duties: the developer who writes code cannot be the sole approver who merges and triggers production builds. | ☐ Yes   ☐ No   ☐ Partial |   | Pipeline branch protection rules; merge approval requirements; example PR showing required reviewers. |
| **3.3.8** | Build environments are ephemeral or reproducible where feasible; persistent build agents are monitored for unauthorized changes. | ☐ Yes   ☐ No   ☐ Partial |   | Build environment specification; ephemeral runner configuration or persistent-agent integrity monitoring evidence. |
| **3.3.9** | Build Secrets Management. No secrets, credentials, API keys, or signing certificates are hardcoded in source code, Dockerfiles, or pipeline configuration files. | ☐ Yes   ☐ No   ☐ Partial |   | Static secret scanning (e.g., truffleHog, gitleaks) integrated into CI; scan output showing zero hardcoded secrets. |
| **3.3.10** | All build secrets are stored in a dedicated secrets management system (e.g., HashiCorp Vault, AWS Secrets Manager, GitHub Encrypted Secrets) with access logging enabled. | ☐ Yes   ☐ No   ☐ Partial |   | Secrets manager configuration; access log sample; list of secrets managed. |
| **3.3.11** | Secrets are rotated on a defined schedule and immediately upon personnel departure or suspected compromise. | ☐ Yes   ☐ No   ☐ Partial |   | Rotation policy; rotation log; off-boarding checklist item. |
| **3.3.12** | Signing keys used for release artifact signing (§3.3.4) are stored in hardware security modules (HSMs) or equivalent key management infrastructure with audit logging. | ☐ Yes   ☐ No   ☐ Partial |   | HSM or KMS configuration; key usage audit log. |

 

## **3.4 Secure Development Properties & Security Testing (CRA Annex I, Part I)**

CRA Annex I, Part I mandates that products are designed, developed, and produced with security by default. This subsection covers pre-release secure coding properties and testing evidence required to substantiate conformity. Items here also supply required content for the Technical File (§7.1). OWASP SAMM provides a structured maturity model for SDL implementation \- see Annex C for mapping.

 

| Ref | Requirement | Conformant? (Yes / No / Partial) | Evidence & Rationale | Guidance / Reference |
| :---- | :---- | :---- | :---- | :---- |
| **3.4.1** | Products are delivered without default credentials; where authentication is required, users are prompted to set credentials on first use and default-deny network exposure applies. | ☐ Yes   ☐ No   ☐ Partial |   | Secure configuration policy; product startup flow documentation; credential policy test records. |
| **3.4.2** | Attack surface minimization is applied: unnecessary ports, services, and interfaces are disabled by default and documented. | ☐ Yes   ☐ No   ☐ Partial |   | Secure defaults checklist; network exposure map; hardening guide published to customers. |
| **3.4.3** | Data confidentiality and integrity controls are implemented: data in transit is encrypted using current standards (TLS 1.2+ or equivalent) and data at rest is encrypted where risk assessment identifies sensitivity. Cryptographic agility is maintained: all cryptographic algorithms in use are reviewed at least annually against current industry guidance (e.g., ENISA Cryptographic Guidelines, NIST SP 800-131A), and deprecated algorithms are retired within a defined timeline documented in the encryption policy. | ☐ Yes   ☐ No   ☐ Partial |   | Encryption policy including algorithm review schedule and deprecation timeline; TLS configuration audit; data classification map; most recent algorithm review record. |
| **3.4.4** | Memory-safety mechanisms are applied where feasible (e.g., use of memory-safe languages, compiler mitigations such as ASLR, stack canaries, CFI) and any exceptions are documented with compensating controls. | ☐ Yes   ☐ No   ☐ Partial |   | Build flag configuration; language/runtime selection rationale; exception register. |
| **3.4.5** | Static Application Security Testing (SAST) is integrated into the CI/CD pipeline and executed on every release candidate; findings are triaged and critical/high findings are resolved before release. | ☐ Yes   ☐ No   ☐ Partial |   | SAST tool configuration; scan results summary; finding disposition records. |
| **3.4.6** | Dynamic Application Security Testing (DAST) or fuzzing is applied at minimum on each major release and results are documented. | ☐ Yes   ☐ No   ☐ Partial |   | DAST/fuzzing tool output; results triage records; remediation evidence. |
| **3.4.7** | Penetration testing or structured threat-model-based security review is performed at minimum annually or upon significant architectural change; findings are tracked to remediation. An independent assessment (conducted by a party external to the development team) is performed at minimum every 24 months. Independence and scope are documented. | ☐ Yes   ☐ No   ☐ Partial |   | Pentest report or security review record with assessor independence statement; finding tracker; remediation sign-off; schedule showing 24-month independent assessment cadence. |
| **3.4.8** | Security testing evidence (SAST results, pentest reports, DAST outputs) is retained as part of the Technical File for submission to market surveillance authorities on request. | ☐ Yes   ☐ No   ☐ Partial |   | Technical File index entry for security testing artifacts; retention policy. Retention period: at least 10 years after market placement, or for the duration of the support period if longer (CRA Art. 13(15)) |
| **3.4.9** | Threat modeling is performed explicitly during initial product design and upon any major architectural change. The threat model must: (a) use a documented methodology (acceptable: STRIDE, Attack Trees, PASTA, or equivalent); (b) enumerate threat actors, attack surfaces, and attack paths; (c) map identified threats to mitigating controls. Threat model records are retained as part of the Technical File (§7.1). | ☐ Yes   ☐ No   ☐ Partial |   | Threat model document(s) with methodology identified; threat-to-control mapping table; update history showing re-assessment at major architectural changes; Technical File index entry. |
| **3.4.10** | A release security approval gate is enforced before any product version is placed on the EU market. Release cannot proceed unless all of the following are confirmed: (a) SBOM generated and validated (§3.1-3.2); (b) SAST scan completed with no unresolved critical or high findings (§3.4.5); (c) DAST or fuzzing completed (§3.4.6); (d) vulnerability review completed against current SBOM with triage decisions recorded (§4.2); (e) named security sign-off obtained from the designated security owner. | ☐ Yes   ☐ No   ☐ Partial |   | Completed release security checklist per release; sign-off record with named approver and date; CI/CD gate configuration showing blocked release on failed checks. |
| **3.4.11** | A mandatory secure coding standard is defined, published, and enforced for all development teams producing code for CRA-scope products. The standard must address at minimum: (a) prohibited functions and unsafe APIs (e.g., unbounded string operations in C/C++); (b) memory-safe language preference policy \- where memory-unsafe languages (C, C++) are used, compensating controls (ASLR, stack canaries, CFI, sanitizers) are documented and applied (§3.4.4); (c) input validation and output encoding requirements; (d) secrets handling rules (no hardcoded credentials, reference to §3.3.9-3.3.12); (e) SAST gate entry and exit criteria \- code may not merge to main without a passing SAST result. Compliance with the standard is verified during code review and confirmed in the release gate (§3.4.10). | ☐ Yes   ☐ No   ☐ Partial |   | Published secure coding standard with version history; SAST gate configuration showing merge-block on violation; memory-safe language policy or compensating control register; code review checklist referencing the standard. |

 

## **3.5 Importer and Distributor Obligations**

CRA Art. 19 and Art. 20 place independent obligations on importers and distributors of products with digital elements. These obligations apply in addition to \- not instead of \- the manufacturer obligations in §§2-3.4. Organizations that import or resell products must complete this sub-section.

 

| Ref | Requirement | Conformant? (Yes / No / Partial) | Evidence & Rationale | Guidance / Reference |
| :---- | :---- | :---- | :---- | :---- |
| **3.5.1** | Before placing an imported product on the EU market, the organization verifies: (a) the manufacturer has completed the appropriate conformity assessment; (b) the required technical documentation exists; (c) the product bears CE marking and includes the EU Declaration of Conformity; (d) the manufacturer has a vulnerability handling process in place for the declared support period. (CRA Art. 19\) | ☐ Yes   ☐ No   ☐ Partial |   | Importer due-diligence checklist per product; manufacturer conformity evidence on file; CE mark verification record. |
| **3.5.2** | If the organization has reason to believe an imported product is not in conformity with the CRA, it does not place it on the market until conformity is achieved, and it informs the manufacturer and, where appropriate, market surveillance authorities. (CRA Art. 19\) | ☐ Yes   ☐ No   ☐ Partial |   | Non-conformity hold procedure; example record of a hold or escalation. |
| **3.5.3** | As a distributor, the organization verifies the product bears the CE mark, includes required instructions and information, and meets essential requirements before making it available. If the distributor becomes aware of a vulnerability or cybersecurity risk in a distributed product, it notifies the manufacturer and cooperates with market surveillance authorities. (CRA Art. 20\) | ☐ Yes   ☐ No   ☐ Partial |   | Distributor due-diligence checklist; vulnerability notification procedure to manufacturer; market surveillance cooperation record. |
| **3.5.4** | System integrators who combine components from multiple manufacturers into a solution placed on the EU market have formally determined whether they are acting as a manufacturer under the CRA. If so, the full conformity assessment obligation applies to the integrated system, not just to the individual components. | ☐ Yes   ☐ No   ☐ Partial |   | System integrator role determination memo; legal sign-off; conformity assessment plan for the integrated system if applicable. |

 

 

# **Section 4: Vulnerability Handling & VEX (CRA Article 13 Alignment)**

CRA Article 13(6) requires manufacturers to address vulnerabilities without undue delay. Article 14 establishes a mandatory three-stage reporting cascade to the EU CRA Single Reporting Platform (EUVDB) for actively exploited vulnerabilities and severe security incidents. This section defines the end-to-end vulnerability lifecycle from ingestion through disclosure and regulatory notification.

 

## **4.1 Vulnerability Ingestion & Monitoring**

Process for continuously checking software components against known vulnerability databases and advisory feeds.

 

| Ref | Requirement | Conformant? (Yes / No / Partial) | Evidence & Rationale | Guidance / Reference |
| :---- | :---- | :---- | :---- | :---- |
| **4.1.1** | An automated process continuously monitors all product SBOMs against CVE databases (NVD, OSV, GitHub Advisory) and package manager advisories. | ☐ Yes   ☐ No   ☐ Partial |   | Tool configuration; example alert triggered by a new CVE. |
| **4.1.2** | Monitoring runs at minimum daily; results are logged and retained for audit purposes. | ☐ Yes   ☐ No   ☐ Partial |   | Scan schedule configuration; log retention policy. |
| **4.1.3** | A defined intake process triages new vulnerability alerts within a documented SLA (e.g., Critical: 24h, High: 72h). | ☐ Yes   ☐ No   ☐ Partial |   | Triage SLA table in vulnerability management policy. |
| **4.1.4** | A Patch SLA Matrix is defined and published, specifying the maximum target fix time by severity for vulnerabilities affecting products in active support (CRA Art. 13). The matrix must cover at minimum: Critical (≤7 days), High (≤30 days), Medium (≤90 days), Low (best effort / next scheduled release). Deviations require documented risk acceptance per §4.3.3. | ☐ Yes   ☐ No   ☐ Partial |   | Patch SLA Matrix document or policy section; evidence of matrix applied to recent vulnerability remediations. |
| **4.1.5** | Vulnerability data is enriched with EPSS scores and KEV catalog status to prioritize response. | ☐ Yes   ☐ No   ☐ Partial |   | Enrichment pipeline documentation; example enriched alert record. |
| **4.1.6** | The EU Vulnerability Database (EUVDB, operated by ENISA at euvdb.enisa.europa.eu) is included as a monitored ingestion feed alongside NVD, OSV, and GitHub Advisory. EUVDB is the authoritative CRA source and may publish actively-exploited status ahead of NVD. | ☐ Yes   ☐ No   ☐ Partial |   | EUVDB feed configuration; monitoring tool screenshot showing EUVDB as an ingestion source. |
| **4.1.7** | The CISA Known Exploited Vulnerabilities (KEV) catalog is monitored as a trigger for immediate 24-hour CRA reporting assessment. A KEV listing for any component in a shipped product automatically initiates the Art. 14 Early Warning evaluation workflow (§4.4.2). | ☐ Yes   ☐ No   ☐ Partial |   | KEV monitoring configuration; documented linkage between KEV listing event and Art. 14 RACI trigger (§4.5.1). |
| **4.1.8** | Vulnerability management effectiveness is measured and reported at minimum quarterly using defined KPIs. Required metrics include: (a) Mean Time to Triage (MTTT) \- time from CVE ingestion to triage decision; (b) Mean Time to Remediate (MTTR) \- time from triage to fix or accepted risk; (c) Open Critical Vulnerabilities \- count of unresolved CVSS 9.0+ or KEV-listed items; (d) Patch SLA Compliance % \- percentage of vulnerabilities remediated within the defined SLA per §4.1.4; (e) VEX Publication Latency \- time from triage decision to published VEX statement. Metrics are reviewed in governance meetings (§2.4) and used to drive continuous improvement. | ☐ Yes   ☐ No   ☐ Partial |   | Metrics dashboard or report showing all five KPIs; trend data across at least two reporting periods; governance review record referencing metrics. |

 

## **4.2 Risk Adjudication & VEX**

Evaluating vulnerability exploitability in context: reachability, environment, safety relevance and outputting machine-readable VEX statements.

 

| Ref | Requirement | Conformant? (Yes / No / Partial) | Evidence & Rationale | Guidance / Reference |
| :---- | :---- | :---- | :---- | :---- |
| **4.2.1** | A documented VEX (Vulnerability Exploitability eXchange) process exists, covering assessment of reachability, exploitability, and environmental context. | ☐ Yes   ☐ No   ☐ Partial |   | VEX process document; assessment criteria checklist. |
| **4.2.2** | VEX statements are issued in machine-readable format (CycloneDX VEX or OpenVEX) for all products in active support. | ☐ Yes   ☐ No   ☐ Partial |   | Sample VEX document; tooling used (e.g., Interlynk vexctl, CycloneDX CLI). |
| **4.2.3** | VEX justifications align with standard status values: not\_affected, affected, fixed, under\_investigation. | ☐ Yes   ☐ No   ☐ Partial |   | VEX status mapping table; sample justified statements. |
| **4.2.4** | VEX statements are versioned, timestamped, and retained as part of the product's technical documentation. | ☐ Yes   ☐ No   ☐ Partial |   | VEX archive; version control history. |
| **4.2.5** | A Safety Relevance classification is applied to components where functional safety or AI/autonomous system context applies (e.g., SRIL/SRAP framework or equivalent). | ☐ Yes   ☐ No   ☐ Partial |   | Safety relevance scoring methodology; component classification register. |

 

## **4.3 Actionable Decisions**

Defined criteria for four clear operational outcomes: Immediate Remediation, Monitored Deferral, Formal Risk Acceptance, and Escalation.

 

| Ref | Requirement | Conformant? (Yes / No / Partial) | Evidence & Rationale | Guidance / Reference |
| :---- | :---- | :---- | :---- | :---- |
| **4.3.1** | Decision criteria for Immediate Remediation are documented (e.g., CVSS ≥9.0, KEV-listed, EPSS ≥0.70, or safety-critical component affected). | ☐ Yes   ☐ No   ☐ Partial |   | Decision matrix or policy text defining remediation triggers. |
| **4.3.2** | Decision criteria for Monitored Deferral are documented, including maximum deferral window and re-assessment trigger. | ☐ Yes   ☐ No   ☐ Partial |   | Deferral SLA table; re-assessment schedule. |
| **4.3.3** | Formal Risk Acceptance requires documented business justification, risk owner sign-off, and a defined expiry date. | ☐ Yes   ☐ No   ☐ Partial |   | Risk acceptance form template; approval workflow. |
| **4.3.4** | Escalation criteria and escalation path are defined, including when legal, executive, or regulatory notification is required. | ☐ Yes   ☐ No   ☐ Partial |   | Escalation matrix; contact list with roles. |
| **4.3.5** | All four decision outcomes are tracked in a vulnerability register with current status, owner, and resolution date. | ☐ Yes   ☐ No   ☐ Partial |   | Vulnerability register schema; sample populated record. |

 

## **4.4 Disclosure & Regulatory Reporting (CRA Art. 14 Three-Stage Cascade)**

Standard operating procedures for publicly disclosing fixes, providing mitigation guidance, and meeting the three-stage CRA Article 14 regulatory reporting cascade: Early Warning (24h), Full Notification (72h), and Final Report (14 days). Items marked with DEADLINE are required before September 11, 2026\.

 

| Ref | Requirement | Conformant? (Yes / No / Partial) | Evidence & Rationale | Guidance / Reference |
| :---- | :---- | :---- | :---- | :---- |
| **4.4.1** | A security advisory process publishes fix notifications to customers and users without undue delay after a patch is available (CRA Art. 14(1)). | ☐ Yes   ☐ No   ☐ Partial |   | Advisory template; distribution channel list (CVE.org, product portal, mailing list). |
| **4.4.2** | ⚠ DEADLINE: September 11, 2026 \- Actively exploited vulnerabilities are reported to ENISA via the EU CRA Single Reporting Platform (EUVDB) within 24 hours of the organization becoming aware of active exploitation (CRA Art. 14(2)(a) Early Warning). | ☐ Yes   ☐ No   ☐ Partial |   | EUVDB submission runbook; on-call contact for ENISA platform access; test submission record. |
| **4.4.3** | ⚠ DEADLINE: September 11, 2026 \- A full vulnerability notification is submitted to EUVDB within 72 hours of the Early Warning, including severity assessment, affected versions, and interim mitigations (CRA Art. 14(2)(b) Full Notification). | ☐ Yes   ☐ No   ☐ Partial |   | Full notification template mapped to EUVDB required fields; 72-hour SLA documented in runbook. |
| **4.4.4** | ⚠ DEADLINE: September 11, 2026 \- A final report is submitted to EUVDB within 14 days after a corrective or mitigating measure becomes available, including root-cause analysis, remediation details, and disclosure timeline information (CRA Art. 14(2)(c) Final Report). | ☐ Yes   ☐ No   ☐ Partial |   | Final report template; post-incident review procedure; 14-day SLA clock definition. |
| **4.4.5** | ⚠ DEADLINE: September 11, 2026 \- Severe security incidents that impact the availability, integrity, or confidentiality of a product with digital elements are reported to ENISA via EUVDB in accordance with the same three-stage cascade as actively exploited vulnerabilities (CRA Art. 14(3)). | ☐ Yes   ☐ No   ☐ Partial |   | "Severe security incident" definition documented (aligns with NIS2 thresholds); incident triage criteria distinguishing security incidents from vulnerability reports. |
| **4.4.6** | Affected customers and users are notified without undue delay regarding actively exploited vulnerabilities or severe security incidents, including available mitigations and corrective actions (CRA Art. 14(8)). | ☐ Yes   ☐ No   ☐ Partial |   | Customer advisory template; notification runbook; mailing list, portal, or security advisory feed evidence. |
| **4.4.7** | Coordinated Vulnerability Disclosure (CVD) policy is published and covers researcher contact channel, response SLA, and safe harbor statement. A dedicated security contact channel is established with the following evidence items: (a) a dedicated security email address (security@\[domain\]) separate from general support; (b) a PGP/GPG public key published on the organization's website or a public keyserver; (c) a security.txt file per RFC 9116 at /.well-known/security.txt referencing the contact, PGP key, and policy URL; (d) the contact channel referenced in SECURITY.md for all stewarded repositories. | ☐ Yes   ☐ No   ☐ Partial |   | CVD policy URL; security.txt file at /.well-known/security.txt; PGP key URL or keyserver fingerprint; SECURITY.md excerpt showing security contact. |
| **4.4.8** | Mitigation guidance (workarounds, configuration changes) is issued when a patch is not immediately available. | ☐ Yes   ☐ No   ☐ Partial |   | Example advisory with mitigation section. |
| **4.4.9** | For non-EU-established manufacturers: the primary CSIRT recipient for Art. 14 reports has been formally identified. Where no EU establishment exists, the CSIRT is determined by where key cybersecurity decisions are made within the Union. Where this cannot be determined, the EU Authorized Representative handles CSIRT routing. This determination is documented and reviewed annually. | ☐ Yes   ☐ No   ☐ Partial |   | CSIRT routing determination memo; AR mandate clause granting CSIRT notification authority if applicable; reference to Delegated Regulation (EU) 2026/881. |
| **4.4.10** | The organization understands and has documented the precise scope of the SME fine exemption under CRA Art. 14: it covers only the financial penalty for missing the 24-hour Early Warning window \- it does NOT exempt small enterprises from the reporting obligation itself. The Art. 14 RACI (§4.5) is maintained regardless of enterprise size. | ☐ Yes   ☐ No   ☐ Partial |   | Written acknowledgement in compliance program documentation; Art. 14 RACI maintained regardless of SME status. |
| **4.4.11** | The organization is aware that under Delegated Regulation (EU) 2026/881, the receiving CSIRT may delay dissemination to other member state CSIRTs on justified cybersecurity grounds (e.g., patch expected within 72 hours; notification detail would enable exploitation). Any delay must be strictly limited, and ENISA must be informed immediately. The Art. 14 runbook references this mechanism. | ☐ Yes   ☐ No   ☐ Partial |   | Art. 14 runbook section on CSIRT dissemination delay; reference to Delegated Regulation (EU) 2026/881. |

 

## **4.5 Art. 14 Notification RACI \- Roles & Trigger Ownership**

CRA Article 14 imposes hard time-based obligations that require pre-assigned, tested role ownership. All items in this section must be completed before September 11, 2026\.

 

| Ref | Requirement | Conformant? (Yes / No / Partial) | Evidence & Rationale | Guidance / Reference |
| :---- | :---- | :---- | :---- | :---- |
| **4.5.1** | ⚠ DEADLINE: September 11, 2026 \- A named individual (by role) is designated as the Art. 14 Notification Owner responsible for initiating the Early Warning submission to EUVDB within the 24-hour clock. Given the 24-hour legal obligation operates continuously, at minimum two trained alternates must be designated (Primary, Backup, Secondary Backup or equivalent), all trained on EUVDB submission mechanics. On-call coverage must be documented for all hours including weekends and public holidays. | ☐ Yes   ☐ No   ☐ Partial |   | RACI table entry with Primary, Backup, and Secondary Backup named by role; training completion records for all three; on-call schedule showing continuous coverage. |
| **4.5.2** | ⚠ DEADLINE: September 11, 2026 \- A named individual (by role) is responsible for completing and submitting the 72-hour Full Notification to EUVDB, and is empowered to escalate to legal/executive if additional approvals are required. | ☐ Yes   ☐ No   ☐ Partial |   | RACI table entry; escalation path documented. |
| **4.5.3** | ⚠ DEADLINE: September 11, 2026 \- A named individual (by role) owns the 14-day Final Report, coordinates post-incident review inputs, and signs off on the submission. | ☐ Yes   ☐ No   ☐ Partial |   | RACI table entry; final report review workflow. |
| **4.5.4** | ⚠ DEADLINE: September 11, 2026 \- The organization has verified EUVDB account access, submission credentials, and at least one test submission prior to September 11, 2026\\. | ☐ Yes   ☐ No   ☐ Partial |   | EUVDB account registration confirmation; test submission record or screenshot. |
| **4.5.5** | ⚠ DEADLINE: September 11, 2026 \- The Art. 14 RACI is reviewed and re-confirmed upon any relevant personnel change and at minimum annually. Initial RACI must be established and reviewed before the September 11 deadline. | ☐ Yes   ☐ No   ☐ Partial |   | RACI version history; review record. |
| **4.5.6** | ⚠ DEADLINE: September 11, 2026 \- The organization conducts at least one tabletop exercise validating the 24-hour, 72-hour, and 14-day Final Report notification process end-to-end, including escalation paths and EUVDB submission mechanics, prior to the September 11 deadline. The exercise is repeated annually thereafter. | ☐ Yes   ☐ No   ☐ Partial |   | Exercise records; scenario description; lessons-learned report; follow-up action log. |

 

 

# **Section 5: Open Source Software (OSS) Stewardship**

CRA Recital 18 and Article 17 create a distinct compliance category for Open Source Software Stewards \- entities that provide OSS for integration into products placed on the EU market. This section governs how the organization engages with upstream communities and clarifies internal steward vs. maintainer boundaries.

 

## **5.1 Open Source Contribution & Engagement**

Policy for engaging with upstream open-source communities while maintaining CRA compliance, including responsible disclosure and community participation.

 

| Ref | Requirement | Conformant? (Yes / No / Partial) | Evidence & Rationale | Guidance / Reference |
| :---- | :---- | :---- | :---- | :---- |
| **5.1.1** | A documented policy governs how employees contribute to upstream open-source projects, including CLA/DCO requirements and IP assignment rules. | ☐ Yes   ☐ No   ☐ Partial |   | OSS contribution policy; CLA tool configuration. |
| **5.1.2** | Security vulnerability reports discovered during product work are responsibly disclosed to upstream maintainers before public disclosure. | ☐ Yes   ☐ No   ☐ Partial |   | Upstream disclosure procedure; example disclosure record. |
| **5.1.3** | The organization engages with relevant security SIGs or working groups (e.g., OpenSSF, CISA, CycloneDX community) to improve OSS supply chain security. | ☐ Yes   ☐ No   ☐ Partial |   | Membership records; meeting participation log; issue/PR contributions. |
| **5.1.4** | OSS dependencies are assessed for community health (maintenance status, contributor diversity, bus-factor risk) before adoption. | ☐ Yes   ☐ No   ☐ Partial |   | Dependency health assessment checklist; tooling (e.g., OSSF Scorecard). |
| **5.1.5** | A dependency approval gate exists: new OSS dependencies must complete a documented security and maintenance review before introduction into any product in CRA scope. The review must assess: (a) known vulnerability history (NVD/OSV check); (b) OSSF Scorecard result; (c) maintenance activity (last commit, release cadence, issue response time); (d) license compatibility. Approval is recorded in a PR or equivalent change-control record. | ☐ Yes   ☐ No   ☐ Partial |   | PR approval records showing dependency review completed; OSS dependency intake checklist; OSSF Scorecard output; example of a dependency rejected or conditionally accepted. |
| **5.1.6** | For any OSS project where the manufacturer vs. steward classification is non-obvious, a formal commercial-activity test has been applied using criteria from Commission guidance §3.2.3: (a) charging a fee for the software; (b) charging for technical support at rates exceeding cost recovery; (c) intending to monetize through a platform; (d) collecting personal data beyond security/compatibility/interoperability purposes; (e) accepting donations that exceed operational costs. If any criterion is met, manufacturer obligations apply. | ☐ Yes   ☐ No   ☐ Partial |   | Commercial-activity test worksheet per project; legal sign-off on borderline cases; reference to Commission draft guidance March 2026, §3.2.3. |
| **5.1.7** | The organization has a documented approach for upstream OSS components whose maintainers are not directly CRA-obligated but where the organization, as manufacturer integrating those components, bears the full compliance obligation. This includes a process for requesting SBOM artifacts, CVD policy documentation, and patch timelines from upstream projects, and for assessing integration risk for components lacking these. | ☐ Yes   ☐ No   ☐ Partial |   | Upstream due-diligence checklist; criteria for accepting/rejecting components based on security hygiene; reference to CRA Art. 13 manufacturer responsibility for third-party components. |

 

## **5.2 Steward vs. Maintainer Boundaries**

Guidelines clarifying the distinct obligations of OSS Stewards \- entities that provide OSS for integration into products placed on the EU market (CRA Art. 3(14)) \- versus individual project maintainers, and how the organization determines which role applies.

 

| Ref | Requirement | Conformant? (Yes / No / Partial) | Evidence & Rationale | Guidance / Reference |
| :---- | :---- | :---- | :---- | :---- |
| **5.2.1** | The organization has documented whether it meets the definition of an OSS Steward under CRA Article 3(14) and has recorded this determination with supporting rationale. | ☐ Yes   ☐ No   ☐ Partial |   | Legal determination memo; CRA Art. 3(14) criteria checklist. |
| **5.2.2** | For projects where the organization acts as Steward, a lightweight security policy is published meeting CRA Annex II steward requirements. | ☐ Yes   ☐ No   ☐ Partial |   | SECURITY.md or equivalent policy for each steward project. |
| **5.2.3** | Internal maintainers understand their distinct obligations vs. the organization's steward-level obligations and have received appropriate guidance. | ☐ Yes   ☐ No   ☐ Partial |   | Training or guidance document; maintainer role definition. |
| **5.2.4** | A registry of projects where the organization acts as Steward (vs. Manufacturer) is maintained and reviewed annually. | ☐ Yes   ☐ No   ☐ Partial |   | Steward registry document; review record. |

 

 

# **Section 6: Security Updates & Support Period**

CRA Article 13(2) requires manufacturers to formally document the expected support period for each product with digital elements and to provide security updates throughout that period. This section ensures the organization can define, publish, and operationalize product support lifecycles.

 

## **6.1 Support Period Definition & Update Obligations**

Processes for defining support periods, delivering security updates, and communicating product lifecycle status to customers and downstream integrators (CRA Art. 13(2)).

 

| Ref | Requirement | Conformant? (Yes / No / Partial) | Evidence & Rationale | Guidance / Reference |
| :---- | :---- | :---- | :---- | :---- |
| **6.1.1** | A documented support period (minimum 5 years unless product lifespan is demonstrably shorter) is defined and published for each product with digital elements placed on the EU market (CRA Art. 13(2)). | ☐ Yes   ☐ No   ☐ Partial |   | Product lifecycle documentation; public-facing support statement; legal justification if period is less than 5 years. |
| **6.1.2** | Security updates addressing vulnerabilities are provided without charge throughout the declared support period. | ☐ Yes   ☐ No   ☐ Partial |   | Patch management policy; release history showing security updates issued within support window. |
| **6.1.3** | A secure software update mechanism is documented, implemented, and tested including integrity verification of update packages and protection against rollback attacks. | ☐ Yes   ☐ No   ☐ Partial |   | Update architecture document; signing key management; rollback-prevention test records. |
| **6.1.4** | End-of-support dates and associated security implications (e.g., no further patches, recommended migration paths) are communicated to customers and downstream integrators with reasonable notice. | ☐ Yes   ☐ No   ☐ Partial |   | Customer communication records; EoL announcement template; advance notice timeline. |
| **6.1.5** | Where a product reaches end-of-support during an active vulnerability's remediation window, a documented escalation procedure exists to manage customer risk. | ☐ Yes   ☐ No   ☐ Partial |   | EoL vulnerability handling procedure; customer advisory template. |
| **6.1.6** | A formal End-of-Life (EOL) transition procedure is defined and published for each product. The procedure must specify: (a) minimum advance notice period for EOL announcement (recommended: 12 months for enterprise products); (b) final security patch release obligations \- at minimum, all known critical and high vulnerabilities must be patched or formally risk-accepted prior to EOL; (c) final SBOM and VEX publication upon EOL; (d) migration path or successor product guidance published to customers. EOL announcements are delivered through the same security advisory channel as vulnerability disclosures (§4.4.7). | ☐ Yes   ☐ No   ☐ Partial |   | EOL procedure document; example EOL announcement; final patch confirmation record; final SBOM artifact; migration guide or EoL advisory published to customers. |
| **6.1.7** | Where a product processes, stores, or transmits personal data or sensitive configuration, the EOL procedure includes data sanitization obligations: (a) guidance published to customers on secure data deletion or migration before EOL date; (b) where the organization operates a cloud-connected component, a documented process for decommissioning data stores and revoking API credentials upon EOL. | ☐ Yes   ☐ No   ☐ Partial |   | Data sanitization guidance published with EOL announcement; decommissioning runbook for cloud-connected components; credential revocation evidence. |

 

 

# **Section 7: Technical File & Supply Chain Sharing**

CRA Articles 13(15) and 28 require manufacturers to prepare technical documentation and make it available to market surveillance authorities (MSAs) on request. Article 13(19) requires SBOMs to accompany products. This section ensures the organization can fulfill these obligations reliably.

 

## **7.1 Market Surveillance Deliverables**

Procedures for compiling and producing technical documentation and SBOMs upon request by market surveillance authorities under CRA Art. 13(15) and Annex VII.

 

| Ref | Requirement | Conformant? (Yes / No / Partial) | Evidence & Rationale | Guidance / Reference |
| :---- | :---- | :---- | :---- | :---- |
| **7.1.1** | A Technical File is maintained for each product in scope, containing the elements required by CRA Annex VII (description, design documents, risk assessment, test reports, SBOM, declarations of conformity). | ☐ Yes   ☐ No   ☐ Partial |   | Technical File index; storage location; access control. |
| **7.1.2** | A documented cybersecurity risk assessment is maintained and updated throughout the product lifecycle, covering identified threats, attack surfaces, likelihood, impact, and mitigating controls (CRA Annex VII). The risk assessment must specify: (a) the methodology used (acceptable methods: ISO 27005, STRIDE, Attack Trees, OCTAVE, or NIST 800-30); (b) the scoring model applied for likelihood and impact determination; (c) review frequency (at minimum annually and upon significant product change). | ☐ Yes   ☐ No   ☐ Partial |   | Risk assessment report referencing named methodology; threat model document; scoring model definition; update history showing assessment reviewed at each major release. |
| **7.1.3** | The Technical File is accessible to designated personnel and can be produced to an MSA within the legally required timeframe. | ☐ Yes   ☐ No   ☐ Partial |   | File retrieval SLA; named custodian. |
| **7.1.4** | SBOMs included in the Technical File are the same machine-readable artifacts generated by the CI/CD pipeline (no manual transcription). | ☐ Yes   ☐ No   ☐ Partial |   | Pipeline artifact link to Technical File storage. |
| **7.1.5** | Technical documentation is retained for at least 10 years after placement on the market, or for the expected product lifetime / support period if longer (CRA Art. 13(15)). | ☐ Yes   ☐ No   ☐ Partial |   | Retention policy; archive location; destruction schedule. |
| **7.1.6** | A documented workflow exists for responding to requests from Market Surveillance Authorities (MSAs). The workflow must specify: (a) named Technical File custodian responsible for MSA engagement; (b) escalation path to legal counsel and executive; (c) a documented organizational SLA for producing Technical File artifacts upon MSA request \- the organization shall respond within 5 business days unless a shorter period is legally required; (d) log of any prior MSA interactions. | ☐ Yes   ☐ No   ☐ Partial |   | MSA response runbook; escalation matrix with named contacts; Technical File retrieval SLA documented as a binding internal commitment; MSA interaction log (or statement confirming no prior interactions). |

 

## **7.2 Downstream & Customer Provisioning**

Delivering accurate, timely security and SBOM documentation to customers and integrators alongside binary or source delivery.

 

| Ref | Requirement | Conformant? (Yes / No / Partial) | Evidence & Rationale | Guidance / Reference |
| :---- | :---- | :---- | :---- | :---- |
| **7.2.1** | SBOMs are made available to customers and integrators alongside each product release (binary or source delivery). | ☐ Yes   ☐ No   ☐ Partial |   | SBOM delivery mechanism (portal, API, package metadata, attestation). |
| **7.2.2** | Security advisories and VEX statements are delivered to downstream integrators through a documented channel. | ☐ Yes   ☐ No   ☐ Partial |   | Advisory distribution list; portal URL; API endpoint. |
| **7.2.3** | Contractual or technical mechanisms ensure downstream integrators receive timely security updates for embedded components. | ☐ Yes   ☐ No   ☐ Partial |   | Contract clause or SLA; notification mechanism. |
| **7.2.4** | A process exists to handle customer requests for additional SBOM detail or vulnerability information within a defined SLA. | ☐ Yes   ☐ No   ☐ Partial |   | Customer-facing SBOM request procedure; support ticket template. |
| **7.2.5** | Where SBOM and VEX artifacts are distributed via automated feeds or APIs, telemetry validation criteria are defined and monitored: (a) feed availability SLA (recommended: 99.5% uptime); (b) schema validation \- machine-readable artifacts are validated against the declared SPDX or CycloneDX schema version before publication; (c) latency SLA \- VEX updates are published to the feed within a defined window of triage completion (recommended: 24 hours); (d) consumer confirmation \- at least one downstream validation check confirms artifacts are parseable by a reference consumer tool. For organizations distributing only via portal or manual request, this item is N/A \- documented as such. | ☐ Yes   ☐ No   ☐ Partial |   | Feed monitoring dashboard or uptime log; schema validation CI gate output; VEX publication latency metric (cross-reference §4.1.8(e)); consumer validation test record; N/A declaration for non-automated distribution. |

 

## **7.3 EU Declaration of Conformity & CE Marking (CRA Art. 28 & 30\)**

To legally place products on the EU market under CRA, manufacturers must draft an EU DoC aligned with Annex V and affix the CE marking. For software-only products distributed digitally, a digital CE marking accessible on the product website satisfies the affixing requirement.

 

| Ref | Requirement | Conformant? (Yes / No / Partial) | Evidence & Rationale | Guidance / Reference |
| :---- | :---- | :---- | :---- | :---- |
| **7.3.1** | An EU Declaration of Conformity (DoC) is drafted for each in-scope product in accordance with CRA Annex V. The DoC must include at minimum: (a) manufacturer name and address; (b) product name, type, and version identifier; (c) statement that the product meets CRA essential requirements (Annex I); (d) reference to the conformity assessment procedure used (Module A self-certification, or Notified Body procedure with body name and certificate number); (e) reference to any harmonized standards applied; (f) place and date of issue; (g) name and signature of authorized signatory. A DoC template pre-populated with the required Annex V structure is maintained and used for each new product. | ☐ Yes   ☐ No   ☐ Partial |   | Completed EU DoC per Annex V for each in-scope product; DoC template document; legal review sign-off. |
| **7.3.2** | The EU DoC is kept up-to-date throughout the product lifetime and updated upon any significant product change that affects the conformity assessment basis. A documented DoC change control procedure defines what triggers a DoC update, who approves it, and how the superseded version is archived. | ☐ Yes   ☐ No   ☐ Partial |   | DoC version history; change control procedure; approval record for each DoC revision. |
| **7.3.3** | The CE marking (or, for software-only products distributed digitally, an equivalent digital CE marking accessible on the product website) is affixed to the product and its packaging or accompanying documentation before EU market placement (CRA Art. 30). | ☐ Yes   ☐ No   ☐ Partial |   | CE mark placement evidence (screenshot, label photograph, or packaging proof); digital CE mark URL. |
| **7.3.4** | The EU DoC is made available to market surveillance authorities and customers on request and is retained for at least 10 years after last placement on the EU market. | ☐ Yes   ☐ No   ☐ Partial |   | DoC storage location; access control; retention policy entry. |

 

## **7.4 EU Authorized Representative (CRA Art. 22 / 25\)**

If a manufacturer is not established in the EU, it must ensure that one of the following is in place before placing any product on the EU market: (a) an appointed EU Authorized Representative (AR) under CRA Art. 22/25; (b) an EU-based importer who places the product on the market; or (c) an EU-based fulfillment service provider acting under a written mandate. An Authorized Representative is not the only option \- but one of these three must be in place. Items 7.4.2-7.4.5 apply only where the AR route is chosen; mark N/A with documented rationale if using the importer or fulfillment provider route instead.

 

| Ref | Requirement | Conformant? (Yes / No / Partial) | Evidence & Rationale | Guidance / Reference |
| :---- | :---- | :---- | :---- | :---- |
| **7.4.1** | The organization has determined whether it qualifies as a "manufacturer" under CRA Art. 3(13) with an EU establishment. If not EU-established, an Authorized Representative must be appointed before market placement. | ☐ Yes   ☐ No   ☐ Partial |   | Legal determination memo; registration address or EU establishment confirmation. |
| **7.4.2** | Where the organization is not established in the EU, a written mandate appointing an EU Authorized Representative (CRA Art. 22 / 25\) is executed before placing any product on the EU market. The mandate must specify: (a) the scope of products covered; (b) the AR's authority to act on behalf of the manufacturer with MSAs; (c) the AR's obligation to maintain a copy of the Technical File and DoC; (d) conditions for mandate termination and transition procedure if the AR relationship ends. | ☐ Yes   ☐ No   ☐ Partial |   | Signed AR mandate covering all required scope elements; legal review sign-off; mandate renewal or review schedule. |
| **7.4.3** | The Authorized Representative's name, address, and contact details are included on the product, its packaging, or accompanying documentation as required by CRA Art. 25\\. | ☐ Yes   ☐ No   ☐ Partial |   | Product label or documentation showing AR details. |
| **7.4.4** | The Authorized Representative is provided with a copy of the EU DoC and Technical File and is empowered to act on behalf of the manufacturer in dealings with market surveillance authorities. | ☐ Yes   ☐ No   ☐ Partial |   | Document transmission record; access confirmation from AR. |
| **7.4.5** | Operational procedures govern the ongoing AR relationship: (a) the AR is notified within 48 hours of any Art. 14 reportable event (actively exploited vulnerability or severe security incident) so the AR can fulfill any MSA notification duties; (b) the AR receives updated DoC and Technical File artifacts within 5 business days of any product update that triggers a DoC revision; (c) the AR relationship is reviewed annually to confirm the AR remains active, appropriately resourced, and the mandate remains current. | ☐ Yes   ☐ No   ☐ Partial |   | AR notification procedure with 48-hour SLA; document delivery log showing Technical File updates sent to AR; annual AR relationship review record. |

 

 

# **Section 8: Cross-Framework Integration**

The CRA sits within a broader EU digital regulatory stack. Organizations treating CRA compliance as a standalone exercise will duplicate work across NIS2, the AI Act, DORA, and the Data Act. This section ensures the organization identifies where CRA conformity artifacts serve multiple regulatory obligations simultaneously.

 

## **8.1 CRA and NIS2**

 

| Ref | Requirement | Conformant? (Yes / No / Partial) | Evidence & Rationale | Guidance / Reference |
| :---- | :---- | :---- | :---- | :---- |
| **8.1.1** | The organization has determined whether it is subject to NIS2 (Directive (EU) 2022/2555) as an essential or important entity independently of its CRA manufacturer obligations. Where both apply, a mapping exists showing how CRA product security artifacts (DoC, SBOM, vulnerability handling records) satisfy NIS2 supply chain security assessment requirements (NIS2 Art. 21(2)(d)). | ☐ Yes   ☐ No   ☐ Partial |   | Dual-framework mapping document; NIS2 supply chain security procedure referencing CRA conformity artifacts as evidence. |
| **8.1.2** | For organizations subject to both NIS2 and CRA: governance, risk assessment, and incident response processes have been designed to serve both frameworks on shared rather than parallel tracks where the underlying obligation is equivalent. | ☐ Yes   ☐ No   ☐ Partial |   | Integrated GRC framework document; evidence that NIS2 incident reporting and CRA Art. 14 notification runbooks share escalation paths and RACI roles where appropriate. |

 

## **8.2 CRA and AI Act**

 

| Ref | Requirement | Conformant? (Yes / No / Partial) | Evidence & Rationale | Guidance / Reference |
| :---- | :---- | :---- | :---- | :---- |
| **8.2.1** | For any product that is both a PDE under CRA and a high-risk AI system under the AI Act (Regulation (EU) 2024/1689): the organization has documented that CRA Annex I compliance satisfies the AI Act Art. 15 cybersecurity requirements for that product, per CRA Art. 12\\. | ☐ Yes   ☐ No   ☐ Partial |   | AI Act / CRA dual-scope determination per product; mapping from CRA Annex I to AI Act Art. 15; reference to CRA Art. 12\\. |
| **8.2.2** | For Important or Critical CRA products that are also high-risk AI systems: CRA conformity assessment requirements take precedence over AI Act internal control provisions for cybersecurity aspects (per CRA Art. 12 interaction). This precedence is documented in the product conformity assessment plan. | ☐ Yes   ☐ No   ☐ Partial |   | Precedence determination in conformity assessment plan; legal review sign-off on the CRA / AI Act interaction. |

 

## **8.3 CRA and DORA**

 

| Ref | Requirement | Conformant? (Yes / No / Partial) | Evidence & Rationale | Guidance / Reference |
| :---- | :---- | :---- | :---- | :---- |
| **8.3.1** | For organizations supplying digital products to financial entities subject to DORA (Regulation (EU) 2022/2554): CRA conformity documentation (Technical File, DoC, SBOM, vulnerability handling SLAs) has been identified as relevant input to DORA ICT third-party risk management due diligence and is made available to financial entity customers on request. | ☐ Yes   ☐ No   ☐ Partial |   | Customer-facing documentation list including DORA-relevant CRA artifacts; reference to DORA Art. 28-30. |

 

## **8.4 CRA and Data Act**

 

| Ref | Requirement | Conformant? (Yes / No / Partial) | Evidence & Rationale | Guidance / Reference |
| :---- | :---- | :---- | :---- | :---- |
| **8.4.1** | For connected products that simultaneously qualify under the Data Act (Regulation (EU) 2023/2854): overlapping obligations around data access, documentation, and user transparency have been identified, and the compliance program addresses both regulations in a coordinated manner. | ☐ Yes   ☐ No   ☐ Partial |   | Data Act / CRA product scope overlap assessment; coordinated documentation plan covering CRA Technical File and Data Act Art. 3 data access obligations. |

 

 

# **Section 9: Procurement & Buyer-Side Obligations**

The CRA does not create direct compliance obligations for enterprise buyers, but it changes what responsible procurement looks like. For organizations also subject to NIS2 as essential or important entities, these questions are simultaneously regulatory requirements.

 

## **9.1 Vendor CRA Qualification**

 

| Ref | Requirement | Conformant? (Yes / No / Partial) | Evidence & Rationale | Guidance / Reference |
| :---- | :---- | :---- | :---- | :---- |
| **9.1.1** | The vendor evaluation process requires suppliers of products with digital elements to confirm: (a) the CRA product classification (Default / Class I / Class II / Critical); (b) the conformity pathway used and, where applicable, the notified body engaged; (c) the declared support period end date. | ☐ Yes   ☐ No   ☐ Partial |   | Updated vendor questionnaire or RFP template; example completed vendor response. |
| **9.1.2** | Procurement contracts for products with digital elements include at minimum: (a) CRA conformity confirmation; (b) commitment to maintain vulnerability handling for the declared support period; (c) notification obligation to the buyer upon discovery of an actively exploited vulnerability in a supplied product; (d) access to Technical File / DoC on request. | ☐ Yes   ☐ No   ☐ Partial |   | Updated standard contract template with CRA clauses; legal review sign-off. |
| **9.1.3** | The organization asks suppliers whether they produce SBOMs for procured products, in what format, and whether they are available to customers. For high-assurance procurement (especially environments covered by NIS2 or DORA), SBOM availability is a mandatory procurement criterion. | ☐ Yes   ☐ No   ☐ Partial |   | Supplier SBOM availability requirement in procurement policy; evidence of SBOM receipt or supplier declaration for high-assurance products. |
| **9.1.4** | The organization verifies that suppliers have credible infrastructure to meet the September 2026 24-hour vulnerability reporting obligation \- specifically, the ability to detect actively exploited vulnerabilities within shipped components within 24 hours. A supplier unable to articulate this is treated as a conformity signal. | ☐ Yes   ☐ No   ☐ Partial |   | Supplier due-diligence question on Sept 2026 monitoring capability; documented assessment outcome per supplier. |
| **9.1.5** | Suppliers of products with digital elements are classified into risk tiers based on product criticality, market exposure, and data sensitivity. At minimum three tiers are defined: Tier 1 (Critical \- direct integration into CRA-scope products, high attack surface or safety relevance); Tier 2 (Significant \- indirect integration or moderate exposure); Tier 3 (Standard \- commodity or low-criticality components). Due-diligence depth, contract requirements, and monitoring frequency are calibrated to tier. This tiering also supports NIS2 supply chain security obligations (§8.1) and DORA ICT third-party risk management (§8.3). | ☐ Yes   ☐ No   ☐ Partial |   | Supplier tiering policy; tiered vendor register with classification rationale; tiered due-diligence checklist showing differentiated requirements per tier; example of a Tier 1 supplier assessment vs. Tier 3\. |

 

 

# **Implementation Roadmap**

The following phased model provides a structured approach to achieving self-certification. Organizations should scope Phase 1 narrowly (e.g., one product line) and expand incrementally.

 

| Phase | Key Action | Typical Owner | Target |
| :---- | :---- | :---- | :---- |
| **PRIORITY \- Art. 14 RACI (§4.4-4.5)** | Register EUVDB account; assign named owners for 24h / 72h / 14-day notification stages; document "severe security incident" definition; complete at least one test submission through the ENISA reporting platform before the deadline. |   | **Before Sep 11, 2026 \- IMMEDIATE** |
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

 

Community contribution: If you have mapped additional ISO/IEC 18974 clauses, OWASP SAMM practices, OpenSSF guides, or Eclipse ORC resources to this checklist, please contribute via GitHub pull request or Google Doc comment. Roman Zhukov (OpenSSF GCP) and Eclipse ORC have offered to contribute implementation guidance for specific sections.

 

 

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

