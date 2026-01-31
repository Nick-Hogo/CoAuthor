---
name: LaTeX Academic Writing
description: This skill should be used when the user asks to "write a paper section", "draft introduction", "write methodology", "academic writing style", "latex best practices", "scientific writing", "paper structure", "write abstract", "write conclusion", or needs guidance on academic writing conventions, LaTeX formatting, and paper organization for scholarly publications.
version: 0.1.0
---

# LaTeX Academic Writing Guide

Guidance for producing high-quality academic papers in LaTeX, covering structure, style, and common conventions.

## Paper Structure

### Standard IMRaD Structure

For empirical research papers:

| Section | Purpose | Typical Length |
|---------|---------|----------------|
| Abstract | Summarize entire paper | 150-300 words |
| Introduction | Problem, motivation, contributions | 1-2 pages |
| Related Work | Position in literature | 1-2 pages |
| Methodology | How research was conducted | 2-4 pages |
| Results | What was found | 2-4 pages |
| Discussion | Interpretation and implications | 1-2 pages |
| Conclusion | Summary and future work | 0.5-1 page |

### Section Writing Guidelines

**Abstract**: State problem, approach, key results, and significance. Write last after paper is complete.

**Introduction**: Follow the "funnel" structure:
1. Broad context (1-2 paragraphs)
2. Specific problem (1 paragraph)
3. Gap in existing work (1 paragraph)
4. Contributions (numbered list)
5. Paper organization (optional)

**Methodology**: Provide enough detail for reproducibility. Include:
- Data/materials description
- Experimental setup
- Evaluation metrics
- Implementation details

**Results**: Present findings objectively without interpretation. Use figures and tables effectively.

**Discussion**: Interpret results, address limitations, compare with prior work.

**Conclusion**: Summarize contributions (not results), state limitations, suggest future directions.

## LaTeX Best Practices

### Document Structure

```latex
\documentclass[conference]{IEEEtran}  % or article, llncs, etc.

% Essential packages
\usepackage{graphicx}    % figures
\usepackage{booktabs}    % professional tables
\usepackage{amsmath}     % math environments
\usepackage{hyperref}    % clickable references
\usepackage{cleveref}    % smart cross-references

\begin{document}
\input{sections/abstract}
\input{sections/introduction}
% ...
\bibliographystyle{IEEEtran}
\bibliography{refs}
\end{document}
```

### Cross-References

Use `\label` and `\ref` consistently:

```latex
\section{Introduction}
\label{sec:intro}

As shown in Section~\ref{sec:methodology}...
Figure~\ref{fig:results} illustrates...
Table~\ref{tab:comparison} compares...
Equation~\eqref{eq:loss} defines...
```

**Naming conventions:**
- Sections: `sec:name`
- Figures: `fig:name`
- Tables: `tab:name`
- Equations: `eq:name`

### Figures

```latex
\begin{figure}[htbp]
  \centering
  \includegraphics[width=\columnwidth]{figures/results.pdf}
  \caption{Description of what the figure shows. Include axis labels explanation if needed.}
  \label{fig:results}
\end{figure}
```

**Guidelines:**
- Use vector formats (PDF, EPS) when possible
- Ensure readable font sizes in figures
- Caption should be self-contained
- Reference every figure in text

### Tables

Use `booktabs` for professional tables:

```latex
\begin{table}[htbp]
  \centering
  \caption{Comparison of methods on benchmark dataset.}
  \label{tab:comparison}
  \begin{tabular}{lcc}
    \toprule
    Method & Accuracy & F1 Score \\
    \midrule
    Baseline & 85.2 & 0.83 \\
    Proposed & \textbf{91.7} & \textbf{0.90} \\
    \bottomrule
  \end{tabular}
\end{table}
```

### Equations

```latex
\begin{equation}
  \mathcal{L} = -\sum_{i=1}^{N} y_i \log(\hat{y}_i)
  \label{eq:loss}
\end{equation}
```

**Guidelines:**
- Number important equations that are referenced
- Use `align` for multi-line equations
- Define all symbols after equation

### Citations

```latex
Prior work~\cite{smith2020} has shown...
Several studies~\cite{jones2019,brown2021} demonstrate...
Smith et al.~\cite{smith2020} proposed...
```

**Guidelines:**
- Use non-breaking space (`~`) before `\cite`
- Group multiple citations chronologically
- Cite recent work (last 3-5 years)
- Include seminal works in the field

## Writing Style

### Academic Tone

**Preferred patterns:**
- "This paper presents..." (not "I present...")
- "The results indicate..." (not "We found...")
- "It can be observed that..." (neutral)

**Hedging language:**
- "suggests", "indicates", "appears to"
- "may", "might", "could"
- "tends to", "seems to"

**Avoid:**
- First person unless journal allows
- Colloquialisms and contractions
- Subjective adjectives without evidence
- Overclaiming ("novel", "first", "best")

### Clarity and Precision

**Be specific:**
- ❌ "significantly improved"
- ✅ "improved accuracy by 12.3%"

**Define terms:**
- Introduce acronyms: "Natural Language Processing (NLP)"
- Define technical terms on first use

**One idea per sentence:**
- Break complex sentences
- Use parallel structure for lists

### Common Errors to Avoid

1. **Dangling modifiers**: "Using deep learning, the accuracy improved." → "Using deep learning, we improved accuracy."

2. **Ambiguous pronouns**: "This shows..." → "This result shows..."

3. **Run-on sentences**: Break into multiple sentences.

4. **Passive overuse**: Mix active and passive appropriately.

5. **Tense inconsistency**: Use past for completed work, present for general truths.

## Quality Checklist

Before submission:

**Structure:**
- [ ] All sections present and complete
- [ ] Logical flow between sections
- [ ] Balanced section lengths

**References:**
- [ ] No undefined references (`??`)
- [ ] All figures/tables referenced in text
- [ ] All citations present in bibliography

**Formatting:**
- [ ] Consistent formatting throughout
- [ ] Page/word limit respected
- [ ] Figures readable at print size

**Writing:**
- [ ] No spelling/grammar errors
- [ ] Consistent terminology
- [ ] Clear, precise language

## Additional Resources

### Reference Files

For detailed guidance:
- **`references/style-templates.md`** - Writing style presets (formal, concise, descriptive)
- **`references/common-errors.md`** - Detailed error patterns and fixes

### Integration with Commands

This skill supports CoAuthor commands:
- `/coauthor:init` - Uses structure guidelines
- `/coauthor:style` - Applies writing style presets
- `/coauthor:review` - Checks against quality standards
