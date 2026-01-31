---
description: Verify citation authenticity and detect potential hallucinations
argument-hint: [bib-file-or-tex-file]
allowed-tools: Read, Grep, mcp__grok-search__web_search, mcp__grok-search__web_fetch
---

Perform rigorous verification of citations to detect hallucinated or incorrect references.

## Purpose

Academic integrity requires accurate citations. This command verifies that:
1. Cited works actually exist
2. Authors, titles, years, and venues are correct
3. DOIs and URLs are valid
4. No fabricated references are present

## Workflow

### Step 1: Extract Citations

If `.bib` file provided:
- Parse all BibTeX entries
- Extract: authors, title, year, journal/conference, DOI, URL

If `.tex` file provided:
- Find `\bibliography{}` or `\addbibresource{}` commands
- Locate and parse the referenced .bib file
- Also check for inline `\bibitem` entries

### Step 2: Verify Each Citation

For each reference, perform multi-source verification:

**Primary Checks:**
1. **DOI Verification**: If DOI present, validate via doi.org
2. **Title Search**: Search exact title in quotes on Google Scholar / Semantic Scholar
3. **Author + Year Search**: Cross-reference author names with publication year

**Verification Criteria:**
- ✅ **Verified**: Found exact match with consistent metadata
- ⚠️ **Needs Review**: Partial match or minor discrepancies (typos, year off by 1)
- ❌ **Suspicious**: Cannot find evidence of existence
- ❓ **Unverifiable**: Preprints, technical reports, or sources not indexed

### Step 3: Check for Common Issues

- **Author name variations**: "J. Smith" vs "John Smith" vs "Smith, J."
- **Title discrepancies**: Subtitle differences, capitalization
- **Venue name changes**: Journal name updates, conference acronyms
- **Year mismatches**: Publication vs acceptance year
- **Predatory journals**: Flag known predatory publishers

### Step 4: Generate Report

```
Citation Verification Report
============================

Total citations: X
✅ Verified: X
⚠️ Needs Review: X
❌ Suspicious: X
❓ Unverifiable: X

SUSPICIOUS CITATIONS (Require Immediate Attention):
---------------------------------------------------
1. [key] Author et al., "Title", Year
   Issue: No matching publication found
   Search attempted: [search queries used]
   Recommendation: Remove or replace with verified source

CITATIONS NEEDING REVIEW:
-------------------------
1. [key] Author et al., "Title", Year
   Issue: Year mismatch (found 2022, cited as 2023)
   Source: [URL to verified publication]
   Recommendation: Update year to 2022

VERIFIED CITATIONS:
-------------------
[List with confirmation sources]
```

## Important Notes

- This is a verification tool, not a citation generator
- Always manually confirm suspicious citations before removal
- Some legitimate sources may be unverifiable (internal reports, personal communications)
- Preprints on arXiv should be verified but flagged for potential update to published version
