# Writing Style Templates

Predefined style presets for academic writing consistency.

## Style: Formal (正式学术风格)

### Characteristics
- Objective, impersonal tone
- Passive voice preferred
- Third-person perspective
- Hedging language for claims
- Complex sentence structures

### Patterns

**Reporting findings:**
- "It was observed that..."
- "The results indicate that..."
- "Analysis revealed that..."
- "Evidence suggests that..."

**Making claims:**
- "This finding suggests..."
- "These results may indicate..."
- "It appears that..."
- "The data support the hypothesis that..."

**Describing methods:**
- "The experiment was conducted..."
- "Data were collected using..."
- "Analysis was performed by..."
- "Participants were recruited from..."

**Transitions:**
- "Furthermore, ..."
- "Moreover, ..."
- "In addition, ..."
- "Consequently, ..."
- "Nevertheless, ..."

### Example Paragraph

> The proposed method was evaluated on three benchmark datasets. It was observed that the approach achieved superior performance compared to baseline methods across all metrics. These results suggest that the incorporation of attention mechanisms may enhance model capability in capturing long-range dependencies. However, it should be noted that computational costs increased correspondingly, which may limit applicability in resource-constrained environments.

---

## Style: Concise (简洁风格)

### Characteristics
- Direct, active voice
- Short, clear sentences
- Minimal hedging
- One idea per sentence
- Strong topic sentences

### Patterns

**Reporting findings:**
- "We found that..."
- "Results show..."
- "The model achieves..."
- "Performance improves by..."

**Making claims:**
- "[X] outperforms [Y]."
- "This approach works because..."
- "The key insight is..."
- "Our contribution is..."

**Describing methods:**
- "We use..."
- "The system processes..."
- "Training involves..."
- "We evaluate on..."

**Transitions:**
- "First, ..."
- "Next, ..."
- "Also, ..."
- "However, ..."
- "Thus, ..."

### Example Paragraph

> We evaluate our method on three benchmarks. Our approach outperforms all baselines. Accuracy improves by 12% on Dataset A. The attention mechanism captures long-range dependencies effectively. Training takes 4 hours on a single GPU. Memory usage remains constant regardless of sequence length.

---

## Style: Descriptive (描述性风格)

### Characteristics
- Detailed explanations
- Step-by-step descriptions
- Rich context and background
- Thorough justification
- Extended implications discussion

### Patterns

**Reporting findings:**
- "Upon examination of the experimental results, it becomes apparent that..."
- "A detailed analysis of the output reveals several interesting patterns, including..."
- "When comparing the performance metrics across different experimental conditions, we observe that..."

**Making claims:**
- "Based on the comprehensive evaluation conducted across multiple datasets and experimental settings, we argue that..."
- "The evidence accumulated through our series of experiments provides strong support for the claim that..."
- "Considering both the quantitative results and qualitative analysis, it can be concluded that..."

**Describing methods:**
- "The methodology employed in this study consists of several interconnected stages, each of which plays a crucial role in..."
- "To accomplish the task of X, the system first performs Y, which involves..."
- "The experimental setup was designed to ensure that all relevant variables were controlled, specifically..."

### Example Paragraph

> The experimental evaluation of our proposed method was conducted across three widely-used benchmark datasets, each representing different aspects of the target task. In the first set of experiments, we compared our approach against five state-of-the-art baseline methods, carefully selecting implementations that have demonstrated strong performance in prior literature. The results of this comparison reveal that our method achieves consistently superior performance across all evaluation metrics, with particularly notable improvements in scenarios involving long input sequences. This improvement can be attributed to the novel attention mechanism introduced in Section 3, which enables the model to effectively capture dependencies between distant elements in the input. It is worth noting, however, that this enhanced capability comes at the cost of increased computational requirements, a trade-off that practitioners should consider when deploying the method in production environments.

---

## Style Selection Guide

| Style | Best For | Avoid When |
|-------|----------|------------|
| Formal | Traditional journals, conservative venues | Page limits tight, reader expects brevity |
| Concise | Conference papers, page-limited venues | Complex ideas need elaboration |
| Descriptive | Methodology papers, tutorials, theses | Strict page limits, results-focused papers |

## Mixing Styles

Different sections may benefit from different styles:

| Section | Recommended Style |
|---------|-------------------|
| Abstract | Concise |
| Introduction | Formal or Descriptive |
| Related Work | Formal |
| Methodology | Descriptive |
| Results | Concise |
| Discussion | Formal or Descriptive |
| Conclusion | Concise |
