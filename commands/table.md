---
description: Generate LaTeX table from description or CSV data
argument-hint: [csv-file-or-description]
allowed-tools: Read, Write, AskUserQuestion
---

Generate a properly formatted LaTeX table based on user input.

## Input Modes

1. **CSV file**: If argument is a file path ending in `.csv`, read and convert it
2. **Description**: Otherwise, interpret as table content description

## Workflow

### Step 1: Gather Table Content

If CSV file provided:
- Read the CSV file
- Parse headers and data rows
- Infer column alignment (numbers right-aligned, text left-aligned)

If description provided:
- Parse the description to understand table structure
- Ask clarifying questions if content is ambiguous

### Step 2: Choose Table Style

Use AskUserQuestion to let user select table format:

**Options:**
1. **booktabs (三线表)** - Clean academic style with `\toprule`, `\midrule`, `\bottomrule`. Recommended for most papers.
2. **Standard** - Basic `\hline` borders, simple and widely compatible
3. **Full grid** - Complete cell borders using `|` column separators
4. **Spanning (跨栏表)** - Multi-column layout using `table*` environment for two-column documents

### Step 3: Configure Options

Ask about additional options:
- Caption text
- Label for cross-referencing
- Column widths (auto or fixed)
- Whether table should float or be placed inline

### Step 4: Generate LaTeX Code

Produce complete table code including:
- Required packages in comments (booktabs, multirow, etc.)
- `\begin{table}` or `\begin{table*}` environment
- Proper column specification
- Caption and label
- The table content with correct formatting

## Output Format

```latex
% Required packages: \usepackage{booktabs}
\begin{table}[htbp]
  \centering
  \caption{Your caption here}
  \label{tab:your-label}
  \begin{tabular}{lcc}
    \toprule
    Header 1 & Header 2 & Header 3 \\
    \midrule
    Data 1 & Data 2 & Data 3 \\
    \bottomrule
  \end{tabular}
\end{table}
```

## Special Cases

- **Long tables**: Suggest `longtable` package for multi-page tables
- **Wide tables**: Suggest `\resizebox` or `tabularx` for width control
- **Complex headers**: Use `\multicolumn` and `\multirow` as needed
