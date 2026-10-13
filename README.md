* * *
# AICCF (AI Content Classification Framework)


AI Content Classification Framework for AI involvement and human accountability

**Current Version:** AICCF v1.1

AICCF is a structured, content-agnostic framework designed to classify work based on the level of AI involvement and human accountability.
It provides a simple and consistent way to describe how content is created, reviewed, and owned across different domains, including writing, code, analysis, and project deliverables.

* * *

Overview
========

As AI becomes increasingly integrated into everyday work, distinguishing between AI-generated and human-created content is no longer sufficient.
AICCF introduces a practical model that focuses on:
*   **Level of AI involvement**
*   **Degree of human oversight**
*   **Clear accountability and ownership**

* * *

Framework Levels
================

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

**Level 5 – Fully Human (No AI Involvement)**  
Content created entirely without AI assistance.  
_Used where strict control, compliance, or complete human authorship is required._

* * *

Principles
==========

*   Human accountability is always required
*   AI is assistive, not authoritative
*   Validation is required before reliance
*   AI involvement should be transparent where appropriate
*   Required level of oversight may vary based on risk and use case

* * *

Tags
====

To simplify adoption, the following tags can be used.

Primary Tags
------------

*   `AIG-U` → AI-Generated Unreviewed 
*   `AIG-R` → AI-Generated Reviewed (Alias: `AIA-R` → AI-Assisted Reviewed) 
*   `AIA-HL` → AI-Assisted Human-Led
*   `H-AIE` → Human-Created AI-Enhanced
*   `FH` → Fully Human (No AI Involvement)


## Quick Use (After attribution where applicable)
    
```text
This project uses AICCF v1.1.    

Reference:
https://github.com/haroonashraf/AICCF

----------

Classification: AICCF: AIG-U (AI-Generated Unreviewed)
    
Classification: AICCF: AIG-R (AI-Generated Reviewed)
OR
Classification: AICCF: AIA-R (AI-Assisted Reviewed)
    
Classification: AICCF: AIA-HL (AI-Assisted Human-Led)
    
Classification: AICCF: H-AIE (Human-Created AI-Enhanced)
    
Classification: AICCF: FH (Fully Human - No AI Involvement)
```
Compatibility Alias
-------------------

*   `AIA-R` → AI-Assisted Reviewed
`AIA-R` is an officially supported alias of `AIG-R` and represents the same classification level.
**The following classifications are equivalent:**

    Classification: AICCF: AIG-R

    Classification: AICCF: AIA-R
    

Both may be used interchangeably.

* * *

AIA-R Review Workflow Clarification
===================================

In some scenarios, AI generates content directly from author-defined requirements and follows the applicable structure, template, coding standards, or documentation standards.

To improve workflow efficiency, such content may be created directly with an AIA-R (AI-Assisted Reviewed) classification while clearly indicating that author review is still required.

Pending Review Example
----------------------

    Author: <AuthorName>
    Date: 07-October-2026
    Classification: AICCF: AIA-R (AI-Assisted Reviewed)
    *Pending Author Review (Please remove this line after review)

After Review
------------

    Author: <AuthorName>
    Date: 07-October-2026
    Classification: AICCF: AIA-R (AI-Assisted Reviewed)

Notes
-----

* Generated from author-defined requirements.
* The author remains accountable for review and approval.
* The "Pending Author Review" notice provides visibility that review has not yet been completed.
* The notice should be removed once review is complete.
* Testing, repository storage, validation, approval, and publication activities should occur after appropriate review.

* * *



* * *

Example Use Cases
=================

* Draft content / brainstorming → AIG-U
* Reports / documentation → AIG-R, AIA-R or AIA-HL
* Requirement-driven AI generated content awaiting review → AIA-R with "Pending Author Review" notice
* Code / technical implementation → AIA-HL or H-AIE
* Sensitive or regulated content → FH or H-AIE


* * *

Example Disclaimers
===================

*   "This content was generated with AI assistance and reviewed by a human."
*   "AI-generated output – requires validation before use."
*   "Human-led work supported by AI tools."
*   "This content was created entirely without AI assistance."

* * *

Applicability
=============

This framework is content-agnostic and can be applied across:
*   Articles and reports
*   Code and technical solutions
*   Data analysis and insights
*   Documentation and communication
*   End-to-end project deliverables

* * *

AICCF Usage Syntax
==================

AICCF supports two standard usage styles for content classification.

Style 1 – Tag Only (Default)
----------------------------

**Syntax:**

    Classification: AICCF: <TAG>
    

Style 2 – Tag with Details
--------------------------

**Syntax:**

    Classification: AICCF: <TAG> (<DETAIL>)
    

* * *

Integration Guide (How to Use AICCF Tags)
=========================================
## 1. Add a Global Reference (Recommended)


In shared or long-lived contexts such as:
*   repositories
*   documentation
*   codebases
It is recommended to include a reference to AICCF once at the beginning to ensure clarity and traceability.

**Recommended format:**

    This project uses AICCF v1.1.
    
    Reference:
    https://github.com/haroonashraf/AICCF
    

**Alternative (more descriptive):**

    This project uses AICCF v1.1 (AI Content Classification Framework) for content classification.
    
    Reference:
    https://github.com/haroonashraf/AICCF
    

After this reference is defined, AICCF tags can be used independently throughout the content.

    AICCF: AIA-HL
    
* * *
## 2. Markdown / Documentation (Clean & Professional)

**Style 1 - Tag Only**

    # Earth-Like Planets Report
    
    Classification: AICCF: AIA-HL
    
    This report analyses nearby Earth-like planets...
    

**Style 2 - Tag with Level Name**

    # Sales Performance Report
    
    Classification: AICCF: AIA-HL (AI-Assisted Human-Led)
    
    This report analyses sales performance...
    

* * *

## 3. Technical Documentation (More Structured)

**Style 1**

    ## Metadata
    
    - Classification: AICCF: AIA-R
    - Author: Data Engineering Team
    - Last Updated: 2026-01-09
    

**Style 2**

    ## Metadata
    
    - Classification: AICCF: AIA-R (AI-Assisted Reviewed)
    - Author: Data Engineering Team
    - Last Updated: 2026-01-09
    

* * *

## 4. Python Code Example

    # Classification: AICCF: AIA-HL (AI-Assisted Human-Led)
    # Python code designed by a developer assisted by AI
    
    import math
    
    def AddBy1(x):
        return (x + 1)
    
    a = 1
    a = AddBy1(a)
    
    print(a)
    

* * *
## 5. SQL Code


    -- Classification: AICCF: H-AIE (Human-Created AI-Enhanced)
    -- SQL script written by an analyst optimized with AI
    
    SELECT TOP 3 Stars
    FROM Sky;
    


* * *

## 5A. AI Generated Content Awaiting Review

    Author: SQL BI Developer
    Date: 07-October-2026
    Classification: AICCF: AIA-R (AI-Assisted Reviewed)
    *Pending Author Review (Please remove this line after review)

    Purpose:
    Initial implementation generated from author-defined requirements.
    Review is required before testing, repository storage, or publication.

After Review

    Author: SQL BI Developer
    Date: 07-October-2026
    Classification: AICCF: AIA-R (AI-Assisted Reviewed)

    Purpose:
    Reviewed and approved by the author prior to testing and publication activities.


* * *

## 6. GitHub Pull Request

    ## Classification: AICCF: AIG-R (AI-Generated Reviewed)
    
    ## Notes
    
    Initial implementation generated using AI and reviewed before submission.
    

* * *

## 7. Commit Message


    Classification: AICCF: AIA-HL
    
    Refactored transformation logic with AI-assisted suggestions
    

* * *

## 8. Data Pipeline / ETL

    pipeline: customer_ingestion
    
    metadata:
      classification: AICCF: AIA-HL (AI-Assisted Human-Led)
      description: Pipeline developed with AI-assisted transformations and human validation
    

* * *

## 9. Dashboard / Report Header

    Customer Insights Dashboard
    
    Classification: AICCF: AIG-R (AI-Generated Reviewed)
    

* * *

## 10. Email / Business Communication

    Subject: Weekly KPI Summary
    
    Classification: AICCF: AIA-HL
    
    Hi Team,
    
    Please find the weekly KPI summary below...
    

* * *

## 11. Sensitive / High-Control Content

    Classification: AICCF: FH (Fully Human - No AI Involvement)
    
    This document has been fully created without AI assistance due to compliance requirements.
    

* * *

## 12. Notes /Wiki Pages / OneNote Documentation 
AICCF can be used alongside document tracking mechanisms such as Last Update logs in Notes, OneNote, Wikis, SharePoint pages, and internal documentation repositories. 

### Style 1 - Notes / OneNote (Plain Text) 

```text
Page Information 

This project uses AICCF v1.1. 

Reference: 
https://github.com/haroonashraf/AICCF 

Classification: AICCF: AIA-R (AI-Assisted Reviewed) 

Purpose: Personal and educational purposes only. 

Last Update: 
04 August 2026 3:15 PM - Version 1.0 ready (<Author Name>) 
- Note complete and reviewed 
- Checklist version added
```
### Style 2 - Markdown Documentation (Wiki Pages)

```
# Page Information 

This project uses AICCF v1.1. 

Reference: 
https://github.com/haroonashraf/AICCF 

**Classification: AICCF: AIA-R (AI-Assisted Reviewed)** 

Purpose: Personal and educational purposes only. 

## Last Update: 
**04 August 2026 3:15 PM - Version 1.0 ready (<Author Name>)** 
- Note complete and reviewed 
- Checklist version added
```

* * *

### Style 3 - Markdown Documentation with Page Information 
This style demonstrates a structured Markdown document using page metadata and update tracking. The AICCF README itself follows this style.

```
Page Information 
================ 

This project uses AICCF v1.1. 

Reference: https://github.com/haroonashraf/AICCF 

**Classification: AICCF: AIA-HL (AI-Assisted Human-Led)** 

Purpose: Public framework documentation and educational purposes. 

Last Update 
=========== 
**04 August 2026 5:00 PM - Version 1.1 updated. (<Author Name>)** 
- Added Notes, Wiki Pages, and OneNote implementation examples demonstrating AICCF usage alongside Last Update document tracking.
```

Specification
=============

The official AICCF v1.1 specification is available in:

[/spec/aiccf-v1-1-spec.json](/spec/aiccf-v1-1-spec.json)
    

AICCF follows a versioned approach to ensure consistency and traceability.
Older versions remain available and unchanged.

* * *

Version(s)
==========

**Current Version:**
*   AICCF v1.1

**Previous Versions:**
*   [/versions/aiccf-v1-0.md](/versions/aiccf-v1-0.md)

* * *

Compatibility Notes
===================

AICCF v1.1 maintains backward compatibility with AICCF v1.0.
Changes introduced in v1.1:
* Added official alias `AIA-R` (AI-Assisted Reviewed) equivalent to `AIG-R` 
* Clarified `FH` as `Fully Human (No AI Involvement)` 
* Updated examples and attribution guidance to reference framework versions 
* Added Notes, Wiki Pages, and OneNote implementation examples 
* Added Style 3 Markdown documentation example with Page Information and Last Update tracking
* Added guidance for requirement-driven AI generated content that may be created directly as AIA-R with a temporary "Pending Author Review" notice.
* * *

Attribution
===========

This framework is based on an original concept developed by the author and refined through an AI-assisted, human-led and reviewed process.
Attribution is appreciated when this framework is shared, published, or adapted externally.
For internal or operational use (e.g., tagging, reporting, or day-to-day workflows), explicit attribution is not required.
Suggested attribution format (when applicable):

    This project uses AICCF v1.1 (AI Content Classification Framework) for content classification.
    
    Reference:
    https://github.com/haroonashraf/AICCF
    

* * *

License
=======

This project is licensed under the Creative Commons Attribution 4.0 International (CC BY 4.0).
You are free to use, adapt, and share this framework with appropriate attribution.

* * *

Final Note
==========

This classification aims to provide a practical and accessible approach to improving transparency, accountability, and trust in AI-assisted work.
Classification: AICCF: AIA-HL (AI-Assisted Human-Led)

* * *

Page Information 
================

This project uses AICCF v1.1. 

Reference: 
https://github.com/haroonashraf/AICCF 

**Classification: AICCF: AIA-HL (AI-Assisted Human-Led)** 

Purpose: Public framework documentation and educational purposes. 

Last Update 
===========
**21 July 2026 12:45 PM - Version 1.1 released. (Haroon ASHRAF)** 
- Added AIA-R (AI-Assisted Reviewed) as an official alias of AIG-R. 
- Clarified FH as Fully Human (No AI Involvement). 
- Updated attribution guidance. 
- Introduced versioned specifications. 

**21 July 2026 7:05 PM - Version 1.1 updated. (Haroon ASHRAF)**  
- Fixed documentation links and repository references following v1.1 publication. 

**04 August 2026 5:00 PM - Version 1.1 updated. (Haroon ASHRAF)** 
- Added Notes, Wiki Pages, and OneNote implementation examples demonstrating AICCF usage alongside Last Update document tracking. 

**12 October 2026 2:30 PM - Version 1.1 updated. (Haroon ASHRAF)**
- Added AIA-R review workflow clarification.
- Added examples showing use of a temporary "Pending Author Review" notice.
- Added implementation guidance for AI generated content awaiting author review before testing, repository storage, or publication.
