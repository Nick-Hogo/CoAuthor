---
description: Analyze and reorganize LaTeX project file structure - standardize layout, auto-create missing directories, rename and relocate existing files
argument-hint: [project-path]
allowed-tools: Read, Write, Edit, Bash(mkdir:*, mv:*, cp:*, ls:*, find:*)
---

Organize a LaTeX academic paper project at the specified path (default: current directory).

## Task

1. **Analyze current state**: Check if target directory exists and contains LaTeX files
2. **Determine action**:
   - Empty/new directory → Initialize standard structure
   - Existing project → Reorganize to standard structure

## Standard Structure

```
project/
├── main.tex           # Main document (or rename existing primary .tex)
├── sections/          # Chapter/section files
│   ├── abstract.tex
│   ├── introduction.tex
│   ├── methodology.tex
│   ├── results.tex
│   ├── discussion.tex
│   └── conclusion.tex
├── figures/           # All figure files (.pdf, .png, .eps)
├── tables/            # Standalone table files
└── refs.bib           # Bibliography file
```

## For New Projects

Create the directory structure and generate template files:
- `main.tex` with standard preamble (article class, common packages)
- Section files with placeholder headings
- Empty `refs.bib` with example entry format

## For Existing Projects

1. Identify the main .tex file (contains `\documentclass`)
2. Rename to `main.tex` if needed
3. Move figure files (.pdf, .png, .jpg, .eps) to `figures/`
4. Move or extract tables to `tables/`
5. Move section files to `sections/`
6. Consolidate bibliography entries to `refs.bib`
7. Update all `\input{}`, `\include{}`, `\includegraphics{}`, `\bibliography{}` paths

## Output

Report what was done:
- Files created or moved
- Path updates made
- Any manual fixes needed
