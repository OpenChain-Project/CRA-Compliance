<p align="center">
  <img src="https://raw.githubusercontent.com/OpenChain-Project/Image-Assets/master/Official/Project-Logo/Long-Logo/long-logo.png" alt="OpenChain Project" width="360">
</p>

# **Cyber Resilience Act (CRA) Compliance Requirements & Checklist**

OpenChain-Aligned Self-Certification Document  
ISO/IEC 18974 Aligned | EU Regulation 2024/2847 | OpenChain ISO/IEC 5230  
Version: RC1 | Date: 19 Aug 2026 | Status: Release Candidate  
Document Owner / OpenChain CRA Working Group Chair: Devashri Datta  
License: CC-BY-4.0

OpenChain page: [openchainproject.org/cracompliance](https://openchainproject.org/cracompliance)  
GitHub: [github.com/OpenChain-Project/CRA-Compliance](https://github.com/OpenChain-Project/CRA-Compliance)  
Community comments: [Google Doc (open for comments)](https://docs.google.com/document/d/1Wog28BZ9NQhY3tN9Wc2NDml2phBDuvYu9zkXSON5z5o/edit?usp=sharing)

Supporting evidence and project history:

* [Contributors and Reviewers](CONTRIBUTORS.md)
* [Revision History](REVISION_HISTORY.md)
* [External References and Adoption](ANNEX_D_EXTERNAL_REFERENCES_AND_ADOPTION.md)

Completing or signing this checklist does not in itself constitute a CRA conformity assessment, an EU Declaration of Conformity, or evidence of lawful CE marking. This document is a readiness and evidence-management tool supporting the applicable conformity-assessment procedure. This document does not constitute legal advice; consult qualified legal counsel before formal regulatory submission.

Important: All bracketed \[INSERT ...\] fields throughout this document must be completed with organization-specific information before any compliance claim or self-certification is made.


# **Section 1: Introduction & Scope**

CRA applicability is not determined solely by whether an organization deploys open-source software in the EU. The primary scope question is whether the organization makes a product with digital elements available on the Union market, or otherwise has a role covered by the CRA, such as manufacturer, importer, distributor, authorised representative, or open-source software steward.

If an organization does not make products with digital elements available on the Union market and does not have a covered CRA role, this checklist is not a legal compliance obligation for that organization. Such organizations may still use it as a voluntary reference for understanding SBOMs, vulnerability handling, evidence management, and software supply chain readiness.

This document defines an OpenChain-aligned organizational compliance framework for the EU Cyber Resilience Act (CRA, Regulation (EU) 2024/2847) and ISO/IEC 18974. It provides a self-certification checklist covering governance, SBOM quality, vulnerability handling, regulatory reporting, OSS stewardship, and technical-file obligations.

The CRA (Regulation (EU) 2024/2847) establishes mandatory cybersecurity requirements for products with digital elements (PDEs) placed on the EU market. The following role definitions are drawn from CRA Art. 3:

 

**Role definitions (CRA Art. 3):**

●  Manufacturer (Art. 3(13)): a natural or legal person who develops or manufactures a PDE, or has a PDE designed or manufactured, and markets it under their name or trademark, whether for payment, free of charge, or as a monetary revenue-generating service.

●  Importer (Art. 3(16)): a natural or legal person established in the Union who places on the market a PDE bearing the name or trademark of a natural or legal person established outside the Union.

●  Distributor (Art. 3(17)): a natural or legal person in the supply chain, other than the manufacturer or importer, that makes a PDE available on the Union market.

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
| **§2.5-2.7 Product Assessment** | Required | Verify evidence / Art. 21 if applicable | Verify evidence / Art. 21 if applicable | N/A | Required | Importers/distributors verify manufacturer conformity evidence unless Article 21 makes them manufacturers; stewards are not manufacturers, so conformity assessment does not apply. |
| **§3.1-3.4 SBOM & SDLC** | Required | N/A | N/A | N/A | Required | Manufacturer builds the product |
| **§3.5 Importer/Distributor** | N/A | Required | Required | See note\* | N/A | \*Art. 24 may bring stewards into scope depending on activities |
| **§3.6 Third-Party Software Qualification** | Required | Verify evidence / Art. 21 if applicable | Verify evidence / Art. 21 if applicable | Recommended | Required | Manufacturer qualifies third-party software sources beyond OSS; importers/distributors verify evidence unless Article 21 makes them manufacturers |
| **§4 Vuln Handling** | Required | Inform manufacturer; Art. 21 if applicable | Inform manufacturer; Art. 21 if applicable | Partial (see note\*\*) | Required | Importers/distributors must inform the manufacturer without undue delay when they become aware of vulnerabilities; Articles 13/14 apply directly if Article 21 makes them manufacturers. Art. 14(1) applies where steward is involved in development; Art. 14(3) and 14(8) apply where severe incidents affect network/information systems provided by the steward |
| **§5 OSS Stewardship** | Optional | Optional | Optional | Required | Required | Core for steward role |
| **§6 Support Period** | Required | N/A | N/A | N/A | Required | Manufacturer sets support period |
| **§7.1-7.4 Technical File** | Required | Verify only | Verify only | N/A | Required | Importers check, not produce |
| **§8 Cross-Framework** | As applicable | As applicable | As applicable | N/A | As applicable | Based on NIS2/DORA/AI Act scope |
| **§9 Procurement** | Optional | Optional | Optional | N/A | Optional | Buyer-side obligation |

 

Note on OSS Steward column: "Optional" indicates the section is not typically required by CRA obligations for stewards but may be adopted voluntarily. "Recommended" indicates good practice. OSS Stewards must put in place and document, in a verifiable manner, a cybersecurity policy supporting secure development and vulnerability handling (CRA Art. 24(1)). Note: under Art. 24, stewards may also fall within scope of §3.5 importer/distributor obligations depending on their activities. For Section 4 (Vulnerability Handling), Art. 14(1) applies to stewards to the extent they are involved in development; Art. 14(3) and 14(8) apply where severe incidents affect network and information systems provided by the steward for development of the relevant FOSS.

 

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
| **3.6** | Third-Party Software Supply Chain Qualification | No | Yes \- 11 Dec 2027 | Partial \- supplier governance supports supply chain risk management |
| **4.1** | Vulnerability Ingestion & Monitoring | Yes \- EUVD/KEV feeds required | No | Yes \- §3.3.1 |
| **4.2** | Risk Adjudication & Vulnerability Exchange | Yes \- exploitability informs Art. 14 | No | Yes \- §3.3.2 |
| **4.3** | Actionable Decisions | Yes \- decisions trigger Art. 14 clock | No | Yes \- §3.3.2 |
| **4.4** | Disclosure & Regulatory Reporting | **YES \- §4.4.2-4.4.5 11 Sep 2026** | No | Partial \- CVD only; ENISA cascade not in 18974 |
| **4.5** | Art. 14 Notification RACI | **YES \- all items 11 Sep 2026** | No | No \- CRA Art. 14 specific |
| **5.1** | OSS Contribution & Engagement | No | Yes \- 11 Dec 2027 | Partial \- §3.1.1 |
| **5.2** | Steward vs. Maintainer Boundaries | No | Yes \- 11 Dec 2027 | No \- CRA Steward concept not in 18974 |
| **5.3** | Self-Maintained Open Source Software | No | Yes \- 11 Dec 2027 | Partial \- supports OSS lifecycle governance |
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

   
**Important: All bracketed \[INSERT ...\] fields throughout this document must be completed with organization-specific information before any compliance claim or self-certification is made. Completion or signature of this checklist does not, by itself, establish CRA conformity. Conformity depends on completion of the applicable conformity-assessment procedure and the associated technical documentation, EU Declaration of Conformity, and CE-marking obligations.**

 

# **Section 2: Program Architecture & Governance**

This section establishes the organizational foundation for CRA compliance. Note: §2.1-2.4 apply to all roles including Stewards (as Recommended). §2.5 and §2.7 apply only to Manufacturers and Importers/Distributors; they are N/A for OSS Stewards.

 

## **2.1 CRA Policy**

A documented cybersecurity policy for CRA compliance defines the organization commitment and obligations. Note: §2.1 is targeted primarily at Manufacturers. The policy obligations for OSS Stewards are lighter and governed by CRA Art. 24 and Annex II.

 

| Ref | Requirement | Conformant? (Yes / No / Partial) | Evidence & Rationale | Guidance / Reference |
| :---- | :---- | :---- | :---- | :---- |
| **2.1.1** | \[CRA REQUIREMENT\] The organization must maintain a documented cybersecurity policy for CRA compliance. The policy should be formally approved by senior management or an equivalent governing body. | ☐ Yes   ☐ No   ☐ Partial |   | Policy document; approval signature or board/exec minute. |
| **2.1.2** | \[GOOD PRACTICE\] The policy should be published and accessible to all relevant personnel. Per CRA Recital 76, manufacturers are encouraged to make their security policies publicly available, including in machine-readable format. | ☐ Yes   ☐ No   ☐ Partial |   | URL or intranet link; screenshot or acknowledgement log. |
| **2.1.3** | \[CRA REQUIREMENT\] The policy must explicitly reference the organization's obligations under CRA Articles 13, 14, and 15 and Annex I Part II(5), which requires a policy on coordinated vulnerability disclosure. This is further detailed in Art. 13(8). PT3 additionally recommends a standalone vulnerability handling policy. | ☐ Yes   ☐ No   ☐ Partial |   | Policy text mapped to CRA articles. |
| **2.1.4** | \[CRA REQUIREMENT\] The policy must cover the full product lifecycle: design, development, release, m aintenance, and end-of-support, consistent with the product lifetime obligations in CRA Art. 13(2) and the vulnerability handling obligations in Art. 13(6). | ☐ Yes   ☐ No   ☐ Partial |   | Lifecycle phase coverage section in policy. |

 

## **2.2 Roles & Responsibilities**

Clear assignment of CRA compliance responsibilities across the organization.

 

| Ref | Requirement | Conformant? (Yes / No / Partial) | Evidence & Rationale | Guidance / Reference |
| :---- | :---- | :---- | :---- | :---- |
| **2.2.1** | \[CRA REQUIREMENT\] The organization must designate a named individual or function with documented authority over CRA compliance program decisions. | ☐ Yes   ☐ No   ☐ Partial |   | RACI chart or org chart with role highlighted. |
| **2.2.2** | \[CRA REQUIREMENT\] Legal or regulatory counsel must have a defined role for interpreting CRA obligations, essential requirements, and regulatory changes. | ☐ Yes   ☐ No   ☐ Partial |   | Legal review sign-off records. |
| **2.2.3** | \[GOOD PRACTICE\] The organization should assign responsibility for SBOM generation, dependency management, and secure-by-design requirements. This may be assigned to a product engineering function or equivalent.  | ☐ Yes   ☐ No   ☐ Partial |   | Ticket/backlog owner assignments; job description excerpts. |
| **2.2.4** | \[GOOD PRACTICE\] The organization should assign responsibility for vulnerability monitoring, exploitability assessment, and security incident response activities required under CRA. These responsibilities may be distributed across functions as appropriate to the organization's size and structure. | ☐ Yes   ☐ No   ☐ Partial |   | SecOps runbook referencing CRA. |
| **2.2.5** | \[GOOD PRACTICE\] Role assignments should be reviewed and updated at least annually or upon significant organizational change. | ☐ Yes   ☐ No   ☐ Partial |   | Change-log or version history of the RACI document. |

 

## **2.3 Competence & Training**

Requirements for ensuring personnel dealing with CRA compliance, SBOMs, and vulnerability handling maintain current knowledge.

 

| Ref | Requirement | Conformant? (Yes / No / Partial) | Evidence & Rationale | Guidance / Reference |
| :---- | :---- | :---- | :---- | :---- |
| **2.3.1** | \[GOOD PRACTICE\] The organization should define a training curriculum covering CRA obligations, SBOM tooling, and vulnerability handling. | ☐ Yes   ☐ No   ☐ Partial |   | Training plan document; LMS catalog entry. |
| **2.3.2** | \[GOOD PRACTICE\] Personnel with CRA compliance responsibilities should complete required training within a defined review cycle. | ☐ Yes   ☐ No   ☐ Partial |   | Training completion records; LMS export. |
| **2.3.3** | \[GOOD PRACTICE\] Competence requirements (knowledge, skills, experience) should be documented for each CRA-relevant role. | ☐ Yes   ☐ No   ☐ Partial |   | Role competency matrix. |
| **2.3.4** | \[GOOD PRACTICE\] A mechanism should exist to keep training current as CRA implementing acts and harmonized standards evolve. | ☐ Yes   ☐ No   ☐ Partial |   | Curriculum review schedule; owner assignment. |

 

## **2.4 Sustainability & Review**

Periodic review processes to ensure CRA compliance mechanisms remain active and up-to-date across release cycles. This subsection also covers compliance exception management (§2.4.6-2.4.8).

 

| Ref | Requirement | Conformant? (Yes / No / Partial) | Evidence & Rationale | Guidance / Reference |
| :---- | :---- | :---- | :---- | :---- |
| **2.4.1** | \[GOOD PRACTICE\] The CRA compliance program should be reviewed at least once per calendar year. | ☐ Yes   ☐ No   ☐ Partial |   | Review meeting minutes or audit report dated within 12 months. |
| **2.4.2** | \[GOOD PRACTICE\] Reviews should be triggered by major product releases, significant dependency changes, or changes to regulatory guidance. | ☐ Yes   ☐ No   ☐ Partial |   | Event-driven review trigger list in governance document. |
| **2.4.3** | \[GOOD PRACTICE\] Review outcomes should be formally recorded and assigned to responsible owners with target resolution dates. | ☐ Yes   ☐ No   ☐ Partial |   | Issue tracker or action log with owner and due date fields. |
| **2.4.4** | \[CRA REQUIREMENT\] The organization must maintain a process to retire or archive compliance records for end-of-life products. Technical documentation must be retained for at least 10 years after market placement, or for the duration of the support period or end of support, whichever is longer (CRA Art. 13(13)). | ☐ Yes   ☐ No   ☐ Partial |   | EoL / archival procedure documentation. |
| **2.4.5** | \[GOOD PRACTICE\] The organization should conduct periodic internal audits of CRA compliance program effectiveness. | ☐ Yes   ☐ No   ☐ Partial |   | Internal audit plan; audit report; finding tracker. |
| **2.4.6** | \[GOOD PRACTICE\] A compliance exception register should be maintained to document temporary deviations from controls, including rationale and expiry. | ☐ Yes   ☐ No   ☐ Partial |   | Exception register template; approval workflow. |
| **2.4.7** | \[GOOD PRACTICE\] Each exception should be assigned a risk owner, a compensating control, and a defined review date. | ☐ Yes   ☐ No   ☐ Partial |   | Exception record with owner, compensating control, and expiry date. |
| **2.4.8** | \[GOOD PRACTICE\] Expired exceptions should be reviewed and either resolved, renewed with updated justification, or escalated. | ☐ Yes   ☐ No   ☐ Partial |   | Exception renewal procedure; escalation log. |

 

## **2.5 Product Risk Categorization & Conformity Assessment Route**

Before executing self-certification, the organization must determine the CRA product classification per CRA Art. 6, 24, and 32 and Annexes III-IV. Technical descriptions of product categories are specified in Implementing Regulation (EU) 2025/2392. Self-certification (Module A, per CRA Annex VIII Part 1\) is only lawful for Default products and certain Class I products using harmonized standards. Art. 32(5) provides an additional pathway for FOSS manufacturers; see item 2.5.9. Note: §2.5 and §2.7 are N/A for OSS Stewards.

 

| Ref | Requirement | Conformant? (Yes / No / Partial) | Evidence & Rationale | Guidance / Reference |
| :---- | :---- | :---- | :---- | :---- |
| **2.5.1** | \[CRA REQUIREMENT\] The organization must document whether each in-scope product constitutes a product with digital elements (PDE) under CRA Art. 3(1), distinguishing it from standalone SaaS excluded under Recital 12\. Products whose primary function is remote data processing for a PDE are in CRA scope; standalone SaaS not providing such processing falls under NIS2, not CRA. | ☐ Yes   ☐ No   ☐ Partial |   | Scope determination memo referencing Recital 12 and Commission guidance C(2026) 5252; product-by-product classification table. |
| **2.5.2** | \[CRA REQUIREMENT\] Before selecting a conformity pathway, the organization must determine whether it has an EU establishment. If the manufacturer is not EU-established, the need for an EU-established responsible economic operator must be confirmed through product-specific legal analysis under applicable Union harmonisation legislation, including Regulation (EU) 2019/1020 Article 4 where applicable. CRA Article 18 permits appointment of an EU authorised representative by written mandate but does not impose that appointment as a blanket requirement. Cross-reference §7.4. | ☐ Yes   ☐ No   ☐ Partial |   | EU establishment confirmation or, where applicable, signed AR mandate, importer agreement, or fulfillment provider contract. |
| **2.5.3** | \[CRA REQUIREMENT\] The organization must formally evaluate each in-scope product against CRA Annex III (Important Class I and II) and Annex IV (Critical) and record a product classification decision with supporting rationale. The technical descriptions of product categories are specified in Implementing Regulation (EU) 2025/2392. | ☐ Yes   ☐ No   ☐ Partial |   | Classification register with product name, classification outcome, and decision date. Reference: CRA Annex III, Annex IV, and Implementing Regulation (EU) 2025/2392 (eur-lex.europa.eu/legal-content/EN/TXT/?uri=CELEX:32025R2392). |
| **2.5.4** | \[CRA REQUIREMENT\] For Default products, the organization may use self-certification (Internal Control \- Module A, per CRA Annex VIII Part 1\) provided the assessment basis is documented. Art. 32(5) provides an additional pathway for manufacturers of products qualifying as FOSS under the commercial-activity test; legal counsel should be consulted on applicability. | ☐ Yes   ☐ No   ☐ Partial |   | Self-assessment record referencing applicable harmonized standard or essential requirements mapped to design. Reference: CRA Annex VIII Part 1 for Module A procedure. |
| **2.5.5** | \[CRA REQUIREMENT\] For Important Class I products, the organization must either: (a) apply a harmonized standard in full and use self-certification, or (b) engage a Notified Body. The decision must be documented and justified. | ☐ Yes   ☐ No   ☐ Partial |   | Notified Body engagement letter OR harmonized standard coverage analysis; classification rationale memo. |
| **2.5.6** | \[CRA REQUIREMENT\] For Important Class II or Critical products, the organization must engage a Notified Body assessment or European Cybersecurity Certification Scheme and track it to completion before EU market placement. | ☐ Yes   ☐ No   ☐ Partial |   | Notified Body contract; assessment status; EU type-examination certificate where required. |
| **2.5.7** | \[CRA REQUIREMENT\] Product classification must be reviewed upon any substantial modification (as defined in CRA Art. 3(30)) or other relevant change that may affect conformity. Annual review may be retained as a good-practice governance cadence. A substantial modification may change the product classification and trigger a new conformity assessment obligation. | ☐ Yes   ☐ No   ☐ Partial |   | Classification review log; change-triggered review records. |
| **2.5.8** | \[GOOD PRACTICE\] The organization should maintain a documented classification decision procedure to ensure consistent classification of new products and substantial modifications. While not explicitly required by CRA text, this procedure supports demonstrable compliance with the classification obligations in Art. 6 and Art. 32\. | ☐ Yes   ☐ No   ☐ Partial |   | Classification decision procedure; examples of classification decisions applied. |
| **2.5.9** | \[CRA REQUIREMENT\] For manufacturers of products qualifying as Free and Open Source Software (FOSS) under the commercial-activity test (§5.1.5), Art. 32(5) allows qualifying Annex III FOSS products to demonstrate conformity by using one of the procedures referred to in Art. 32(1), provided that the technical documentation referred to in Art. 31 is publicly available at market placement. The organization must determine whether this pathway applies and document the determination with legal rationale. | ☐ Yes   ☐ No   ☐ Partial |   | Legal determination memo on Art. 32(5) applicability; reference to Commission guidance C(2026) 5252 on commercial-activity test criteria. |

 

## **2.6 Cybersecurity Risk Assessment (CRA Art. 13(2)–(4))**

\[CRA REQUIREMENT\] The manufacturer must perform and document a cybersecurity risk assessment for each product with digital elements, taking into account the intended purpose, reasonably foreseeable use, operating environment, and foreseeable risks across the product lifecycle.

The cybersecurity risk assessment determines which CRA Annex I essential cybersecurity requirements apply and how those requirements are addressed. This section is distinct from §2.5: §2.5 determines the product's CRA classification and conformity-assessment route under CRA Art. 6, Art. 32, and Annexes III-IV, while §2.6 determines which requirements apply and how.

Art. 13(5) due diligence for third-party and FOSS components is addressed in §3 and §5. This section is not applicable to OSS Stewards unless the steward also qualifies as the manufacturer for the relevant product or activity.

## **2.7 Harmonized Standards Tracking**

CRA conformity depends on harmonized standards under Standardisation Request M/606, developed by ETSI, CEN, and CENELEC. As of August 2026, PT1 and PT3 drafts have been updated significantly since their public inquiry versions; final versions are not yet publicly available but are expected imminently. PT1 public inquiry draft and PT3 public inquiry draft are accessible via the NBN portal. ISO 27001 and IEC 62443 do not automatically create a presumption of CRA Annex I conformity, though they may be used as supporting evidence per EC FAQ 6.1 and Annex VIII Part 1\. Commission guidance final published version: C(2026) 5252, published 27 Jul 2026\.

 

| Ref | Requirement | Conformant? (Yes / No / Partial) | Evidence & Rationale | Guidance / Reference |
| :---- | :---- | :---- | :---- | :---- |
| **2.7.1** | \[GOOD PRACTICE\] The organization should identify which harmonized standards under Standardisation Request M/606 are relevant to its product categories and actively monitor their publication status via ETSI, CEN, and CENELEC. | ☐ Yes   ☐ No   ☐ Partial |   | Standards tracking register; assigned owner. PT1 public inquiry draft: app.nbn.be (search CEN PT1 CRA); PT3 public inquiry draft: app.nbn.be (search CEN PT3 CRA). Note: both drafts have been significantly updated since public inquiry; final versions are not yet publicly available. Monitor via CEN/CENELEC portal. |
| **2.7.2** | \[CRA REQUIREMENT\] Where harmonized standards relevant to the product are not yet available, the organization must document the gap and record whether a Notified Body has been engaged (required for Class I products absent harmonized standards). | ☐ Yes   ☐ No   ☐ Partial |   | Conformity pathway decision log; Notified Body engagement record or written rationale. |
| **2.7.3** | \[GOOD PRACTICE\] The organization should be aware that ISO 27001, IEC 62443, and similar general security standards do not automatically create a presumption of CRA Annex I conformity. CRA conformity must be assessed against Annex I requirements directly. However, per EC FAQ chapter 6.1 and Annex VIII, existing certifications under such standards may be used as supporting evidence within a broader conformity assessment, provided all Annex I essential requirements are explicitly addressed. | ☐ Yes   ☐ No   ☐ Partial |   | Written acknowledgement in conformity documentation. |
| **2.7.4** | \[GOOD PRACTICE\] A trigger should exist to update the conformity pathway and re-run self-certification when a relevant M/606 harmonized standard is published. | ☐ Yes   ☐ No   ☐ Partial |   | Standards publication monitoring procedure; update trigger defined in program governance. |

 

 

# **Section 3: Component Management & SBOM Quality**

This section governs the quality and integrity of SBOMs. CRA Article 13 requires manufacturers to document components with sufficient granularity to identify known vulnerabilities. OpenChain ISO/IEC 18974 requires a documented process for component identification and vulnerability tracking.

 

## **3.1 Software Identification & Bill of Materials**

Processes for generating machine-readable SBOMs for all released products. CRA requires SBOMs covering at the very least the top-level dependencies of those products.

 

| Ref | Requirement | Conformant? (Yes / No / Partial) | Evidence & Rationale | Guidance / Reference |
| :---- | :---- | :---- | :---- | :---- |
| **3.1.1** | \[CRA REQUIREMENT\] The organization must maintain a documented process for generating machine-readable SBOMs for all released products, covering at the very least the top-level dependencies of those products. | ☐ Yes   ☐ No   ☐ Partial |   | SBOM generation procedure; tool configuration (e.g., Syft, Trivy, CycloneDX CLI). Reference: BSI TR-03183. |
| **3.1.2** | \[CRA REQUIREMENT\] SBOMs must be produced in a commonly used, machine-readable format, such as a currently supported version of SPDX or CycloneDX, and must comply with any applicable implementing acts, harmonized standards, or common specifications. | ☐ Yes   ☐ No   ☐ Partial |   | Sample SBOM file; format validation report. Reference: BSI TR-03183-2 for SBOM content requirements. |
| **3.1.3** | \[GOOD PRACTICE\] SBOM generation should be integrated into the CI/CD pipeline and produce an artifact on every release build. | ☐ Yes   ☐ No   ☐ Partial |   | Pipeline configuration excerpt; build artifact manifest. |
| **3.1.4** | \[CRA REQUIREMENT\] SBOMs must cover, at minimum, top-level dependencies and must comprehensively include transitive and embedded dependencies to the depth necessary to identify, assess, and remediate vulnerabilities affecting the product. Any components or dependency levels not covered shall be documented together with a risk-based justification and the alternative measures used to ensure effective vulnerability management. | ☐ Yes   ☐ No   ☐ Partial |   | Tooling depth configuration; documented exclusions with risk-based justification; sample SBOM component count vs. dependency graph audit. |
| **3.1.5** | ⚠ DEADLINE: 11 Sep 2026 \- ⚠  \[GOOD PRACTICE\] The organization should document a target SBOM depth decision with operational rationale tied to the ability to determine within 24 hours whether an actively exploited CVE affects any shipped product. The depth decision should acknowledge implementation limits, define the intended dependency depth for each product or build type, and explain how unresolved transitive dependencies are monitored or risk-managed. A top-level-only SBOM may be insufficient for transitive-dependency scenarios. | ☐ Yes   ☐ No   ☐ Partial |   | SBOM depth policy; operational rationale linking depth to 24-hour window; evidence of automated CVE-to-SBOM matching test; documented monitoring method for unresolved dependency levels. |
| **3.1.6** | \[DIRECT CRA OBLIGATION\] SBOMs must be drawn up in a commonly used, machine-readable format and must cover at least the top-level dependencies of the product. \[ORGANIZATION SBOM PROFILE / IMPLEMENTATION CONTROL\] The organization SBOM profile should include product-level metadata (product name, version, supplier, release date, unique product identifier) and component-level metadata (component name, version, supplier, unique component identifier such as PURL or CPE, cryptographic hash, and license information including declared and concluded license) for each component. These additional fields support implementation, traceability, CISA Minimum Elements alignment, ISO/IEC 18974 alignment, and ISO/IEC 5230 compliance evidence, but are not presented as the CRA statutory minimum. | ☐ Yes   ☐ No   ☐ Partial |   | SBOM field mapping to CRA Annex I (primary requirement), CISA 2025 Minimum Elements for SBOM (informational reference replacing the 2021 NTIA minimum elements), and BSI TR-03183-2 (implementation guidance for German market). Where these references differ, CRA Annex I takes precedence. Reference: https://www.[bsi.bund.de](https://www.bsi.bund.de/EN/Themen/Unternehmen-und-Organisationen/Standards-und-Zertifizierung/Technische-Richtlinien/TR-nach-Thema-sortiert/tr03183/TR-03183_node.html)/TR03183 |
| **3.1.7** | \[GOOD PRACTICE\] For products containing physical hardware components, a Hardware Bill of Materials (HBOM) should be maintained alongside the SBOM to identify hardware components and their firmware dependencies. For machine-readable HBOM exchange, CycloneDX (ECMA-424 / CycloneDX 1.7 or later) is the recommended format; SPDX 3.x hardware profile may be used where producer and consumer tooling support it. Software-only organizations may mark this item N/A with documented rationale. | ☐ Yes   ☐ No   ☐ Partial |   | Machine-readable HBOM (CycloneDX/ECMA-424 preferred; SPDX 3.x hardware profile where supported); hardware component inventory; firmware version register. |
| **3.1.8** | \[GOOD PRACTICE\] The organization should maintain a dependency registry with pinned versions and approved component entries to ensure SBOM reproducibility across builds. | ☐ Yes   ☐ No   ☐ Partial |   | Dependency lock files; package registry configuration; approved component list. |

 

## **3.2 Data Quality & Completeness**

Criteria for validating SBOM completeness, component granularity, and handling Known Unknowns.

 

| Ref | Requirement | Conformant? (Yes / No / Partial) | Evidence & Rationale | Guidance / Reference |
| :---- | :---- | :---- | :---- | :---- |
| **3.2.1** | \[GOOD PRACTICE\] A completeness validation gate should be applied to SBOMs before release, using automated or manual review. | ☐ Yes   ☐ No   ☐ Partial |   | SBOM linting tool output (e.g., sbom-scorecard, ort); CI gate pass/fail log. |
| **3.2.2** | \[CONFORMITY EVIDENCE / IMPLEMENTATION CONTROL\] The organization should maintain a defined policy for handling Known Unknowns \- components whose identity cannot be fully determined \- distinguishing them from intentionally withheld proprietary code. | ☐ Yes   ☐ No   ☐ Partial |   | Policy text or SBOM annotation convention for unknown components. |
| **3.2.3** | \[CONFORMITY EVIDENCE / IMPLEMENTATION CONTROL\] Minimum required SBOM fields per CRA Annex I should be validated, and BSI TR-03183-2 field validation may be used as an implementation reference before SBOM sign-off. | ☐ Yes   ☐ No   ☐ Partial |   | Validation rule set; example of a rejected SBOM and remediation. |
| **3.2.4** | \[GOOD PRACTICE\] Quality metrics for SBOMs (e.g., completeness score, field population rate) should be tracked and reviewed periodically. | ☐ Yes   ☐ No   ☐ Partial |   | Dashboard screenshot or metrics report. |
| **3.2.5** | \[GOOD PRACTICE\] File-level or snippet-level SBOM references should be avoided where a complete software package can be identified. If file-level or snippet-level references are used, the SBOM should clearly label the granularity, map the reference to the smallest complete software package where possible, and state whether the dependency chain terminates at that point when further dependency tracking is not feasible. | ☐ Yes   ☐ No   ☐ Partial |   | SBOM sample; package mapping rationale; snippet/file-level exception record; dependency-chain termination note. |

 

## **3.3 Provenance & Integrity**

Mechanisms for verifying software origins, tamper prevention, change tracking, and secure build infrastructure.

 

| Ref | Requirement | Conformant? (Yes / No / Partial) | Evidence & Rationale | Guidance / Reference |
| :---- | :---- | :---- | :---- | :---- |
| **3.3.1** | \[CONFORMITY EVIDENCE / IMPLEMENTATION CONTROL\] Components in released products should have verified source information, such as upstream repository URL, commit hash, or verified package registry coordinates, where needed to support CRA conformity evidence and supply-chain integrity. | ☐ Yes   ☐ No   ☐ Partial |   | SBOM externalRef fields; PURL entries; reproducible-build artifacts. |
| **3.3.2** | \[CONFORMITY EVIDENCE / IMPLEMENTATION CONTROL\] Cryptographic checksums, such as SHA-256 or stronger, should be recorded for release artifacts where needed to support integrity evidence and release traceability. | ☐ Yes   ☐ No   ☐ Partial |   | Artifact manifest with hash values; signing key documentation. |
| **3.3.3** | \[GOOD PRACTICE\] A change-tracking mechanism should record component additions, removals, and version updates between releases. | ☐ Yes   ☐ No   ☐ Partial |   | SBOM diff report between consecutive releases; changelog integration. |
| **3.3.4** | \[GOOD PRACTICE\] Software signing or attestation (e.g., Sigstore, in-toto, SLSA provenance) should be applied to release artifacts. | ☐ Yes   ☐ No   ☐ Partial |   | Signing workflow; verification command for customers. SLSA framework: [slsa.dev](https://slsa.dev). |
| **3.3.5** | \[GOOD PRACTICE\] The organization should maintain a documented secure build infrastructure policy covering build environment isolation, reproducibility, and integrity verification. | ☐ Yes   ☐ No   ☐ Partial |   | Build environment configuration; reproducible build evidence; infrastructure-as-code repository. |
| **3.3.6** | \[GOOD PRACTICE\] Build pipelines should be isolated from development environments and access to production build systems must be restricted to authorized personnel. | ☐ Yes   ☐ No   ☐ Partial |   | Access control policy for build systems; audit log of build system access. |
| **3.3.7** | \[GOOD PRACTICE\] Build artifacts should be generated in a clean, reproducible environment and verified before promotion to release. | ☐ Yes   ☐ No   ☐ Partial |   | Build verification procedure; clean-room build evidence. |
| **3.3.8** | \[GOOD PRACTICE\] Secrets (API keys, signing keys, credentials) must NOT be embedded in source code or build artifacts. A secrets management solution should be used. | ☐ Yes   ☐ No   ☐ Partial |   | Secrets scanning tool configuration; secrets management policy; tool output showing no embedded secrets. |
| **3.3.9** | \[GOOD PRACTICE\] Signing keys used for release artifact attestation should be stored in a hardware security module (HSM) or equivalent key management system. | ☐ Yes   ☐ No   ☐ Partial |   | Key management policy; HSM or KMS configuration evidence. |
| **3.3.10** | \[GOOD PRACTICE\] The organization should document the full chain of custody from source code commit to released artifact, enabling post-incident provenance analysis. | ☐ Yes   ☐ No   ☐ Partial |   | Build provenance attestation (e.g., SLSA provenance); artifact lineage documentation. |
| **3.3.11** | \[GOOD PRACTICE\] Third-party build tools, compilers, and dependencies used in the build pipeline should be inventoried, version-pinned, and monitored for vulnerabilities. | ☐ Yes   ☐ No   ☐ Partial |   | Build tool inventory; version pinning configuration; vulnerability monitoring scope including build tools. |
| **3.3.12** | \[GOOD PRACTICE\] The integrity of the build pipeline itself should be verified periodically through pipeline audits or automated integrity checks. | ☐ Yes   ☐ No   ☐ Partial |   | Pipeline audit records; integrity check configuration; anomaly detection evidence. |

 

## **3.4 Secure Development Properties & Security Testing (CRA Annex I, Part I)**

CRA Annex I Part I mandates products are designed and produced with security by default. This subsection defines secure product design and development capabilities, not only release testing. Organizations should build security architecture design, secure feature development, threat modeling, and verification practices into the product lifecycle so authentication, least privilege, encryption, logging, data protection, secure update, and attack-surface controls are designed in from the outset. Items here supply required content for the Technical File (§7.1).

 

| Ref | Requirement | Conformant? (Yes / No / Partial) | Evidence & Rationale | Guidance / Reference |
| :---- | :---- | :---- | :---- | :---- |
| **3.4.1** | \[CRA REQUIREMENT\] Products must be delivered without default credentials. Where authentication is required, users must be prompted to set unique credentials on first use and default-deny network exposure must apply (CRA Annex I Part I). | ☐ Yes   ☐ No   ☐ Partial |   | Secure configuration policy; product startup flow documentation; credential policy test records. |
| **3.4.2** | \[CRA REQUIREMENT\] Attack surface minimization must be applied: unnecessary ports, services, and interfaces must be disabled by default and documented in an inbound connections register. | ☐ Yes   ☐ No   ☐ Partial |   | Secure defaults checklist; inbound connections register; network exposure map; hardening guide. |
| **3.4.3** | \[CONFORMITY EVIDENCE / IMPLEMENTATION CONTROL\] Data in transit must be encrypted using current standards (TLS 1.2 or higher or equivalent). Data at rest must be encrypted where the cybersecurity risk assessment identifies sensitivity. | ☐ Yes   ☐ No   ☐ Partial |   | Encryption policy; TLS configuration audit; data classification map. |
| **3.4.4** | \[CONFORMITY EVIDENCE / IMPLEMENTATION CONTROL\] Memory-safety mechanisms must be applied where technically feasible (e.g., memory-safe languages, compiler mitigations such as ASLR, stack canaries, CFI). Any exceptions must be documented with compensating controls. | ☐ Yes   ☐ No   ☐ Partial |   | Build flag configuration; language or runtime selection rationale; exception register. |
| **3.4.5** | \[CONFORMITY EVIDENCE / IMPLEMENTATION CONTROL\] Static Application Security Testing (SAST) must be integrated into the CI/CD pipeline and executed on every release candidate. Critical and high findings must be resolved or formally risk-accepted before release. | ☐ Yes   ☐ No   ☐ Partial |   | SAST tool configuration; scan results summary; finding disposition records. |
| **3.4.6** | \[CONFORMITY EVIDENCE / IMPLEMENTATION CONTROL\] Dynamic Application Security Testing (DAST) or fuzzing must be applied at minimum on each major release and results must be documented. | ☐ Yes   ☐ No   ☐ Partial |   | DAST or fuzzing tool output; results triage records; remediation evidence. |
| **3.4.7** | \[CONFORMITY EVIDENCE / IMPLEMENTATION CONTROL\] Penetration testing or a structured threat-model-based security review must be performed at minimum annually or upon significant architectural change. An independent assessment should be used periodically. Findings must be tracked to remediation. | ☐ Yes   ☐ No   ☐ Partial |   | Pentest report or security review record; finding tracker; remediation sign-off. |
| **3.4.8** | \[CONFORMITY EVIDENCE / IMPLEMENTATION CONTROL\] Security testing evidence (SAST results, pentest reports, DAST outputs) must be retained as part of the Technical File. Retention period: at least 10 years after market placement, or the support period if longer (CRA Art. 13(13)). | ☐ Yes   ☐ No   ☐ Partial |   | Technical File index entry for security testing artifacts; retention policy. |
| **3.4.9** | \[CONFORMITY EVIDENCE / IMPLEMENTATION CONTROL\] A threat model must be produced for each product, covering the attack surface, threat actors, attack vectors, and mitigating controls. The threat model must be updated upon significant architectural change. | ☐ Yes   ☐ No   ☐ Partial |   | Threat model document; methodology used (e.g., STRIDE, PASTA); update history. |
| **3.4.10** | \[CONFORMITY EVIDENCE / IMPLEMENTATION CONTROL\] A documented release security gate must exist and must be passed before any product version is placed on the EU market. The gate must verify that all critical and high security findings are resolved or formally risk-accepted. | ☐ Yes   ☐ No   ☐ Partial |   | Release gate checklist; sign-off evidence; exception log for accepted risks. |
| **3.4.11** | \[GOOD PRACTICE\] The organization should maintain a documented secure coding standard covering input validation, authentication, session management, error handling, and cryptographic usage, and must train developers on its application. | ☐ Yes   ☐ No   ☐ Partial |   | Secure coding standard document; developer training records. |

 

## **3.5 Importer and Distributor Obligations**

CRA Art. 19 and Art. 20 place independent obligations on importers and distributors. Note: under Art. 24, OSS Stewards may also fall within scope of these obligations depending on their specific activities; legal determination is recommended.

 

| Ref | Requirement | Conformant? (Yes / No / Partial) | Evidence & Rationale | Guidance / Reference |
| :---- | :---- | :---- | :---- | :---- |
| **3.5.1** | \[CRA REQUIREMENT\] Before placing an imported product on the EU market, the organization must verify: (a) the manufacturer has completed the appropriate conformity assessment; (b) required technical documentation exists; (c) the product bears CE marking and includes the EU Declaration of Conformity; (d) the manufacturer has a vulnerability handling process in place for the declared support period (CRA Art. 19). Note: OSS Stewards may also fall within scope of these obligations under CRA Art. 24 depending on their activities; legal determination is recommended. | ☐ Yes   ☐ No   ☐ Partial |   | Importer due-diligence checklist per product; manufacturer conformity evidence on file; CE mark verification record. |
| **3.5.2** | \[CRA REQUIREMENT\] If the organization has reason to believe an imported product is not in conformity with the CRA, it must NOT place it on the market until conformity is achieved, and must inform the manufacturer and, where appropriate, market surveillance authorities (CRA Art. 19). | ☐ Yes   ☐ No   ☐ Partial |   | Non-conformity hold procedure; example record of a hold or escalation. |
| **3.5.3** | \[CRA REQUIREMENT\] As a distributor, the organization must verify the product bears CE marking, includes required instructions and information, and meets essential requirements before making it available. If the distributor becomes aware of a vulnerability or cybersecurity risk in a distributed product, it must notify the manufacturer and cooperate with market surveillance authorities (CRA Art. 20). | ☐ Yes   ☐ No   ☐ Partial |   | Distributor due-diligence checklist; vulnerability notification procedure to manufacturer; market surveillance cooperation record. |
| **3.5.4** | \[CRA REQUIREMENT\] System integrators who combine components from multiple manufacturers into a solution placed on the EU market must formally determine whether they are acting as a manufacturer under the CRA. If so, the full conformity assessment obligation applies to the integrated system. | ☐ Yes   ☐ No   ☐ Partial |   | System integrator role determination memo; legal sign-off; conformity assessment plan for the integrated system if applicable. |

 

 

## **3.6 Third-Party Software Supply Chain Qualification**

Third-party software includes commercial off-the-shelf software, SDKs, technology partnership components, outsourced development deliverables, ODM/OEM components, freeware, and other non-open-source software incorporated into products with digital elements. Manufacturers should qualify and manage these suppliers and components across the lifecycle so third-party software does not compromise CRA readiness.

 

| Ref | Requirement | Conformant? (Yes / No / Partial) | Evidence & Rationale | Guidance / Reference |
| :---- | :---- | :---- | :---- | :---- |
| **3.6.1** | \[GOOD PRACTICE\] The organization should maintain an inventory of third-party software sources, including COTS software, SDKs, technology partner components, outsourced development deliverables, ODM/OEM components, freeware, and other non-open-source software included in products with digital elements. | ☐ Yes   ☐ No   ☐ Partial |   | Third-party software register; supplier/source classification; component owner records. |
| **3.6.2** | \[GOOD PRACTICE\] Third-party software suppliers should be qualified before use based on security capability, vulnerability handling process, update/support commitments, and ability to support CRA evidence requests. | ☐ Yes   ☐ No   ☐ Partial |   | Supplier qualification checklist; security questionnaire; approval record. |
| **3.6.3** | \[GOOD PRACTICE\] Contracts or equivalent procurement controls should allocate CRA-relevant responsibilities, including vulnerability notification, security update cooperation, SBOM or component information availability, and support-period commitments where applicable. | ☐ Yes   ☐ No   ☐ Partial |   | Contract clause library; supplier terms; procurement approval record. |
| **3.6.4** | \[GOOD PRACTICE\] Outsourced development and technology partnership deliverables should undergo software code compliance and security review before integration into the product build or release baseline. | ☐ Yes   ☐ No   ☐ Partial |   | Code review records; security testing reports; acceptance criteria; release gate evidence. |
| **3.6.5** | \[GOOD PRACTICE\] ODM/OEM and embedded third-party components should be assessed for vulnerability monitoring, update delivery, secure configuration, and support lifecycle alignment with the product support period. | ☐ Yes   ☐ No   ☐ Partial |   | ODM/OEM assessment; support matrix; vulnerability monitoring record; update delivery evidence. |
| **3.6.6** | \[GOOD PRACTICE\] The organization should maintain lifecycle governance for third-party software introduction, evaluation, approval, monitoring, requalification, risk mitigation, and retirement. | ☐ Yes   ☐ No   ☐ Partial |   | Third-party software governance process; review cadence; risk register; retirement/EOL records. |

 

# **Section 4: Vulnerability Handling & Vulnerability Exchange (VEX / CSAF)**

CRA Article 13(6) requires manufacturers to address vulnerabilities without undue delay. Article 14 establishes a mandatory three-stage reporting cascade to the CRA Single Reporting Platform (SRP). This section defines the end-to-end vulnerability lifecycle from ingestion through disclosure and regulatory notification.

 

## **4.1 Vulnerability Ingestion & Monitoring**

Process for continuously monitoring all identified software components in supported products against vulnerability databases and advisory feeds.

 

| Ref | Requirement | Conformant? (Yes / No / Partial) | Evidence & Rationale | Guidance / Reference |
| :---- | :---- | :---- | :---- | :---- |
| **4.1.1** | \[CRA REQUIREMENT\] During the support period, the organization must continuously monitor all identified software components contained in supported products against relevant vulnerability databases, supplier advisories, and other reliable vulnerability sources. Monitoring must be performed at a documented, risk-based frequency and at a documented, risk-based frequency; daily monitoring may be used as an organisational implementation target where automated monitoring is available. Known gaps in component coverage must be documented and addressed through supplementary identification and monitoring measures. | ☐ Yes   ☐ No   ☐ Partial |   | Tool configuration; EUVD ([euvd.enisa.europa.eu](https://euvd.enisa.europa.eu)) feed; NVD, OSV, GitHub Advisory feeds; example alert triggered by a new CVE. |
| **4.1.2** | \[GOOD PRACTICE\] Monitoring results should be logged and retained for audit purposes. | ☐ Yes   ☐ No   ☐ Partial |   | Scan schedule configuration; log retention policy. |
| **4.1.3** | \[GOOD PRACTICE\] A defined intake process should triage new vulnerability alerts within a documented, risk-based SLA. | ☐ Yes   ☐ No   ☐ Partial |   | Triage SLA table in vulnerability management policy. |
| **4.1.4** | \[GOOD PRACTICE\] Vulnerability data should be enriched with contextual scoring (e.g., EPSS, KEV catalog status) to support risk-based prioritization. A documented Patch SLA Matrix should define response timelines by severity tier. | ☐ Yes   ☐ No   ☐ Partial |   | Enrichment pipeline documentation; Patch SLA Matrix; example enriched alert record. |
| **4.1.5** | \[GOOD PRACTICE / IMPLEMENTATION CONTROL\] The EU Vulnerability Database (EUVD, operated by ENISA at euvd.enisa.europa.eu) should be included as a monitored ingestion feed where appropriate. EUVD is an important ENISA vulnerability source and may support Article 14 assessment, but it is not the exclusive or mandatory source for determining Article 14 reportability. | ☐ Yes   ☐ No   ☐ Partial |   | EUVD feed configuration; monitoring tool screenshot showing EUVD as an ingestion source. |
| **4.1.6** | \[GOOD PRACTICE\] The CISA Known Exploited Vulnerabilities (KEV) catalog should be monitored as a trigger for immediate applicability and active-exploitation assessment. A KEV listing for any component in a shipped product should trigger assessment; Article 14 reporting is triggered when the manufacturer becomes aware of an actively exploited vulnerability contained in the product. | ☐ Yes   ☐ No   ☐ Partial |   | KEV monitoring configuration; documented linkage between KEV listing event and Art. 14 RACI trigger. |
| **4.1.7** | \[GOOD PRACTICE\] Vulnerability monitoring should extend to third-party and open-source components for which the manufacturer has not received an SBOM from the upstream supplier, using supplementary identification methods. | ☐ Yes   ☐ No   ☐ Partial |   | Supplementary monitoring procedure for components without upstream SBOM; tooling configuration. |
| **4.1.8** | \[GOOD PRACTICE\] Vulnerability management KPIs (e.g., mean time to detect, mean time to remediate by severity tier, percentage of components with confirmed monitoring coverage) should be tracked and reviewed periodically. | ☐ Yes   ☐ No   ☐ Partial |   | KPI dashboard or metrics report; review cadence documentation. |

 

## **4.2 Risk Adjudication & Vulnerability Exchange (VEX / CSAF)**

Evaluating vulnerability exploitability in context and issuing machine-readable exploitability statements conforming to a recognized standard (CSAF v2.0 VEX profile, CycloneDX VEX, or OpenVEX).

 

| Ref | Requirement | Conformant? (Yes / No / Partial) | Evidence & Rationale | Guidance / Reference |
| :---- | :---- | :---- | :---- | :---- |
| **4.2.1** | \[CRA REQUIREMENT\] The organization must maintain a documented vulnerability exploitability assessment process covering reachability analysis, exploitability in context, and environmental factors. | ☐ Yes   ☐ No   ☐ Partial |   | Vulnerability exploitability assessment process document; assessment criteria checklist. Reference: CISA VEX minimum viable guidelines. |
| **4.2.2** | \[GOOD PRACTICE\] Vulnerability exploitability statements should be issued in a machine-readable format conforming to a recognised vulnerability exchange standard. Accepted formats include CSAF v2.0 VEX profile, CycloneDX 1.4+ VEX, or OpenVEX. | ☐ Yes   ☐ No   ☐ Partial |   | Sample exploitability statement; tooling used (e.g., Interlynk vexctl, CycloneDX CLI, OpenVEX tooling). |
| **4.2.3** | \[GOOD PRACTICE\] Exploitability statements should conform to the native status vocabulary and justification fields of the chosen standard without modification. The chosen standard's status values must be used as defined (e.g., CSAF: fixed, known\_affected, known\_not\_affected, under\_investigation; CycloneDX: not\_affected, affected, fixed, under\_investigation, false\_positive). | ☐ Yes   ☐ No   ☐ Partial |   | Exploitability statement status mapping table; sample justified statements per chosen standard. |
| **4.2.4** | \[GOOD PRACTICE\] Exploitability statements should be versioned, timestamped, and retained as part of the product's technical documentation. | ☐ Yes   ☐ No   ☐ Partial |   | Exploitability statement archive; version control history. |
| **4.2.5** | \[GOOD PRACTICE\] A Safety Relevance classification should be applied to components where functional safety or AI/autonomous system context applies (e.g., SRIL/SRAP framework or equivalent). Organizations without safety-critical products may mark this item N/A with documented rationale. | ☐ Yes   ☐ No   ☐ Partial |   | Safety relevance scoring methodology; component classification register. |

 

## **4.3 Actionable Decisions**

Defined criteria for four operational outcomes: Immediate Remediation, Monitored Deferral, Formal Risk Acceptance, and Escalation.

 

| Ref | Requirement | Conformant? (Yes / No / Partial) | Evidence & Rationale | Guidance / Reference |
| :---- | :---- | :---- | :---- | :---- |
| **4.3.1** | \[CRA REQUIREMENT\] The organization must document decision criteria for immediate remediation (e.g., actively exploited vulnerability confirmed, CVSS base score meeting a defined threshold, or safety-critical component affected). | ☐ Yes   ☐ No   ☐ Partial |   | Decision matrix or policy text defining remediation triggers. |
| **4.3.2** | \[GOOD PRACTICE\] Decision criteria for monitored deferral should be documented, including maximum deferral window and re-assessment trigger. | ☐ Yes   ☐ No   ☐ Partial |   | Deferral SLA table; re-assessment schedule. |
| **4.3.3** | \[GOOD PRACTICE\] Formal risk acceptance must require documented business justification, a named risk owner, and a defined expiry date. | ☐ Yes   ☐ No   ☐ Partial |   | Risk acceptance form template; approval workflow. |
| **4.3.4** | \[CRA REQUIREMENT\] The organization must define escalation criteria and escalation paths, including when regulatory notification under CRA Art. 14 is triggered. | ☐ Yes   ☐ No   ☐ Partial |   | Escalation matrix; contact list with roles. |
| **4.3.5** | \[GOOD PRACTICE\] All vulnerability disposition outcomes should be tracked in a vulnerability register with current status, owner, and resolution date. | ☐ Yes   ☐ No   ☐ Partial |   | Vulnerability register schema; sample populated record. |

 

## **4.4 Disclosure & Regulatory Reporting (CRA Art. 14 Three-Stage Cascade)**

Standard operating procedures for publicly disclosing fixes, providing mitigation guidance, and meeting the three-stage CRA Article 14 regulatory reporting cascade: Early Warning (24h), Full Notification (72h), and Final Report. Items marked with a deadline are required before 11 Sep 2026\.

 

| Ref | Requirement | Conformant? (Yes / No / Partial) | Evidence & Rationale | Guidance / Reference |
| :---- | :---- | :---- | :---- | :---- |
| **4.4.1** | \[CRA REQUIREMENT\] The organization must maintain a security advisory process to notify affected customers and users without undue delay regarding actively exploited vulnerabilities or severe security incidents, including available mitigations and corrective actions (CRA Art. 14(8)). | ☐ Yes   ☐ No   ☐ Partial |   | Advisory template; distribution channel list (CVE.org, product portal, mailing list). |
| **4.4.2** | ⚠ DEADLINE: 11 Sep 2026 \- ⚠  \[CRA REQUIREMENT\] Actively exploited vulnerabilities contained in a product with digital elements must be notified simultaneously to the CSIRT designated as coordinator and to ENISA via the CRA Single Reporting Platform (SRP), with an early warning within 24 hours of the organization becoming aware of active exploitation (CRA Art. 14(1), 14(2)(a), 14(7)). | ☐ Yes   ☐ No   ☐ Partial |   | SRP submission runbook; on-call contact for SRP platform access; tabletop exercise or internal reporting simulation record. |
| **4.4.3** | ⚠ DEADLINE: 11 Sep 2026 \- ⚠  \[CRA REQUIREMENT\] A full vulnerability notification must be submitted to the CRA Single Reporting Platform (SRP) without undue delay and, in any event, within 72 hours after the manufacturer becomes aware of the actively exploited vulnerability, including severity assessment, affected versions, and interim mitigations (CRA Art. 14(2)(b) \- Full Notification). | ☐ Yes   ☐ No   ☐ Partial |   | Full notification template mapped to SRP required fields; 72-hour SLA documented in runbook. |
| **4.4.4** | ⚠ DEADLINE: 11 Sep 2026 \- ⚠  \[CRA REQUIREMENT\] A final report must be submitted to the CRA Single Reporting Platform (SRP) within 14 days after a corrective or mitigating measure becomes available, including the vulnerability description, severity and impact; available information concerning any malicious actor; and details of the security update or other corrective measures (CRA Art. 14(2)(c) \- Final Report). Root-cause analysis and disclosure timeline information may be retained as internal post-incident evidence. | ☐ Yes   ☐ No   ☐ Partial |   | Final report template; post-incident review procedure; 14-day SLA clock definition. |
| **4.4.5** | ⚠ DEADLINE: 11 Sep 2026 \- ⚠  \[CRA REQUIREMENT\] Severe security incidents impacting the availability, authenticity, integrity, or confidentiality of sensitive or important data or functions, or leading or capable of leading to malicious code introduction or execution, must be notified simultaneously to the CSIRT designated as coordinator and to ENISA via the CRA Single Reporting Platform (SRP) (CRA Art. 14(3)-(5)). The final report for severe incidents must be submitted within one month after submission of the 72-hour incident notification under CRA Art. 14(4)(b). | ☐ Yes   ☐ No   ☐ Partial |   | Severe security incident definition document (aligns with NIS2 thresholds); incident triage criteria; one-month final report template. |
| **4.4.6** | \[CRA REQUIREMENT\] Affected customers and users must be notified without undue delay regarding actively exploited vulnerabilities or severe security incidents, including available mitigations and corrective actions (CRA Art. 14(8)). | ☐ Yes   ☐ No   ☐ Partial |   | Customer advisory template; notification runbook; mailing list, portal, or security advisory feed evidence. |
| **4.4.7** | \[CRA REQUIREMENT\] The organization must maintain a Coordinated Vulnerability Disclosure (CVD) policy and an identifiable reporting/contact mechanism. Response SLA and safe harbor language may be retained as good-practice implementation controls. | ☐ Yes   ☐ No   ☐ Partial |   | CVD policy URL; security.txt file. Reference: ISO/IEC 30111 and 29147\. |
| **4.4.8** | \[CRA REQUIREMENT\] Where a security update is not immediately available, the organization must issue mitigation guidance (workarounds, configuration changes) to affected users without undue delay. | ☐ Yes   ☐ No   ☐ Partial |   | Example advisory with mitigation section. |
| **4.4.9** | \[CRA REQUIREMENT\] The organization must formally identify the national CSIRT to which CRA Art. 14 reports are addressed. For a manufacturer with a main establishment in the Union, the CSIRT is determined by the Member State where cybersecurity decisions for its products with digital elements are predominantly taken. Where no main establishment exists in the Union, the organization must apply the CRA Art. 14(7) fallback order based on authorised representative, importer, distributor, and then highest number of users. This determination must be documented and reviewed when relevant facts change. | ☐ Yes   ☐ No   ☐ Partial |   | CSIRT routing determination memo; reference to Delegated Regulation (EU) 2026/881. |
| **4.4.10** | \[CRA REQUIREMENT\] The organization must document that the SME fine exemption under CRA Art. 14 covers only the financial penalty for missing the 24-hour Early Warning window and does NOT exempt the organization from the reporting obligation itself. | ☐ Yes   ☐ No   ☐ Partial |   | Written acknowledgement in compliance program documentation; Art. 14 RACI maintained regardless of SME status. |
| **4.4.11** | \[CRA REQUIREMENT\] The organization must be aware that under Delegated Regulation (EU) 2026/881, the receiving CSIRT may delay dissemination to other member state CSIRTs on justified cybersecurity grounds. Any delay must be strictly limited and ENISA must be informed immediately. The Art. 14 runbook must reference this mechanism. | ☐ Yes   ☐ No   ☐ Partial |   | Art. 14 runbook section on CSIRT dissemination delay; reference to Delegated Regulation (EU) 2026/881. |

 

## **4.5 Art. 14 Notification RACI \- Roles & Trigger Ownership**

CRA Article 14 imposes hard time-based obligations requiring pre-assigned, tested role ownership. All deadline items must be completed before 11 Sep 2026\.

 

| Ref | Requirement | Conformant? (Yes / No / Partial) | Evidence & Rationale | Guidance / Reference |
| :---- | :---- | :---- | :---- | :---- |
| **4.5.1** | ⚠ DEADLINE: 11 Sep 2026 \- ⚠  \[CRA REQUIREMENT\] The organization must designate a named individual (by role) as the Art. 14 Notification Owner responsible for initiating the Early Warning submission to the CRA Single Reporting Platform (SRP) within the 24-hour clock. | ☐ Yes   ☐ No   ☐ Partial |   | RACI table entry; named backup; on-call schedule. |
| **4.5.2** | ⚠ DEADLINE: 11 Sep 2026 \- ⚠  \[CRA REQUIREMENT\] The organization must designate a named individual (by role) responsible for completing and submitting the 72-hour Full Notification to the CRA Single Reporting Platform (SRP), empowered to escalate to legal or executive if additional approvals are required. | ☐ Yes   ☐ No   ☐ Partial |   | RACI table entry; escalation path documented. |
| **4.5.3** | ⚠ DEADLINE: 11 Sep 2026 \- ⚠  \[CRA REQUIREMENT\] The organization must designate a named individual (by role) to own the 14-day Final Report for actively exploited vulnerabilities and the one-month final report for severe incidents, coordinate post-incident review inputs, and sign off on the submission. | ☐ Yes   ☐ No   ☐ Partial |   | RACI table entry; final report review workflow. |
| **4.5.4** | ⚠ DEADLINE: 11 Sep 2026 \- \[CRA REQUIREMENT\] The organization should maintain CRA Single Reporting Platform (SRP) readiness by ensuring EU Login access, designated primary and backup submitters, an offline notification worksheet, and a documented tabletop exercise. Manufacturers and open source software stewards should initiate CSIRT validation when a specific notification needs to be submitted, consistent with ENISA SRP guidance; validation does not prevent submission. | ☐ Yes   ☐ No   ☐ Partial |   | EU Login readiness record; primary/backup submitter assignment; offline notification worksheet; tabletop exercise or internal reporting simulation record. |
| **4.5.5** | \[CRA REQUIREMENT\] The organization must maintain a documented procedure recording when awareness of an incident or actively exploited vulnerability first occurred, to establish the Art. 14 reporting clock start time. | ☐ Yes   ☐ No   ☐ Partial |   | Incident log with awareness timestamp; governance documentation. |
| **4.5.6** | \[CRA REQUIREMENT\] The Art. 14 RACI must be reviewed and re-confirmed upon any relevant personnel change and at minimum annually. | ☐ Yes   ☐ No   ☐ Partial |   | RACI version history; review record. |

 

 

# **Section 5: Open Source Software (OSS) Stewardship**

The definition, scope, and obligations of Open Source Software Stewards are established in CRA Art. 3(14), Recitals 18 and 19, and Art. 24\. This section governs upstream engagement, license compliance, and steward vs. maintainer boundaries.

 

## **5.1 Open Source Contribution & Engagement**

Policy for engaging with upstream open-source communities while maintaining CRA compliance.

 

| Ref | Requirement | Conformant? (Yes / No / Partial) | Evidence & Rationale | Guidance / Reference |
| :---- | :---- | :---- | :---- | :---- |
| **5.1.1** | \[GOOD PRACTICE\] The organization should maintain a documented policy governing how personnel contribute to upstream open-source projects, including CLA/DCO requirements and IP assignment rules. | ☐ Yes   ☐ No   ☐ Partial |   | OSS contribution policy; CLA tool configuration. OpenChain ISO/IEC 5230 as reference. |
| **5.1.2** | \[CRA REQUIREMENT\] Security vulnerabilities discovered during product work must be responsibly disclosed to upstream maintainers before public disclosure (CRA Art. 13 manufacturer responsibility for third-party components). | ☐ Yes   ☐ No   ☐ Partial |   | Upstream disclosure procedure; example disclosure record. |
| **5.1.3** | \[GOOD PRACTICE\] The organization should engage with relevant security working groups (e.g., OpenSSF, CISA, CycloneDX community) to improve OSS supply chain security. Note: This is a recommended good practice and is not a published CRA legal requirement. | ☐ Yes   ☐ No   ☐ Partial |   | Membership records; meeting participation log; issue/PR contributions. |
| **5.1.4** | \[GOOD PRACTICE\] OSS dependencies should be assessed for community health (maintenance status, contributor diversity, EOL date) before adoption. Components whose EOL falls within the product support lifetime should be avoided or formally risk-accepted. | ☐ Yes   ☐ No   ☐ Partial |   | Dependency health assessment checklist; tooling (e.g., OpenSSF Scorecard: [securityscorecards.dev](https://securityscorecards.dev)). |
| **5.1.5** | \[CRA REQUIREMENT\] For any OSS project where the manufacturer vs. steward classification is non-obvious, the organization must apply a formal commercial-activity test using criteria from Commission guidance C(2026) 5252: (a) charging a fee for the software; (b) charging for technical support exceeding cost recovery; (c) intending to monetize through a platform; (d) collecting personal data beyond security/compatibility purposes; (e) accepting donations exceeding operational costs. These criteria are indicators supporting the commercial-activity assessment. The final manufacturer, steward, or out-of-scope determination should be based on CRA analysis and documented legal review, taking Commission guidance into account as non-binding interpretative guidance. | ☐ Yes   ☐ No   ☐ Partial |   | Commercial-activity test worksheet per project; legal sign-off on borderline cases; reference to Commission guidance C(2026) 5252\. |
| **5.1.6** | \[CRA REQUIREMENT\] The organization must maintain a documented process for managing integration risk from upstream OSS components whose maintainers are not directly CRA-obligated. This process must cover how the organization assesses component security hygiene, monitors for vulnerabilities in those components, and documents its findings. Where upstream projects provide SBOM artifacts, CVD policies, or patch timelines, the organization should use them. Where they do not, the organization must document its compensating measures. The organization should support upstream projects in improving security transparency over time rather than treating the absence of these artifacts as a blocker. | ☐ Yes   ☐ No   ☐ Partial |   | Upstream due-diligence checklist; criteria for accepting or rejecting components; reference to CRA Art. 13 manufacturer responsibility. |
| **5.1.7** | \[GOOD PRACTICE\] A dependency approval gate should exist requiring security review of new dependencies before they are introduced into supported products. | ☐ Yes   ☐ No   ☐ Partial |   | Dependency approval procedure; approval workflow; example approved and rejected dependency records. |

 

## **5.2 Steward vs. Maintainer Boundaries**

Guidelines clarifying the distinct obligations of OSS Stewards under CRA Art. 3(14), Recitals 18 and 19, and Art. 24(1), versus individual project maintainers.

 

| Ref | Requirement | Conformant? (Yes / No / Partial) | Evidence & Rationale | Guidance / Reference |
| :---- | :---- | :---- | :---- | :---- |
| **5.2.1** | \[CRA REQUIREMENT\] The organization must document whether it meets the definition of an OSS Steward under CRA Art. 3(14) and record this determination with supporting rationale. | ☐ Yes   ☐ No   ☐ Partial |   | Legal determination memo; CRA Art. 3(14) criteria checklist. |
| **5.2.2** | \[CRA REQUIREMENT\] For projects where the organization acts as Steward, a lightweight cybersecurity policy must be put in place and documented in a verifiable manner under CRA Art. 24(1). Publication through SECURITY.md may be retained as good practice. | ☐ Yes   ☐ No   ☐ Partial |   | SECURITY.md or equivalent policy for each steward project. Reference: CRA Art. 24(1) and Annex II. |
| **5.2.3** | \[GOOD PRACTICE\] Internal maintainers should understand their distinct obligations vs. the organization's steward-level obligations and should receive appropriate guidance. | ☐ Yes   ☐ No   ☐ Partial |   | Training or guidance document; maintainer role definition. |
| **5.2.4** | \[GOOD PRACTICE\] A registry of projects where the organization acts as Steward (vs. Manufacturer) should be maintained and reviewed annually. | ☐ Yes   ☐ No   ☐ Partial |   | Steward registry document; review record. |

 

 

## **5.3 Self-Maintained Open Source Software**

This subsection applies where an organization uses legacy, unsupported, end-of-life, forked, or internally maintained open source components in products with digital elements. These items are not a general requirement for all open source use; they apply when the organization assumes maintenance responsibility because upstream support is unavailable or insufficient.

 

| Ref | Requirement | Conformant? (Yes / No / Partial) | Evidence & Rationale | Guidance / Reference |
| :---- | :---- | :---- | :---- | :---- |
| **5.3.1** | \[GOOD PRACTICE\] Where legacy, end-of-life, forked, or internally maintained open source components are used, the organization should define a self-maintenance framework covering ownership, support scope, patch responsibility, and exit criteria. | ☐ Yes   ☐ No   ☐ Partial |   | Self-maintained OSS register; component owner assignment; support plan; risk acceptance record. |
| **5.3.2** | \[GOOD PRACTICE\] Self-maintained open source components should have source traceability and development management controls, including upstream origin, fork history, local modifications, build provenance, and release branch records. | ☐ Yes   ☐ No   ☐ Partial |   | Source repository records; fork history; patch logs; build provenance. |
| **5.3.3** | \[GOOD PRACTICE\] The organization should maintain version release and security update processes for self-maintained open source components used in released products. | ☐ Yes   ☐ No   ☐ Partial |   | Release procedure; version tags; update records; customer/security advisory records where applicable. |
| **5.3.4** | \[GOOD PRACTICE\] Where self-maintained open source components are redistributed or publicly supported, the organization should provide a mechanism for publishing security advisories, update availability, and contact information, such as a project page, security advisory feed, or equivalent channel. | ☐ Yes   ☐ No   ☐ Partial |   | Advisory page or feed; SECURITY.md; contact point; distribution record. |

 

# **Section 6: Security Updates & Support Period**

CRA Article 13(2) requires manufacturers to formally document the expected support period and provide security updates throughout that period.

 

## **6.1 Support Period Definition & Update Obligations**

 

| Ref | Requirement | Conformant? (Yes / No / Partial) | Evidence & Rationale | Guidance / Reference |
| :---- | :---- | :---- | :---- | :---- |
| **6.1.1** | \[CRA REQUIREMENT\] The organization must define and publish the expected support period for each product with digital elements placed on the EU market. The support period must be at least five years unless the expected product lifetime is shorter. A rolling-release model is also a valid approach, provided the end of support is clearly communicated and security updates are provided throughout (CRA Art. 13(2)). | ☐ Yes   ☐ No   ☐ Partial |   | Product lifecycle documentation; public-facing support statement; legal justification if period is less than 5 years; rolling-release policy if applicable. |
| **6.1.2** | \[CRA REQUIREMENT\] Security updates addressing identified security issues must be disseminated without delay and, unless otherwise agreed between a manufacturer and a business user for a tailor-made product with digital elements, free of charge (CRA Annex I Part II, point (8)). Issued security updates must remain available for the period required by CRA Art. 13(9). | ☐ Yes   ☐ No   ☐ Partial |   | Patch management policy; release history showing security updates issued within support window. |
| **6.1.3** | \[CRA REQUIREMENT\] The organization must document, implement, and test a secure software update mechanism including integrity verification of update packages, protection against rollback attacks, and automatic delivery by default where technically feasible with user opt-out capability. | ☐ Yes   ☐ No   ☐ Partial |   | Update architecture document; signing key management; rollback-prevention test records; automatic update configuration. |
| **6.1.4** | \[CRA REQUIREMENT\] End-of-support dates and associated security implications must be communicated to customers and downstream integrators, including at least the month and year at the time of purchase in an easily accessible manner (CRA Art. 13(8), 13(19)). As good practice, where feasible, at least 12 months advance notice should be given before the final security update. | ☐ Yes   ☐ No   ☐ Partial |   | Customer communication records; EoL announcement template; advance notice evidence. |
| **6.1.5** | \[GOOD PRACTICE\] Where a product reaches end-of-support during an active vulnerability's remediation window, the organization should maintain a documented escalation procedure to manage customer risk. | ☐ Yes   ☐ No   ☐ Partial |   | EoL vulnerability handling procedure; customer advisory template. |
| **6.1.6** | \[GOOD PRACTICE\] An end-of-support transition procedure should exist to guide customers through migration, including identification of supported alternatives and a timeline for ending security update delivery. | ☐ Yes   ☐ No   ☐ Partial |   | EoL transition guide; customer migration documentation; timeline for final security update. |
| **6.1.7** | \[GOOD PRACTICE\] At end-of-life, the organization should provide or document a procedure for secure deletion of user data held by the product and for secure data transfer to alternative solutions. | ☐ Yes   ☐ No   ☐ Partial |   | Data sanitization procedure; secure deletion test records; data portability documentation. |

 

 

# **Section 7: Technical File & Supply Chain Sharing**

CRA Articles 13(12), 13(13), 28, 31, and Annex VII require manufacturers to prepare technical documentation and make it available to MSAs on request. This section ensures all legal documentation obligations are met.

 

## **7.1 Market Surveillance Deliverables**

 

| Ref | Requirement | Conformant? (Yes / No / Partial) | Evidence & Rationale | Guidance / Reference |
| :---- | :---- | :---- | :---- | :---- |
| **7.1.1** | \[CRA REQUIREMENT\] The organization must maintain a Technical File for each in-scope product containing all elements required by CRA Annex VII: product description, design documents, cybersecurity risk assessment, SDL evidence, security test results, SBOM, connections audit, EU Declaration of Conformity, and EOL declaration. | ☐ Yes   ☐ No   ☐ Partial |   | Technical File index; storage location; access control. CRA Annex VII checklist. |
| **7.1.2** | \[CRA REQUIREMENT\] The organization must perform and maintain a documented cybersecurity risk assessment including threat modelling (attack surface, threat actors, attack vectors) with a documented methodology. The assessment must be performed before development begins and updated throughout the product lifecycle. | ☐ Yes   ☐ No   ☐ Partial |   | Risk assessment report; threat model document; update history reviewed at each major release. |
| **7.1.3** | \[CRA REQUIREMENT\] The Technical File must be accessible to designated personnel and must be capable of being produced to a market surveillance authority (MSA) within the legally required timeframe. | ☐ Yes   ☐ No   ☐ Partial |   | File retrieval SLA; named custodian. |
| **7.1.4** | \[CRA REQUIREMENT\] SBOMs included in the Technical File must be the same machine-readable artifacts generated by the CI/CD pipeline (no manual transcription). | ☐ Yes   ☐ No   ☐ Partial |   | Pipeline artifact link to Technical File storage. |
| **7.1.5** | \[CRA REQUIREMENT\] Technical documentation must be retained for at least 10 years after placement on the market, or for the expected product lifetime or support period if longer (CRA Art. 13(13)). | ☐ Yes   ☐ No   ☐ Partial |   | Retention policy; archive location; destruction schedule. |
| **7.1.6** | \[GOOD PRACTICE\] The organization should maintain a documented MSA response workflow defining how a Technical File request from a market surveillance authority is received, processed, and fulfilled within the legally required timeframe. | ☐ Yes   ☐ No   ☐ Partial |   | MSA response SOP; named responsible contact; estimated fulfillment timeline. |

 

## **7.2 Downstream & Customer Provisioning**

 

| Ref | Requirement | Conformant? (Yes / No / Partial) | Evidence & Rationale | Guidance / Reference |
| :---- | :---- | :---- | :---- | :---- |
| **7.2.1** | \[CRA REQUIREMENT\] The SBOM must be made available to market surveillance authorities upon reasoned request as part of the Technical File (CRA Annex VII). \[GOOD PRACTICE\] SBOMs may be made available to customers and integrators alongside each product release; this is strongly recommended practice but is not a CRA legal obligation enforceable against the manufacturer. | ☐ Yes   ☐ No   ☐ Partial |   | SBOM delivery mechanism (portal, API, package metadata, attestation) where voluntarily provided; MSA Technical File access procedure. |
| **7.2.2** | \[GOOD PRACTICE\] Security advisories and vulnerability exploitability statements should be delivered to downstream integrators through a documented channel. | ☐ Yes   ☐ No   ☐ Partial |   | Advisory distribution list; portal URL; API endpoint. |
| **7.2.3** | \[GOOD PRACTICE\] Contractual or technical mechanisms should be used to ensure downstream integrators receive timely security updates for embedded components. | ☐ Yes   ☐ No   ☐ Partial |   | Contract clause or SLA; notification mechanism. |
| **7.2.4** | \[GOOD PRACTICE\] A process may exist to handle customer requests for additional SBOM detail or vulnerability information.  | ☐ Yes   ☐ No   ☐ Partial |   | Customer-facing SBOM request procedure; support ticket template. |
| **7.2.5** | \[GOOD PRACTICE\] Where the product transmits telemetry, the organization should document and validate that telemetry data collection is limited to what is necessary and that outbound connections are audited. | ☐ Yes   ☐ No   ☐ Partial |   | Telemetry data inventory; outbound connections audit log; data minimisation policy. |

 

## **7.3 User-Facing Documentation (CRA Art. 13(18) / Annex II)**

CRA Art. 13(18) and Annex II require manufacturers to provide clear and understandable information and instructions to users. Note: CRA Art. 24 governs OSS Steward obligations, not manufacturer user-facing documentation.

 

| Ref | Requirement | Conformant? (Yes / No / Partial) | Evidence & Rationale | Guidance / Reference |
| :---- | :---- | :---- | :---- | :---- |
| **7.3.1** | \[CRA REQUIREMENT\] The organization must provide information and instructions to users in a language easily understood by them, covering: intended use, cybersecurity properties, how to configure security settings, the declared end-of-support date, and how to report vulnerabilities (CRA Art. 13(18) / Annex II). | ☐ Yes   ☐ No   ☐ Partial |   | User manual or README; Annex II compliance checklist; language coverage evidence. |
| **7.3.2** | \[CRA REQUIREMENT\] The EU DoC must be kept up-to-date and must be updated upon any significant product change affecting the conformity assessment basis. | ☐ Yes   ☐ No   ☐ Partial |   | DoC version history; update procedure documentation. |
| **7.3.3** | \[CRA REQUIREMENT\] The CE marking (or, for software-only products distributed digitally, a digital CE marking accessible on the product website) must be affixed before EU market placement (CRA Art. 30). | ☐ Yes   ☐ No   ☐ Partial |   | CE mark placement evidence (screenshot, label photograph, or packaging proof); digital CE mark URL. |
| **7.3.4** | \[CRA REQUIREMENT\] The EU DoC must be made available to market surveillance authorities and must be retained for at least 10 years after last placement on the EU market. | ☐ Yes   ☐ No   ☐ Partial |   | DoC storage location; access control; retention policy entry. |

 

## **7.4 EU Declaration of Conformity & CE Marking (CRA Art. 28 & 30\)**

 

| Ref | Requirement | Conformant? (Yes / No / Partial) | Evidence & Rationale | Guidance / Reference |
| :---- | :---- | :---- | :---- | :---- |
| **7.4.1** | \[LEGAL REVIEW / IMPLEMENTATION CONTROL\] The organization must document whether the manufacturer is established in the Union for the product and, if not, conduct product-specific legal analysis to determine whether applicable Union harmonisation legislation requires an EU-established responsible economic operator. CRA Article 18 permits, but does not require, appointment of an authorised representative by written mandate. Any Article 4 Regulation (EU) 2019/1020 or other Union-act obligations must be assessed separately before market placement. | ☐ Yes   ☐ No   ☐ Partial |   | Legal determination memo; EU establishment confirmation or, where applicable, AR mandate, importer agreement, or fulfillment provider contract. |
| **7.4.2** | \[CRA REQUIREMENT\] Where the AR pathway is chosen, a written mandate must be executed before placing any product on the EU market. The mandate must specify at minimum the obligations defined in CRA Art. 18(3): (a) keeping the EU DoC and Technical File available to MSAs for at least 10 years or the support period whichever is longer; (b) providing MSAs with information and documentation necessary to demonstrate conformity upon reasoned request; (c) cooperating with MSAs on any action taken to eliminate risks posed by the product. | ☐ Yes   ☐ No   ☐ Partial |   | Signed AR mandate; mandate text confirming Art. 18(3)(a-c) obligations; AR's EU address and contact details. |
| **7.4.3** | \[LEGAL REVIEW / IMPLEMENTATION CONTROL\] Where an authorised representative pathway is used, the organization must maintain the written mandate required by CRA Article 18 and confirm, through product-specific legal analysis, whether any product, packaging, documentation, or other contact-detail marking obligations apply under CRA or other applicable Union harmonisation legislation. CRA Article 18 does not itself impose an authorised-representative product-labeling requirement. | ☐ Yes   ☐ No   ☐ Partial |   | Product label or documentation showing AR details. |
| **7.4.4** | \[CRA REQUIREMENT\] Where the AR pathway is chosen, the AR must be provided with a copy of the EU DoC and Technical File and must be empowered to act on behalf of the manufacturer in dealings with market surveillance authorities. | ☐ Yes   ☐ No   ☐ Partial |   | Document transmission record; access confirmation from AR. |
| **7.4.5** | \[GOOD PRACTICE\] Where the AR pathway is chosen, the organization should maintain documented operational procedures governing how the AR fulfills the Art. 18(3) obligations in practice, including escalation paths and communication protocols with MSAs. | ☐ Yes   ☐ No   ☐ Partial |   | AR operational procedure document; communication protocol; escalation path. |

 

| Ref | Requirement | Conformant? (Yes / No / Partial) | Evidence & Rationale | Guidance / Reference |
| :---- | :---- | :---- | :---- | :---- |

 

 

# **Section 8: Cross-Framework Integration**

The CRA sits within a broader EU digital regulatory stack. This section ensures the organization identifies where CRA conformity artifacts serve multiple regulatory obligations simultaneously.

 

## **8.1 CRA and NIS2**

 

| Ref | Requirement | Conformant? (Yes / No / Partial) | Evidence & Rationale | Guidance / Reference |
| :---- | :---- | :---- | :---- | :---- |
| **8.1.1** | \[GOOD PRACTICE\] The organization should determine whether it is subject to NIS2 (Directive (EU) 2022/2555) as an essential or important entity independently of its CRA manufacturer obligations. Where both apply, a mapping should exist showing how CRA product security artifacts satisfy NIS2 supply chain security assessment requirements (NIS2 Art. 21(2)(d)). | ☐ Yes   ☐ No   ☐ Partial |   | Dual-framework mapping document; NIS2 supply chain security procedure referencing CRA conformity artifacts. |
| **8.1.2** | \[GOOD PRACTICE\] For organizations subject to both NIS2 and CRA, governance, risk assessment, and incident response processes should be designed to serve both frameworks on shared rather than parallel tracks where the underlying obligation is equivalent. | ☐ Yes   ☐ No   ☐ Partial |   | Integrated GRC framework document; evidence that NIS2 incident reporting and CRA Art. 14 notification runbooks share escalation paths and RACI roles. |

 

## **8.2 CRA and AI Act**

 

| Ref | Requirement | Conformant? (Yes / No / Partial) | Evidence & Rationale | Guidance / Reference |
| :---- | :---- | :---- | :---- | :---- |
| **8.2.1** | \[GOOD PRACTICE\] For any product that is both a PDE under CRA and a high-risk AI system under the AI Act (Regulation (EU) 2024/1689), the organization should document that CRA Annex I compliance satisfies the AI Act Art. 15 cybersecurity requirements for that product, per CRA Art. 12\. | ☐ Yes   ☐ No   ☐ Partial |   | AI Act / CRA dual-scope determination per product; mapping from CRA Annex I to AI Act Art. 15\. |
| **8.2.2** | \[GOOD PRACTICE\] For Important or Critical CRA products that are also high-risk AI systems, the organization should document that CRA conformity assessment requirements take precedence over AI Act internal control provisions for cybersecurity aspects (per CRA Art. 12). This precedence should be recorded in the product conformity assessment plan. | ☐ Yes   ☐ No   ☐ Partial |   | Precedence determination in conformity assessment plan; legal review sign-off. |

 

## **8.3 CRA and DORA**

 

| Ref | Requirement | Conformant? (Yes / No / Partial) | Evidence & Rationale | Guidance / Reference |
| :---- | :---- | :---- | :---- | :---- |
| **8.3.1** | \[GOOD PRACTICE\] For organizations supplying digital products to financial entities subject to DORA (Regulation (EU) 2022/2554), CRA conformity documentation (Technical File, DoC, SBOM, vulnerability handling SLAs) should be identified as relevant input to DORA ICT third-party risk management due diligence and should be made available to financial entity customers on request. | ☐ Yes   ☐ No   ☐ Partial |   | Customer-facing documentation list including DORA-relevant CRA artifacts; reference to DORA Art. 28-30. |

 

## **8.4 CRA and Data Act**

 

| Ref | Requirement | Conformant? (Yes / No / Partial) | Evidence & Rationale | Guidance / Reference |
| :---- | :---- | :---- | :---- | :---- |
| **8.4.1** | \[GOOD PRACTICE\] For connected products that simultaneously qualify under the Data Act (Regulation (EU) 2023/2854), overlapping obligations around data access, documentation, and user transparency should be identified, and the compliance program should address both regulations in a coordinated manner. | ☐ Yes   ☐ No   ☐ Partial |   | Data Act / CRA product scope overlap assessment; coordinated documentation plan. |

 

## **8.5 CRA and eIDAS**

eIDAS 2.0 (Regulation (EU) 2024/1183) governs electronic identification and trust services. Where CRA products interact with eIDAS-governed identity services or where an Authorized Representative operates under eIDAS-regulated digital identity, the interaction between the two frameworks should be assessed.

 

| Ref | Requirement | Conformant? (Yes / No / Partial) | Evidence & Rationale | Guidance / Reference |
| :---- | :---- | :---- | :---- | :---- |
| **8.5.1** | \[GOOD PRACTICE\] For products that interact with eIDAS-governed electronic identification or trust services, the organization should assess whether eIDAS 2.0 (Regulation (EU) 2024/1183) creates obligations in addition to CRA, particularly where the product functions as a relying party or issues electronic attestations. | ☐ Yes   ☐ No   ☐ Partial |   | Legal determination memo; eIDAS / CRA dual-scope assessment; reference to Regulation (EU) 2024/1183. |
| **8.5.2** | \[GOOD PRACTICE\] Where the organization appoints an EU Authorized Representative and that AR operates using eIDAS-regulated digital identity services, the organization should document how the eIDAS and CRA AR obligations interact and should seek legal counsel given the evolving hybridization of these frameworks. | ☐ Yes   ☐ No   ☐ Partial |   | Legal counsel assessment; AR mandate review against eIDAS identity obligations; reference to CRA Art. 18 and eIDAS 2.0 Art. 45\. |

 

 

# **Section 9: Procurement & Buyer-Side Obligations**

The CRA changes what responsible procurement looks like. For organizations subject to NIS2, these questions are simultaneously regulatory requirements.

 

## **9.1 Vendor CRA Qualification**

 

| Ref | Requirement | Conformant? (Yes / No / Partial) | Evidence & Rationale | Guidance / Reference |
| :---- | :---- | :---- | :---- | :---- |
| **9.1.1** | \[GOOD PRACTICE\] The vendor evaluation process should require suppliers of products with digital elements to confirm: (a) the CRA product classification; (b) the conformity pathway used; (c) the declared support period end date. Note: The notified body used is published on the EU DoC and need not be separately collected. | ☐ Yes   ☐ No   ☐ Partial |   | Updated vendor questionnaire or RFP template; example completed vendor response. |
| **9.1.2** | \[GOOD PRACTICE\] Procurement contracts for products with digital elements should include at minimum: (a) CRA conformity confirmation; (b) commitment to maintain vulnerability handling for the declared support period; (c) notification obligation to the buyer upon discovery of an actively exploited vulnerability in a supplied product. Note: Contractual access to Technical File or DoC is a good practice and not a CRA statutory obligation. | ☐ Yes   ☐ No   ☐ Partial |   | Updated standard contract template with CRA clauses; legal review sign-off. |
| **9.1.3** | \[GOOD PRACTICE\] The organization should ask suppliers whether they produce SBOMs for procured products, in what format, and whether they are available. For high-assurance procurement, SBOM availability should be a mandatory procurement criterion. | ☐ Yes   ☐ No   ☐ Partial |   | Supplier SBOM availability requirement in procurement policy; evidence of SBOM receipt or supplier declaration. |
| **9.1.4** | \[GOOD PRACTICE\] The organization should verify that suppliers have credible processes to detect and report actively exploited vulnerabilities in shipped components in a timely manner consistent with CRA Art. 14 obligations. | ☐ Yes   ☐ No   ☐ Partial |   | Supplier due-diligence question on vulnerability monitoring capability; documented assessment outcome per supplier. |
| **9.1.5** | \[GOOD PRACTICE\] The organization should implement a supplier risk tiering model classifying vendors by the criticality of the components they supply, the security maturity of their CRA compliance program, and their vulnerability response track record. | ☐ Yes   ☐ No   ☐ Partial |   | Supplier risk tier matrix; tiering criteria document; example tier assignment records. |

 

 

# **Implementation Roadmap**

The following phased model provides a structured approach to achieving self-certification.

 

| Phase | Key Action | Typical Owner | Target |
| :---- | :---- | :---- | :---- |
| **PRIORITY \- Art. 14 RACI (§4.4-4.5)** | Confirm current CRA Single Reporting Platform (SRP) registration process directly with ENISA and national CSIRT or MSA; assign named owners for 24h/72h/14-day notification stages; document severe security incident definition; complete at least one test submission or equivalent preparatory contact before the deadline. |   | **Before 11 Sep 2026 \- IMMEDIATE** |
| **1 \- Scope & Categorization** | Determine organizational role using §1 applicability table; confirm PDE vs SaaS (§2.5.1); complete EU establishment determination (§2.5.2/§7.4); complete risk classification including Art. 32(5) FOSS determination (§2.5.3-2.5.9); complete cybersecurity risk assessment (§2.6). | Legal \+ CISO | Month 1-2 |
| **2 \- Policy & Governance** | Draft and approve CRA policy (§2.1); assign responsibilities (§2.2); training (§2.3); M/606/PT1/PT3 monitoring (§2.7). | Legal \+ CISO | Month 1-3 |
| **3 \- SBOM & SDLC** | Generate SBOMs per CRA original text covering at the very least top-level dependencies (§3.1); validate completeness including license information fields (§3.2); establish provenance signing (§3.3); implement SAST/DAST, threat modeling, release gate (§3.4); importer/distributor checklist (§3.5). | Platform Eng. | Month 2-4 |
| **4 \- Vuln Pipeline** | Deploy continuous monitoring including EUVD and KEV feeds (§4.1); exploitability assessment (§4.2); decision criteria (§4.3); CVD policy (§4.4). | SecOps | Month 3-5 |
| **5 \- Vulnerability Exchange & Disclosure** | Implement exploitability exchange workflow (§4.2); integrate SRP Art. 14 reporting runbook (§4.4); train responders; run tabletop exercise (§4.5). | SecOps \+ Legal | Month 4-6 |
| **6 \- OSS Governance** | Steward vs manufacturer determination per Art. 3(14), Recitals 18 and 19, Art. 24 (§5.1); upstream due-diligence (§5.1.6); publish SECURITY.md per Art. 24(1) (§5.2). | OSS Program | Month 5-7 |
| **7 \- Support Period** | Define and publish support periods; document secure update mechanism; EoL comms (§6.1). | Product \+ Legal | Month 5-7 |
| **8 \- Technical File & CE** | Compile Technical Files; draft EU DoC; affix CE marking; confirm AR/importer/fulfillment arrangement (§7.1-7.4). | Compliance PM | Month 6-8 |
| **8A \- Cross-Framework** | NIS2 (§8.1); AI Act (§8.2); DORA (§8.3); Data Act (§8.4); eIDAS (§8.5). | Legal \+ CISO | Month 7-9 |
| **8B \- Procurement** | Vendor CRA qualification (§9.1). | Legal \+ Procurement | Month 7-9 |
| **9 \- Self-Certification** | Complete this checklist; remediate gaps; conduct internal audit (§2.4.5); file conformance claim. Total items: 170\. | CRA Program Mgr | Month 8-10 |
| **10 \- Continuous Ops** | Annual review (§2.4); training refresh; SBOM quality; advisory cadence; annual tabletop exercise; PT1/PT3 monitoring. | All owners | Ongoing |

 

 

# **Self-Certification Summary**

**Legal notice:** Completing or signing this checklist does not in itself constitute a CRA conformity assessment, an EU Declaration of Conformity, or evidence of lawful CE marking. Self-certification (Module A) is available according to the applicable Article 32 conformity-assessment procedure, including for qualifying Annex III FOSS products where Article 32(5) conditions are met and Article 31 technical documentation is publicly available at market placement. A conformity claim requires: (a) completion of all applicable checklist items with supporting evidence; (b) issuance of an EU Declaration of Conformity per Annex V; (c) proper CE marking per Art. 30\. Organizations are advised to seek qualified legal counsel before making a formal conformity claim.

 

Upon completing all checklist items, complete the attestation below.

 

| Organization | \[INSERT: Full legal entity name of manufacturer\] |
| :---- | :---- |
| **Organizational Role(s)** | \[INSERT: Manufacturer / Importer / Distributor / OSS Steward \- circle all that apply\] |
| **Product / Scope** | \[INSERT: Product name(s) and version(s) in scope\] |
| **Self-Certification Date** | \[Date\] |
| **CRA Program Manager** | \[INSERT: Name, Title \- Signature required for formal submission\] |
| **Next Review Date** | \[Date \- max 12 months from above\] |
| **Items answered Yes** | \[  \] of 170 total checklist items |
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
| **PDE (Product with Digital Elements)** | A software or hardware product and its remote data processing solutions, including separately marketed software or hardware components (CRA Art. 3(1)); the direct or indirect data-connection scope test is addressed under CRA Art. 2(1). |
| **SBOM (Software Bill of Materials)** | A machine-readable inventory of software components in a product, covering at the very least the top-level dependencies, including component identifiers, versions, suppliers, and license information (CRA Annex I Part II; ISO/IEC 18974; ISO/IEC 5230). |
| **Substantial Modification** | A modification to a product after market placement that affects compliance with essential requirements or changes the intended purpose (CRA Art. 3(30)). |
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
| Mandatory regulatory notification (Art. 14\) | Part II, §5 | 4.4.2-4.4.6, 4.5 | SRP submission runbook; RACI; tabletop exercise or internal reporting simulation record |
| SBOM documentation (covering at least top-level dependencies) | Part II, §6 | 3.1, 3.2 | Machine-readable SBOM; CISA 2025 minimum-element field coverage; license information fields (CISA 2025; ISO/IEC 18974/5230); file/snippet-level reference handling where applicable |
| Secure development lifecycle | Part I (general) | 3.3, 3.4, 3.6, 5.3 | Build provenance; secrets management; signing; SAST/DAST; third-party software qualification; self-maintained OSS controls where applicable |
| Risk assessment documented | CRA Art. 13(2)–(4); Annex VII | 2.6, 7.1.1, 7.1.2 | Risk assessment report; threat model; update history |
| Technical file compiled | Annex VII | 7.1 | Technical File index; storage location; MSA retrieval SLA |
| EU Declaration of Conformity (Module A per Annex VIII Part 1\) | Annex V \+ Annex VIII Part 1 | 7.3.1-7.3.4 | Completed DoC per Annex V; CE mark evidence; retention record |

 

 

# **Appendix C \- ISO/IEC 18974 & OWASP SAMM Cross-Reference Mapping**

This mapping shows how ISO/IEC 18974 clauses and OWASP SAMM practices align with checklist sections. PT1/PT3 placeholder rows will be updated when final versions are published.

 

| ISO/IEC 18974 Clause | Requirement Summary | CRA Checklist Section(s) | OWASP SAMM Reference |
| :---- | :---- | :---- | :---- |
| **§3.1.1** | Security policy for open source | §2.1 CRA Policy, §5.1 | SAMM: Governance \> Policy & Compliance |
| **§3.1.2** | Competence and awareness | §2.3 Competence & Training | SAMM: Governance \> Education & Guidance |
| **§3.2.1** | SBOM process and tooling | §3.1 SBOM Generation | SAMM: Implementation \> Secure Build |
| **§3.2.2** | SBOM completeness and data quality (incl. license information per ISO/IEC 5230\) | §3.2 Data Quality, including file/snippet reference handling | SAMM: Implementation \> Secure Build |
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

 

 

# **Annex D — External References and Adoption**

The live external references and adoption register is maintained separately from this checklist to allow public references, confirmations, and community adoption evidence to be updated without changing the normative checklist content.

Register: [ANNEX_D_EXTERNAL_REFERENCES_AND_ADOPTION.md](https://github.com/OpenChain-Project/CRA-Compliance/blob/main/ANNEX_D_EXTERNAL_REFERENCES_AND_ADOPTION.md)

Inclusion in the register means that an organization, public forum, event, or resource has referenced, used, evaluated, or relied on the OpenChain CRA Checklist. Inclusion does not imply endorsement, certification, legal approval, OpenChain membership, sponsorship, audit status, or a statement of CRA compliance.


# **Annex E — Contributors and Reviewers**

The live contributor and reviewer register is maintained separately from this checklist so attribution, organizational context, and contribution details can be updated without changing the normative checklist content.

Register: [CONTRIBUTORS.md](https://github.com/OpenChain-Project/CRA-Compliance/blob/main/CONTRIBUTORS.md)

# **Annex F — Revision History**

The revision history is maintained separately from this checklist to preserve a concise public record of authorship, review cycles, and major changes while keeping the checklist front matter aligned with OpenChain document style.

Register: [REVISION_HISTORY.md](https://github.com/OpenChain-Project/CRA-Compliance/blob/main/REVISION_HISTORY.md)


# **References & Implementation Resources**

References marked as "draft" or "pending" are informational only and non-binding until formally adopted or published. This applies to all such references including those cited in §2.5.1, §2.7, §5.1.6, and Annex C.

 

**Regulatory & Legal**

 

●  EU Cyber Resilience Act (full text) \- [eur-lex.europa.eu/eli/reg/2024/2847/oj/eng](https://eur-lex.europa.eu/eli/reg/2024/2847/oj/eng)

●  Commission guidance C(2026) 5252 (final, 27 Jul 2026\) \- [digital-strategy.ec.europa.eu](https://digital-strategy.ec.europa.eu/en/library/commission-publishes-new-guidance-support-timely-cyber-resilience-act-implementation)

●  Implementing Regulation (EU) 2025/2392 \- Product category technical descriptions \- [eur-lex.europa.eu/legal-content/EN/TXT/?uri=CELEX:32025R2392](https://eur-lex.europa.eu/legal-content/EN/TXT/?uri=CELEX:32025R2392)

●  CRA Compliance Matrix (independent) \- [cyberresilienceact.eu/compliance-matrix.html](https://www.cyberresilienceact.eu/compliance-matrix.html)

●  ENISA EU Vulnerability Database (EUVD) \- [euvd.enisa.europa.eu](https://euvd.enisa.europa.eu)

●  Commission Delegated Regulation (EU) 2026/881 \- notification dissemination delay conditions

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

 

●  SPDX Specification 3.x \- spdx.github.io/spdx-spec

●  SPDX Hardware profile (SPDX 3.x) \- spdx.dev

●  CycloneDX Specification 1.7 / ECMA-424 \- cyclonedx.org / ecma-international.org

●  CycloneDX HBOM guidance \- cyclonedx.org

●  CISA 2025 Minimum Elements for a Software Bill of Materials (SBOM) (informational reference replacing the 2021 NTIA minimum elements) \- cisa.gov

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
