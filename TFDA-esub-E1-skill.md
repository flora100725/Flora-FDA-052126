# skill.md

## Skill Name
Medical Device Regulatory Review Report Generator (FDA-Friendly Word Output)

## Skill Purpose
This skill is designed to automatically generate a **Detailed Medical Device Regulatory Review Report** in Microsoft Word (.docx) format.

The generated report is intended to support:
- FDA 510(k) Premarket Notification submissions
- Supporting Test Report Summaries
- Technical Documentation for regulatory review
- Internal Quality Assurance (QA) and Regulatory Affairs (RA) assessments

The structure, terminology, and tone are aligned with FDA reviewer expectations and IEC/ISO standards.

---

## Target Output Format
- Microsoft Word (.docx)
- Structured regulatory document
- Editable tables
- Formal, objective regulatory language
- English (U.S.)

---

## Input Schema

### Required Inputs
- Product Name
- Manufacturer
- Regulatory Submission Purpose  
  (e.g., FDA 510(k), TFDA, CE MDR)
- Intended Product Type  
  (Software, Hardware, Energy-based, Imaging System)

### Optional Inputs
- Document Number Prefix (e.g., QA-REP-XXX)
- Test Laboratory / Issuing Organization
- Software-only Medical Device (Yes / No)

---

## Core Workflow Logic

### Step 1 – Generate Document Header
Automatically create the following document elements:
- Document Title: **Product Specification and Regulatory Review Report**
- Product Name
- Manufacturer
- Regulatory Purpose
- Document Number (auto-generated if not provided)
- Date of Issue

---

### Step 2 – Generate Review Sections Based on Standardized Templates
For each applicable review item, generate:
- A dedicated section (Heading level)
- A standardized review table

#### Standard Review Table Format (Fixed)
| Field | Description |
|---|---|
| Report Title | |
| Document Number | |
| Issuing Organization | |
| Applicable Product(s) | |

All sections shall be generated even if deemed *Not Applicable*, with rationale provided where appropriate.

---

## Regulatory Review Item Template Library

### Performance Specifications

### Electrical Safety
- IEC 60601-1

### Electromagnetic Compatibility (EMC)
- IEC 60601-1-2

### Biocompatibility Evaluation
- ISO 10993 Series

### Alarm Systems
- IEC 60601-1-8  
- (Applicable to infusion pumps, central monitoring systems, etc.)

### Laser Hair Growth Devices
- Output power density
- Output power accuracy
- Wavelength range
- Timer functionality

### Laser Product Safety
- IEC 60825-1

### Photobiological Safety
- IEC 62471
- Applicable wavelength range: 200 nm to 3000 nm
- Includes LED products (excluding lasers)
- May apply to infrared products (e.g., infrared lamps)

### Laser Systems for Relief of Minor Muscle and Joint Pain
- Skin Tone Adjustment output power and wavelength ratio
- Pulse frequency
- Pulse duration

### Ophthalmic Instruments
- ISO 15004-1 (General requirements)
- ISO 15004-2 (Light hazard protection)

### Direct Ophthalmoscopes
- ISO 10942

### Retinoscopes
- ISO 12865

### Corneal Topography Devices
- ISO 19980

### Visual Function Analyzers
- Tear film analysis
- Dry eye assessment

### Diagnostic Ultrasound Safety
- IEC 60601-2-37
- Transducer surface temperature
- Thermal Index (TI)
- Mechanical Index (MI)
- Ultrasound energy risk assessment
- Freeze function
- Center frequency
- Axial and lateral resolution

### Ultrasound Physiotherapy Equipment
- IEC 60601-2-5
- IEC 61689 (Measurement methods, 0.5–5 MHz)

### DICOM Image Communication Standard
- DICOM conformance and interoperability

### X-Ray Equipment
- IEC 62220-1 (Image quality of flat-panel detectors)
- Detector-to-host system compatibility
- Dose Area Product (DAP)
- X-ray tube assemblies (IEC 60601-2-28)
- Radiation protection (IEC 60601-1-3)
- General diagnostic X-ray systems (IEC 60601-2-54)
- Interventional X-ray systems (IEC 60601-2-43)

### CT X-Ray Equipment
- IEC 60601-2-44

### Radiotherapy Equipment – Coordinates and Movements
- IEC 61217

### Medical Electron Accelerators
- IEC 60601-2-1  
  (Energy range: 1 MeV to 50 MeV)

### Magnetic Resonance Imaging (MRI) Equipment
- IEC 60601-2-33

### Positron Emission Tomography (PET)
- NEMA NU 2-2018

### Infusion Pumps
- IEC 60601-2-24

---

## Advanced AI Capabilities

### Feature 1 – Applicability Determination and Rationale
The AI shall:
- Assess product type and intended use
- Automatically classify each review item as:
  - Applicable
  - Not Applicable
- Provide a concise regulatory rationale for Not Applicable items
  (FDA-style justification)

---

### Feature 2 – Intended Use and Claims Consistency Check
The AI shall:
- Identify potentially high-risk terms such as:
  - “diagnose”
  - “detect”
  - “treat”
- Flag inconsistencies with FDA 510(k) regulatory expectations
- Provide neutral, reviewer-friendly wording recommendations

---

### Feature 3 – Regulatory Mapping Tags
Each section shall include internal tags indicating relevance to:
- FDA 510(k) Supporting Documentation
- IEC / ISO compliance evidence
- Technical File / Design Dossier structure

---

## Output Rules
- Do not assume test results
- Do not generate numerical data
- Do not fabricate compliance statements
- Preserve space for manual data entry
- Output must be fully editable in Microsoft Word (.docx)

---

## Regulatory Scope
- FDA 510(k)
- IEC 60601 Series
- ISO 10993 / ISO 15004 / ISO 19980
- NEMA Standards
- CE MDR Technical Documentation alignment

---

## End of Skill
