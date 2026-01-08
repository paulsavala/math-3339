# Textbook Chapter Template

## Template Guidelines

### Overall Structure

All textbook chapters should follow this structure:

1. **Front Matter** (YAML header with title, format settings)
2. **Module Resources** (links to homework, quiz)
3. **Introduction** (engaging overview of the chapter)
4. **Main Content Sections** (8-10 major sections covering core topics)
5. **Summary** (recap of key points)
6. **Practice Exercises** (4-6 exercises)
7. **Additional Resources** (links to external resources)

### Writing Style

**Follow the professor's casual, probing style:**

- Write conversationally, as if talking to students
- Use probing questions rather than direct answers
- Example: "But wait—why does that work? Let's think about it..."
- Avoid overly formal academic language
- Include phrases like "Let's jump in", "Here's the thing", "Don't worry about X right now"
- End sections with thought-provoking questions or connections

**Code demonstrations:**

- Include code every 2-3 paragraphs maximum
- Don't just show code—explain what it's doing and why
- Build up complexity gradually
- Use realistic datasets and examples
- Comment code to explain reasoning, not just what the code does

**Conceptual explanations:**

- Start with intuition, then formalize
- Use analogies and real-world examples
- Connect to what students already know
- Explain the "why" before the "how"
- Make abstract concepts concrete through visualization

### Section Organization

**Major sections (numbered with ##):**

- 8-10 major sections per chapter
- Each covers one core topic from the module
- Should flow logically, building on previous sections

**Subsections (numbered with ###):**

- 2-4 subsections per major section
- Break down the major topic into digestible pieces
- Include at least one code example per subsection

### Code Examples

**Requirements:**

- Every subsection should have at least one code example
- Maximum 2-3 paragraphs before showing code
- Code blocks should be executable (use proper imports)
- Include output or visualization when relevant
- Build complexity gradually across the chapter

**Format:**

```python
# Example structure
import pandas as pd
import seaborn as sns

# Load data
df = pd.read_csv('example.csv')

# Do something meaningful
result = df.groupby('category')['value'].mean()
print(result)
```

**Explanation pattern:**

1. Brief intro to what you're going to do
2. Show the code
3. Explain what happened and why it matters
4. Connect to the bigger picture

### Images and Visualizations

**Requirements:**

- Include 2-3 images/diagrams per chapter
- Create an `images/` subfolder in each module's textbook folder
- Use descriptive filenames (e.g., `bias-variance-tradeoff.png`)
- Reference images with relative paths: `![Description](images/filename.png)`
- Create a `placeholder-info.md` file describing needed images

**Types of images:**

- Workflow diagrams
- Conceptual illustrations
- Example visualizations (good vs. bad)
- Screenshots of tools/interfaces
- Mathematical concepts visualized

### Module Resources Section

**At the top of each chapter, include:**

```markdown
## Module Resources

**Related Assignments:**

- [Module X Homework](../../Assignments/Module%20X%20-%20Topic/module-x-homework.qmd)
- [Module X Quiz](../../Assignments/Module%20X%20-%20Topic/module-x-quiz.qmd)
```

**Note:** Use proper URL encoding for spaces in paths (%20)

### Introduction Section

**Purpose:**

- Hook the reader with why this topic matters
- Preview what they'll learn
- Connect to previous modules (if applicable)
- Set expectations and tone

**Length:** 3-5 paragraphs

**Style:**

- Start with a compelling question or scenario
- Use conversational tone
- Avoid listing learning objectives formally
- Build excitement about the topic

### Summary Section

**Purpose:**

- Recap the main concepts covered
- Emphasize key takeaways
- Connect back to the big picture
- Prepare students for what's next

**Length:** 3-4 paragraphs

**Style:**

- Don't just list topics covered
- Synthesize the main ideas
- Reinforce why these concepts matter
- End with: "Use your brain. That's what it's there for."

### Practice Exercises Section

**Requirements:**

- 4-6 exercises per chapter
- Range from simple to complex
- Mix conceptual and coding exercises
- Should be doable without AI assistance
- Align with "Topics Done By-Hand" from module overview

**Format:**

```markdown
## Practice Exercises

1. **[Exercise name]:** [Description of what to do]

2. **[Exercise name]:** [Description of what to do]

[etc.]
```

### Additional Resources Section

**Include:**

- Official documentation links (Pandas, Scikit-learn, etc.)
- Relevant tutorials or guides
- Tool-specific resources (Gemini CLI, etc.)
- Visualization galleries
- Articles or videos for deeper learning

**Format:**

```markdown
## Additional Resources

- [Resource name](URL) - Brief description
- [Resource name](URL) - Brief description
[etc.]
```

### Placeholder Content

When creating a template or draft chapter:

- Use `XXX` for content placeholders
- Include brief descriptions of what should go there
- Leave code blocks with comments showing what example to include
- Mark image locations with descriptive placeholder filenames

---

## Chapter Template Structure

```markdown
---
title: "Chapter [X]: [Topic Name]"
format:
  html:
    toc: true
    toc-depth: 3
    code-fold: false
    theme: cosmo
jupyter: python3
---

## Module Resources

**Related Assignments:**

- [Module X Homework](../../Assignments/Module%20X%20-%20Topic/module-x-homework.qmd)
- [Module X Quiz](../../Assignments/Module%20X%20-%20Topic/module-x-quiz.qmd)

---

## Introduction

XXX - Engaging introduction (3-5 paragraphs)
- Why this topic matters
- What they'll learn
- Connection to data science workflow

---

## 1. [First Major Topic]

### 1.1 [First Subtopic]

XXX - Conceptual explanation (2-3 paragraphs)

```python
# XXX - Code example demonstrating the concept
# code here
```

XXX - Explanation of what the code does and why it matters

### 1.2 [Second Subtopic]

XXX - Continue pattern...

### 1.3 [Third Subtopic]

XXX - Continue pattern...

![Placeholder for diagram](images/diagram-name-placeholder.png)

---

## 2. [Second Major Topic]

### 2.1 [Subtopic]

XXX - Content...

```python
# XXX - Code example
```

### 2.2 [Subtopic]

XXX - Content...

---

[Continue for 8-10 major sections...]

---

## Summary

XXX - Synthesis of main concepts (3-4 paragraphs)
- Key takeaways
- Why these concepts matter
- Connection to future work
- End with: "Use your brain. That's what it's there for."

---

## Practice Exercises

1. **[Exercise name]:** XXX - Description
2. **[Exercise name]:** XXX - Description
3. **[Exercise name]:** XXX - Description
4. **[Exercise name]:** XXX - Description

---

## Additional Resources

- [Resource name](URL) - Description
- [Resource name](URL) - Description
- [Resource name](URL) - Description
```

---

## Directory Structure

For each module's textbook chapter:

```
Textbook/
  Module-X-Topic/
    chapter-x-topic.qmd          # Main chapter file
    images/                       # Images folder
      placeholder-info.md         # Description of needed images
      diagram1.png               # Actual images (to be created)
      diagram2.png
```

---

## Module-Specific Adaptations

### Module 1 (EDA and AI-Assisted Coding):
- Emphasize AI prompting throughout
- Include examples of good vs. bad prompts
- Show when to use AI vs. hand-coding
- Focus on Pandas, Seaborn, testing

### Module 2 (Intro to ML Models):
- Focus on model instantiation, fitting, predicting
- Show different model types in action
- Emphasize evaluation metrics
- Compare models systematically

### Module 3 (ML Theory):
- Heavy use of visualization to explain concepts
- Loss functions shown with code and plots
- Bias-variance visualized extensively
- Theoretical concepts made concrete

### Module 4 (Regression):
- Extensive diagnostic plots
- Residual analysis examples
- Coefficient interpretation in context
- Regularization effects visualized

### Module 5 (Classification):
- Confusion matrices and ROC curves
- Metric interpretation in business context
- Class imbalance examples
- Decision boundaries visualized

### Module 6 (Neural Networks):
- PyTorch code structure emphasized
- Training curves and interpretation
- Architecture diagrams
- Connection to earlier concepts

### Module 7 (Pretrained Models):
- Hugging Face examples
- Model card interpretation
- Transfer learning workflow
- Fine-tuning examples

---

## Quality Checklist

Before finalizing a chapter, verify:

- [ ] Module Resources section links to correct homework/quiz
- [ ] Introduction is engaging and sets proper expectations
- [ ] 8-10 major sections covering all core topics
- [ ] Code examples every 2-3 paragraphs
- [ ] All code is executable and properly formatted
- [ ] 2-3 images included with placeholder info
- [ ] Writing style matches professor's casual tone
- [ ] Concepts explained with intuition before formalization
- [ ] Summary synthesizes key ideas
- [ ] 4-6 practice exercises included
- [ ] Additional Resources section populated
- [ ] Ends with "Use your brain. That's what it's there for."
