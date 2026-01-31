---
description: Assess rejection risk and identify paper weaknesses
argument-hint: [main-tex-file]
allowed-tools: Read, Grep, Glob
---

Perform comprehensive rejection risk assessment for an academic paper.

## Purpose

Identify potential weaknesses that commonly lead to paper rejection, providing actionable feedback before submission.

## Workflow

### Step 1: Load Paper Content

Read the main .tex file and all included sections via `\input{}` or `\include{}` commands.

### Step 2: Structural Analysis

Check for standard academic paper components:

| Section | Status | Notes |
|---------|--------|-------|
| Title | ✓/✗ | Is it specific and informative? |
| Abstract | ✓/✗ | Present? Within typical length (150-300 words)? |
| Keywords | ✓/✗ | Present if required by venue? |
| Introduction | ✓/✗ | States problem, motivation, contributions? |
| Related Work | ✓/✗ | Adequate literature coverage? |
| Methodology | ✓/✗ | Reproducible? Clearly explained? |
| Results | ✓/✗ | Data presented clearly? |
| Discussion | ✓/✗ | Interprets results? Addresses limitations? |
| Conclusion | ✓/✗ | Summarizes contributions? Future work? |
| References | ✓/✗ | Sufficient quantity? Recent works included? |

### Step 3: Content Quality Checks

**Writing Issues:**
- Overclaiming language ("novel", "first", "best" without evidence)
- Vague statements lacking specifics
- Unsupported assertions
- Grammatical patterns suggesting non-native writing
- Inconsistent terminology

**Technical Issues:**
- Missing experimental details
- Inadequate baselines or comparisons
- Statistical significance not reported
- Figures/tables without proper captions or references
- Equations without numbering or explanation

**Formatting Issues:**
- Orphan `\ref{}` or `\cite{}` commands (undefined references)
- Figures not referenced in text
- Tables not referenced in text
- Inconsistent formatting (fonts, spacing)
- Page limit concerns (estimate page count)

### Step 4: Risk Assessment

Generate overall risk score:

```
REJECTION RISK ASSESSMENT
=========================

Overall Risk: [LOW / MEDIUM / HIGH / CRITICAL]

CRITICAL ISSUES (Must Fix):
---------------------------
1. [Issue description]
   Location: [file:line or section]
   Impact: [Why this causes rejection]
   Fix: [Specific recommendation]

MAJOR CONCERNS (Should Fix):
----------------------------
1. [Issue description]
   ...

MINOR ISSUES (Nice to Fix):
---------------------------
1. [Issue description]
   ...

STRENGTHS:
----------
- [Positive aspect 1]
- [Positive aspect 2]

SUBMISSION READINESS: [NOT READY / NEEDS WORK / NEARLY READY / READY]
```

### Step 5: Comparative Analysis

If paper mentions target venue:
- Check if structure matches venue expectations
- Verify citation of relevant venue publications
- Note any venue-specific requirements

## Output

Provide the complete assessment with:
1. Risk score and justification
2. Prioritized list of issues
3. Specific, actionable recommendations
4. Estimated effort to address each issue
