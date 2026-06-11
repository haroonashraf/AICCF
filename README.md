# AICCF (AI Content Classification Framework)
AI Content Classification Framework for AI involvement and human accountability

AICCF is a structured, content-agnostic framework designed to classify work based on the level of AI involvement and human accountability.

It provides a simple and consistent way to describe how content is created, reviewed, and owned across different domains, including writing, code, analysis, and project deliverables.

---

# Overview

As AI becomes increasingly integrated into everyday work, distinguishing between AI-generated and human-created content is no longer sufficient.

AICCF introduces a practical model that focuses on:
- **Level of AI involvement**
- **Degree of human oversight**
- **Clear accountability and ownership**

---

# Framework Levels

**Level 1 – Fully AI-Generated (Unreviewed)**  
Content generated entirely by AI with no human validation.  
_Not suitable for production or decision-making use._

**Level 2 – AI-Generated, Human-Reviewed**  
AI-generated content that has been reviewed and validated by a human.  
_Minimum acceptable level for most practical use cases._

**Level 3 – AI-Assisted, Human-Led**  
Content primarily created by a human with AI providing support (drafting, suggestions, structuring).  
_Default working model for most scenarios._

**Level 4 – Human-Created, AI-Enhanced**  
Human-created content with minor AI assistance (e.g., grammar, formatting, optimisation).  
_High confidence with minimal AI influence._

**Level 5 – Fully Human-Created**  
Content created without any AI involvement.  
_Used where strict control or compliance is required._

---

# Principles

- Human accountability is always required  
- AI is assistive, not authoritative  
- Validation is required before reliance  
- AI involvement should be transparent where appropriate  
- Required level of oversight may vary based on risk and use case  

---

# Tags

To simplify adoption, the following tags can be used:

- `AIG-U` → AI-Generated Unreviewed  
- `AIG-R` → AI-Generated Reviewed  
- `AIA-HL` → AI-Assisted Human-Led  
- `H-AIE` → Human-Created AI-Enhanced  
- `FH` → Fully Human  

---

# Example Use Cases

- Draft content / brainstorming → `AIG-U`  
- Reports / documentation → `AIG-R` or `AIA-HL`  
- Code / technical implementation → `AIA-HL` or `H-AIE`  
- Sensitive or regulated content → `FH` or `H-AIE`  

---

# Example Disclaimers

- “This content was generated with AI assistance and reviewed by a human.”  
- “AI-generated output – requires validation before use.”  
- “Human-led work supported by AI tools.”  

---

# Applicability

This framework is content-agnostic and can be applied across:
- Articles and reports  
- Code and technical solutions  
- Data analysis and insights  
- Documentation and communication  
- End-to-end project deliverables  

---
#  AICCF Usage Syntax
------------------

AICCF supports two standard usage styles for content classification.

* * *

### Style 1 – Tag Only (Default)

**Syntax:**

`Classification: AICCF: <TAG>`

* * *

### Style 2 – Tag with Details

**Syntax:**

`Classification: AICCF: <TAG> (<DETAIL>)`


# Integration Guide (How to Use AICCF Tags)

## 1. Add a “Global Reference” (Recommended)
-----------------------------------------
In shared or long-lived contexts such as:

*   repositories
*   documentation
*   codebases

It is recommended to include a reference to AICCF once at the beginning to ensure clarity and traceability.

**Recommended format:**

`This project uses AICCF v1.0. Reference: https://github.com/haroonashraf/AICCF`

* * *

**Alternative (more descriptive):**

`This project uses AICCF (AI Content Classification Framework) for content classification. Reference: https://github.com/haroonashraf/AICCF`

* * *

After this reference is defined, AICCF tags can be used independently throughout the content:

`AICCF: AIA-HL`

## 2. Markdown / Documentation (Clean & Professional)

**Style 1 - Tag Only**
```
# Earth-Like Planets Report
Classification: AICCF: AIA-HL 
This report analyses near by Earth-like planets...
```
**Style 2 - Tag with Level Name**
```
# Sales Performance Report
Classification: AICCF: AIA-HL (AI-Assisted Human-Led)
This report analyses near by Earth-like planets...
```

## 3. Technical Documentation (More Structured)
**Style 1**
```
## Metadata (Style 1)

- Classification: AICCF: AIG-R
- Author: Data Engineering Team
- Last Updated: 2026-01-09
```
**Style 2**
```
## Metadata (Style 2)

- Classification: AICCF: AIG-R (AI-Generated Reviewed)
- Author: Data Engineering Team
- Last Updated: 2026-01-09
```

## 4. Python Code Example
```python
# Classification: AICCF: AIA-HL (AI-Assisted Human-Led) 
# Python code designed by a developer assisted by AI 

import math
def AddBy1(x):
    return (x+1)

a=1
a=AddBy1(a)
print(a)
```

## 5. SQL Code - Style 1
```sql
-- Classification: AICCF: H-AIE (Human-Created AI-Enhanced) 
-- SQL script written by an analyst optimized with AI 

SELECT TOP 3 Stars from Sky
```

## 6. GitHub Pull Request (Best Practice) - Style 2
```MD
Markdown## Classification: AICCF: AIG-R (AI-Generated Reviewed)

## Notes
Initial implementation generated using AI and reviewed before submission.
```

## 7. Commit Message (Lightweight) - Style 2
```
Classification: AICCF: AIA-HL

Refactored transformation logic with AI-assisted suggestions
```

## 8. Data Pipeline / ETL (Very Relevant to You) - Sytle 1
```
Yamlpipeline: customer_ingestion

metadata:
  classification: AICCF: AIA-HL (AI-Assisted Human-Led) 
  description: Pipeline developed with AI-assisted transformations and human validation
```

## 9. Dashboard / Report Header - Style 1
```
Customer Insights Dashboard
Classification: AICCF: AIG-R (AI-Generated Reviewed)
```

## 10. Email / Business Communication
```Subject: Weekly KPI Summary

Classification: AICCF: AIA-HL

Hi Team,
Please find the weekly KPI summary below...
```

## 11. Sensitive / High-Control Content
Markdown
```
Classification: AICCF: FH
This document has been fully created without AI assistance due to compliance requirements.
```

---

# Specification
-------------

The official AICCF v1.0 specification is available in:

[/spec/spec-aiccf-v1.json](/spec/spec-aiccf-v1.json)


AICCF follows a versioned approach to ensure consistency and traceability.  
Older versions remain available and unchanged.

---

## Version(s)

**Current Version:** 
- AICCF v1.0

**Previous Versions:**
*   None

# Attribution

This framework is based on an original concept developed by the author and refined through an AI-assisted, human-led and reviewed process.
Attribution is appreciated when this framework is shared, published, or adapted externally.

For internal or operational use (e.g., tagging, reporting, or day-to-day workflows), explicit attribution is not required.
Suggested attribution format (when applicable):

_This project uses AICCF (AI Content Classification Framework) for content_ classification. Reference: https://github.com/haroonashraf/AICCF

---

# License
This project is licensed under the Creative Commons Attribution 4.0 International (CC BY 4.0).
You are free to use, adapt, and share this framework with appropriate attribution.

---

# Final Note

This classification aims to provide a practical and accessible approach to improving transparency, accountability, and trust in AI-assisted work.
