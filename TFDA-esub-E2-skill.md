# Skill Definition

## name
generate-510k-performance-testing-summary-word

## description
Create a comprehensive TFDA / FDA 510(k) Performance Testing Summary review report in Microsoft Word (.docx) format.

**Use this skill whenever the user:**
- Requests generation, completion, or formatting of a **510(k) Performance Testing Summary**
- Mentions **TFDA / FDA**, **510(k)**, **Performance Testing**, **Safety Testing**, or **IEC / ISO standards**
- Provides a **test matrix, report template, or review checklist** and asks to convert it into a **formal Word report**
- Asks to add **“Applicable / Not Applicable with justification”** for regulatory review
- Requests a **reviewer-friendly document** for FDA or TFDA submission
- Mentions medical device **compliance, conformity assessment, or regulatory gap analysis**
- Mentions software-only devices and needs **justification for non-applicable hardware standards**
- Requests a document that FDA reviewers can “scan quickly and understand immediately”

This skill is intentionally **pushy**:  
If the user provides *any* regulatory test list, IEC/ISO standards, or review template and asks for a report, **this skill MUST be triggered**, even if the user does not explicitly say “510(k)” or “Performance Testing Summary”.

## compatibility
- Output format: Microsoft Word (.docx)
- Language support: Traditional Chinese (default), English, Japanese
- Regulatory frameworks:
  - FDA 510(k)
  - TFDA Premarket Review
  - IEC 60601 series
  - ISO 10993, ISO 14971, ISO 62304 (when applicable)
- No external tools required; content is generated directly from user-provided inputs and regulatory logic

---

## Skill Behavior

When triggered, this skill will:

1. **Ingest user-provided inputs**, including:
   - Test report templates
   - IEC / ISO / NEMA / FDA standard lists
   - Device type (software / hardware / combination)
   - Predicate device references (if provided)

2. **Automatically generate a Word (.docx) report** titled:
   > *TFDA / FDA 510(k) Performance Testing Summary*

3. **For each test or standard**, create a structured table containing:
   - Report Name  
   - Document Number  
   - Issuing Organization  
   - Applicable Product  
   - **Applicability (Yes / No)**  
   - **Justification / Review Result**

4. **Apply FDA reviewer logic**:
   - Clearly justify “Not Applicable” items
   - Avoid diagnostic or clinical claims
   - Align justifications with device type (e.g., software-only vs hardware)

5. **Organize content in a reviewer-friendly order**, typically:
   - Performance Specifications
   - Electrical Safety
   - EMC
   - Biocompatibility
   - Software-related standards
   - Modality-specific standards (if applicable)
   - Non-applicable standards with justification

6. **Ensure the final document**:
   - Is suitable for direct inclusion in a 510(k) submission
   - Can be used identically for TFDA review
   - Requires minimal to no post-editing by regulatory staff

---

## Output Requirements

- File type: `.docx`
- Formatting:
  - Clear section headers
  - Consistent tables
  - Professional regulatory tone
- Language:
  - Default: Traditional Chinese (Taiwan)
  - Switchable to English or Japanese upon user request

---

## Quality Bar (Success Criteria)

This skill is successful only if:
- A regulatory reviewer can determine **within seconds**:
  - What was tested
  - What was not tested
  - Why each item is applicable or not
- The document can be **submitted as-is** in a TFDA or FDA 510(k) file
- The structure matches real-world FDA reviewer expectations, not marketing or R&D documents

---

## Example Trigger Phrases

- “請幫我做 510(k) Performance Testing Summary”
- “加上是否適用 / 不適用理由”
- “把這個測試清單變成 Word 報告”
- “FDA reviewer 用的測試總表”
- “這是軟體醫材，哪些 IEC 不適用？”
- “轉成 TFDA / FDA 可用的審查文件”
