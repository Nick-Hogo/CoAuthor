# Common Academic Writing Errors

Patterns of errors frequently encountered in academic papers with corrections.

## Grammar and Style Errors

### 1. Dangling Modifiers

**Error:**
> Using deep learning, the accuracy improved significantly.

**Problem:** The modifier "Using deep learning" has no clear subject.

**Correction:**
> Using deep learning, we improved accuracy significantly.
> By applying deep learning, the model achieved higher accuracy.

---

### 2. Ambiguous Pronouns

**Error:**
> The model processes the input and generates output. This shows improvement.

**Problem:** "This" is ambiguous - does it refer to the process or the output?

**Correction:**
> The model processes the input and generates output. This generation process shows improvement.
> The model processes the input and generates output. The resulting output shows improvement.

---

### 3. Run-on Sentences

**Error:**
> The model was trained on a large dataset and it achieved state-of-the-art results on multiple benchmarks and the training process took approximately 12 hours on a single GPU.

**Correction:**
> The model was trained on a large dataset. It achieved state-of-the-art results on multiple benchmarks. The training process took approximately 12 hours on a single GPU.

---

### 4. Subject-Verb Agreement

**Error:**
> The set of parameters are optimized during training.

**Correction:**
> The set of parameters is optimized during training.
> The parameters are optimized during training.

---

### 5. Tense Inconsistency

**Error:**
> We train the model on Dataset A. The results showed improvement.

**Correction:**
> We trained the model on Dataset A. The results showed improvement.
> We train the model on Dataset A. The results show improvement.

**Guideline:**
- Past tense: Completed actions, your experiments
- Present tense: General truths, established facts, describing figures

---

## Technical Writing Errors

### 6. Overclaiming

**Error:**
> Our novel method achieves the best results ever reported.

**Problem:** "Novel," "best ever" are unsupported superlatives.

**Correction:**
> Our method achieves competitive results, outperforming recent baselines on Dataset X.
> To our knowledge, our method achieves the highest reported accuracy on this benchmark.

---

### 7. Vague Quantification

**Error:**
> The model significantly outperforms baselines.

**Correction:**
> The model outperforms baselines by 5.2% in accuracy.
> The model achieves statistically significant improvement (p < 0.01).

---

### 8. Undefined Acronyms

**Error:**
> We use NLP techniques with a CNN architecture.

**Correction:**
> We use Natural Language Processing (NLP) techniques with a Convolutional Neural Network (CNN) architecture.

**Rule:** Define on first use, then use acronym consistently.

---

### 9. Missing Antecedent for "respectively"

**Error:**
> The accuracy and F1 score improved by 5% and 3%.

**Correction:**
> The accuracy and F1 score improved by 5% and 3%, respectively.

---

### 10. Incorrect Use of "which" vs "that"

**Error:**
> The method which we propose achieves high accuracy.

**Correction:**
> The method that we propose achieves high accuracy. (defining/restrictive)
> Our method, which uses attention, achieves high accuracy. (non-defining/descriptive)

**Rule:**
- "That" for essential information (no comma)
- "Which" for additional information (with comma)

---

## LaTeX-Specific Errors

### 11. Missing Non-breaking Spaces

**Error:**
```latex
as shown in Figure 1...
Smith et al. [5] proposed...
```

**Correction:**
```latex
as shown in Figure~\ref{fig:results}...
Smith et al.~\cite{smith2020} proposed...
```

**Rule:** Use `~` before `\ref`, `\cite`, units, and abbreviations.

---

### 12. Inconsistent Label Naming

**Error:**
```latex
\label{intro}
\label{fig1}
\label{table_results}
```

**Correction:**
```latex
\label{sec:intro}
\label{fig:architecture}
\label{tab:results}
```

**Convention:** `type:descriptive-name`

---

### 13. Orphan References

**Error:**
```latex
Figure 1 shows...  % But no \label in figure
See Section 3...   % Hardcoded number
```

**Correction:**
```latex
Figure~\ref{fig:architecture} shows...
See Section~\ref{sec:methodology}...
```

---

### 14. Equation Without Context

**Error:**
```latex
The loss function:
\begin{equation}
\mathcal{L} = -\sum_i y_i \log \hat{y}_i
\end{equation}
We minimize this loss.
```

**Correction:**
```latex
The cross-entropy loss function is defined as:
\begin{equation}
\mathcal{L} = -\sum_{i=1}^{N} y_i \log \hat{y}_i
\label{eq:loss}
\end{equation}
where $y_i$ is the ground truth label and $\hat{y}_i$ is the predicted probability for sample $i$. We minimize Equation~\eqref{eq:loss} using gradient descent.
```

---

## Structural Errors

### 15. Missing Contribution Statement

**Error:** Introduction ends without clear contributions.

**Correction:** Add explicit contribution list:
> The main contributions of this paper are:
> 1. We propose X, which addresses Y.
> 2. We introduce Z, enabling W.
> 3. We demonstrate through experiments that...

---

### 16. Results Without Interpretation

**Error:** Results section lists numbers without explanation.

**Correction:** Interpret each result:
> Our method achieves 92.3% accuracy, outperforming the best baseline by 4.1 percentage points. This improvement is particularly notable on long sequences, where the attention mechanism effectively captures distant dependencies.

---

### 17. Missing Limitations

**Error:** Paper claims success without acknowledging limitations.

**Correction:** Add limitations section:
> **Limitations.** Our approach has several limitations. First, computational cost scales quadratically with sequence length. Second, the method requires substantial training data. Third, performance degrades on out-of-domain inputs.

---

## Quick Reference: Error Categories

| Category | Common Errors |
|----------|---------------|
| Grammar | Dangling modifiers, agreement, tense |
| Clarity | Ambiguous pronouns, run-ons, vague terms |
| Technical | Overclaiming, undefined terms, missing stats |
| LaTeX | Missing `~`, inconsistent labels, orphan refs |
| Structure | Missing contributions, no interpretation, no limitations |
