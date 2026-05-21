# name
medical-device-regulatory-review-report-generator

# description
Create a comprehensive, regulator-ready medical device regulatory review report in Microsoft Word format based on user-provided device information, testing scope, and target regulatory pathways (TFDA, FDA 510(k), CE MDR).

⚠️ Use this skill whenever the user:
- Mentions generating, compiling, or optimizing **regulatory review reports**, **testing summaries**, or **technical documentation**
- Requests **Word (.docx) outputs** for medical device compliance, testing, or submission
- Refers to **TFDA**, **FDA 510(k)**, **CE MDR**, **IEC**, **ISO**, **DICOM**, **laser**, **imaging**, or **software medical devices**
- Wants a **product specification × review result**, **test matrix**, or **evidence mapping table**
- Is preparing or reviewing **510(k) submissions**, **Technical Documentation**, **Design History File (DHF)**, or **Essential Requirements / GSPR mapping**

This skill generates:
- A structured **Word (.docx) regulatory review report**
- A **Product Specification × Review Result master table**
- Regulatory-aligned sections covering **safety, performance, and compliance**
- Pre-filled practical examples for **software medical devices, imaging devices, and laser products**
- Content aligned with **TFDA review logic**, **FDA 510(k) expectations**, and **CE MDR Technical Documentation (Annex II & III)**

The output is designed to be reviewer-friendly, traceable, and directly usable for submissions without restructuring.

# compatibility
- Tools: python-docx
- Output format: Microsoft Word (.docx)
- Regulatory frameworks supported:
  - TFDA Medical Device Technical Documentation
  - FDA 510(k) (21 CFR, eSTAR-aligned structure)
  - EU MDR (Regulation (EU) 2017/745)
- Standards commonly referenced:
  - IEC 60601 series
  - IEC 62304
  - ISO 10993
  - IEC 60825-1
  - IEC 62471
  - IEC 60601-2-x series
  - DICOM Conformance
  - NEMA NU 2

# skill_behavior
When this skill is triggered, it should:

1. **Identify target regulatory pathways**
   - Determine whether the report is for TFDA, FDA 510(k), CE MDR, or multiple pathways
   - Apply neutral terminology accepted by all authorities where possible

2. **Generate a Word (.docx) report with the following structure**
   - Cover page (device name, manufacturer, regulatory scope)
   - Table of contents
   - Section 1: Product Overview
   - Section 2: Product Specification × Review Result Master Table
   - Section 3: Safety and Performance Standards Review
   - Section 4: Software, Imaging, or Laser-Specific Requirements (as applicable)
   - Section 5: Summary of Compliance and Supporting Evidence
   - Section 6: Conclusion and Regulatory Readiness Statement

3. **Create a Product Specification × Review Result master table**
   - Two primary columns:
     - Product Specification / Regulatory Requirement
     - Review Result / Supporting Documentation
   - Include report name, document number, issuing body, and applicable product
   - Ensure each row is traceable to a test report or technical file

4. **Pre-fill practical examples**
   - Software Medical Device (SaMD): IEC 62304, software level of concern, data integrity
   - Imaging Device / DICOM: Image transmission, compatibility, IEC 60601-1/-1-2
   - Laser Product: IEC 60825-1, optical output parameters, safety classification

5. **Ensure consistency with submission artifacts**
   - Align terminology and structure with:
     - FDA 510(k) sections and test report matrices
     - CE MDR Annex II / Annex III Technical Documentation
     - Internal DHF and verification & validation records

6. **Maintain reviewer-friendly principles**
   - Clear, concise wording
   - Explicit references to standards and documents
   - No diagnostic or clinical claims unless explicitly provided by the user
   - Ready for direct submission or minor customization

# evaluation_criteria
A successfully generated report should:
- Be immediately usable as a regulatory submission attachment
- Require no structural rework for TFDA, FDA, or CE reviewers
- Provide clear traceability between requirements and evidence
- Be understandable to both regulatory reviewers and quality engineers
- Be delivered entirely in Microsoft Word format
