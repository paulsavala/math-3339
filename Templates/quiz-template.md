# Quiz Template

## Template Guidelines

### Overall Structure

All quizzes should follow this two-section structure:
- **Section A: Conceptual Questions (approximately 50% of points)** - Testing understanding of concepts, trade-offs, and decision-making
- **Section B: Code Writing (approximately 50% of points)** - Testing ability to write code by hand

Total: Typically 25-50 points (adjustable based on chapter complexity)

Time: 30-45 minutes

### Point Distribution Philosophy

**Points should reflect:**
- Complexity of the concept or code required
- Number of parts in the question
- Level of reasoning needed

**Typical ranges:**
- Simple recall/identification: 2 points
- Moderate explanation/interpretation: 3 points
- Complex reasoning/multi-part questions: 3-4 points
- Code writing tasks: 2-4 points depending on complexity

### Section A: Conceptual Questions

**Purpose:**
- Test conceptual understanding without a computer
- Assess ability to reason about trade-offs and make decisions
- Evaluate recognition of when techniques are appropriate/inappropriate
- Check understanding of metrics and their interpretations

**Question Types:**

1. **Scenario identification** (2-3 points)
   - Given scenarios, identify problem type/appropriate technique
   - Example: "Is this classification or regression?"
   - Multiple scenarios in one question

2. **Metric interpretation** (3 points)
   - Given metric values, interpret meaning
   - Compare models based on different metrics
   - Explain which metric to prioritize in a business context

3. **Trade-off reasoning** (3-4 points)
   - Understand precision vs recall, bias vs variance, etc.
   - Explain when to choose one approach over another
   - Justify decisions based on context

4. **Conceptual explanation** (2-3 points)
   - Define terms in own words
   - Explain why something works or fails
   - Describe relationships between concepts

5. **Problem diagnosis** (3-4 points)
   - Given symptoms (overfitting, poor performance, etc.), identify cause
   - Suggest solutions to problems
   - Recognize when assumptions are violated

6. **Matching questions** (2-3 points)
   - Match models to their characteristics
   - Match metrics to their uses
   - Match problems to solutions

7. **Scenario-based reasoning** (3-4 points)
   - Multi-part questions about a specific scenario
   - Requires applying multiple concepts
   - Tests understanding of workflow and decision-making

**Typical distribution:** 6-8 questions totaling 45-55% of quiz points

### Section B: Code Writing

**Purpose:**
- Test ability to write basic code without computer/IDE
- Ensure students know fundamental syntax and workflows
- Assess understanding of what code does, not just copying
- Check recall of essential library functions

**Important Notes:**
- Syntax perfection is NOT required
- Focus on logic and correct approach
- Minor syntax errors minimally penalized
- Students should demonstrate understanding of the workflow

**Question Types:**

1. **Data manipulation** (2-3 points)
   - Load data, select columns, filter rows
   - Create train/test splits
   - Basic Pandas operations

2. **Model instantiation** (2-3 points)
   - Create model objects with correct parameters
   - Example: `LinearRegression()`, `DecisionTreeClassifier(max_depth=5)`

3. **Model workflow** (3-4 points)
   - Complete fit/predict workflow
   - May include model creation, fitting, and prediction in sequence

4. **Metric calculation** (2-3 points)
   - Calculate metrics using sklearn functions
   - Example: `accuracy_score(y_test, predictions)`

5. **Visualization code** (3-4 points)
   - Create basic plots (scatter, histogram, bar)
   - Add labels and titles
   - May be more challenging due to syntax details

6. **Function writing** (4-5 points)
   - Write simple functions that take inputs and return outputs
   - Demonstrate logic and workflow understanding
   - Example: comparison function, evaluation function

**Typical distribution:** 5-7 questions totaling 45-55% of quiz points

### Grading Rubric Guidelines

**Section A (Conceptual):**
- Full credit: Demonstrates clear understanding
- Partial credit: Shows correct reasoning even if incomplete
- Focus on understanding, not perfect wording

**Section B (Code):**
- Correct logic and approach: 70-80% of points
- Syntax and details: 20-30% of points
- Minor syntax errors minimally penalized
- Must show understanding of workflow

**Include statement:** "Minor syntax errors will not be heavily penalized. Focus is on correct logic and understanding of the workflow."

### Standard Sections

**Every quiz should include:**

1. **Title and metadata** (Quarto YAML header)
2. **Instructions** with:
   - Time limit (30-45 minutes)
   - Format: In-class, by-hand (no computer)
   - General instruction about writing neatly
   - Note about partial credit
3. **Section A: Conceptual Questions** (~50% of points, 6-8 questions)
4. **Section B: Code Writing** (~50% of points, 5-7 questions)
5. **Grading Rubric** (breakdown by section with note about syntax)

### Assumptions Section for Code Writing

**Always include for Section B:**

```markdown
For questions X-Y, assume you have already imported:
```python
[relevant imports for the chapter]
```

Also assume you have [description of available data/variables].
```

**Example for ML chapter:**
```markdown
For questions 6-12, assume you have already imported:
```python
import pandas as pd
import numpy as np
from sklearn.model_selection import train_test_split
from sklearn.linear_model import LinearRegression
from sklearn.metrics import mean_squared_error, r2_score
```

Also assume you have a DataFrame called `df` with features and a target column.
```

### Writing Style

**Instructions:**
- Clear and direct
- Specify "by hand" and "no computer" explicitly
- Set expectations about syntax

**Questions:**
- Start with clear action verbs
- Provide sufficient context
- Multi-part questions should use a), b), c)
- Ask "why" and "explain your reasoning" frequently

**Conceptual questions:**
- Present realistic scenarios
- Require application of knowledge, not just recall
- Include business/practical context when relevant

**Code questions:**
- Be specific about what to create
- Specify variable names if relevant
- Break complex tasks into steps

### Formatting Guidelines for Quarto Markdown

**IMPORTANT - List Rendering:**
- Lists preceded by bold text, headings, or other content **MUST** have a blank line before the list starts
- Without the blank line, Quarto will not render the list properly

**Correct formatting:**
```markdown
**Models:** Logistic Regression, Decision Tree, k-Nearest Neighbors

**Advantages:**

1. Easy to interpret and visualize the decision-making process
2. Makes no assumptions about the underlying data distribution
3. Provides probability estimates and handles binary classification well
```

**Incorrect formatting (will not render as list):**
```markdown
**Advantages:**
1. Easy to interpret and visualize the decision-making process
2. Makes no assumptions about the underlying data distribution
```

**Apply this rule to:**
- Multi-part questions (a, b, c)
- Matching question options
- Scenario lists
- Any list following text, bold text, or headings

---

## Quiz Template Structure

```markdown
---
title: "Chapter [X] Quiz: [Topic Name]"
format:
  html:
    toc: true
    code-fold: false
    theme: cosmo
---

## Instructions

**Time:** 30-45 minutes
**Format:** In-class, by-hand (no computer)

Answer all questions. Write code by hand as neatly as possible. Partial credit will be given for correct reasoning even if syntax isn't perfect.

---

## Section A: Conceptual Questions

### Question 1 ([2-4] points)

[Conceptual question with clear scenario/context]

[If multi-part: **a)**, **b)**, **c)**]

---

### Question 2 ([2-4] points)

[Continue pattern for 6-8 questions total]

---

[Questions 3-8...]

---

## Section B: Code Writing

For questions [X]-[Y], assume you have already imported:
```python
[relevant imports]
```

Also assume you have [description of available data/variables].

---

### Question [X] ([2-3] points)

Write code to [specific task].

---

### Question [X+1] ([2-4] points)

[Continue pattern for 5-7 questions total]

---

[Remaining code questions...]

---

## Grading Rubric

**Section A: Conceptual Questions ([total] points)**

- [Category 1]: [points]
- [Category 2]: [points]
- [Category 3]: [points]
- [etc.]

**Section B: Code Writing ([total] points)**

- [Category 1]: [points]
- [Category 2]: [points]
- [etc.]

**Note:** Minor syntax errors will not be heavily penalized. Focus is on correct logic and understanding of the workflow.

**Total: [sum] points**
```

---

## Chapter-Specific Adaptations

### Chapter 1 (EDA):
**Conceptual focus:**
- When to use different visualizations
- Data quality issues and solutions
- Interpretation of distributions and patterns
- AI prompting strategies
- Purpose of different types of tests

**Code focus:**
- Loading and filtering data (Pandas)
- Creating visualizations (Seaborn)
- Basic statistics
- Writing simple test functions

**Imports:**
```python
import pandas as pd
import seaborn as sns
import matplotlib.pyplot as plt
```

### Cha 2 (Intro ML Models):
**Conceptual focus:**
- Classification vs regression identification
- Model selection justification
- Metric interpretation (R², MSE, accuracy, precision, recall, F1)
- Understanding overfitting
- Hyperparameter concepts
- Scaling importance

**Code focus:**
- Train/test split
- Model instantiation with parameters
- Fit/predict workflow
- Metric calculation
- Simple comparison functions

**Imports:**
```python
import pandas as pd
import numpy as np
from sklearn.model_selection import train_test_split
from sklearn.linear_model import LinearRegression, LogisticRegression
from sklearn.tree import DecisionTreeClassifier
from sklearn.neighbors import KNeighborsClassifier
from sklearn.metrics import accuracy_score, mean_squared_error, r2_score
```

### Module 3 (ML Theory):
**Conceptual focus:**
- Loss function selection and interpretation
- Bias-variance tradeoff
- Optimization concepts (gradient descent)
- Overfitting vs underfitting diagnosis
- Training/validation/test set methodology

**Code focus:**
- Implementing simple loss functions
- Creating train/val/test splits
- Comparing models on different metrics
- Plotting learning curves

### Module 4 (Regression):
**Conceptual focus:**
- Linear regression assumptions
- When regularization helps
- Interpreting coefficients
- Residual analysis
- Multicollinearity problems
- Choosing between Ridge/Lasso/Elastic Net

**Code focus:**
- Fitting linear regression variants
- Computing residuals
- Polynomial feature creation
- Regularized regression with alpha parameter
- Diagnostic plotting

### Module 5 (Classification):
**Conceptual focus:**
- Choosing appropriate evaluation metrics
- Precision-recall tradeoffs
- Class imbalance handling
- Decision boundary interpretation
- Feature importance understanding
- When to use different classifiers

**Code focus:**
- Multiple classifier implementation
- Confusion matrix creation
- ROC curve plotting
- Handling class weights
- Feature importance extraction

### Module 6 (Neural Networks):
**Conceptual focus:**
- When neural networks are appropriate
- Activation function selection
- Architecture design reasoning
- Interpreting training curves
- Overfitting diagnosis
- Regularization techniques (dropout, batch norm)

**Code focus:**
- Reading PyTorch model definitions
- Understanding layer structures
- Creating DataLoaders
- Interpreting training loop code
- Plotting loss curves

### Module 7 (Pretrained Models):
**Conceptual focus:**
- When to use pretrained vs train from scratch
- Transfer learning concepts
- Fine-tuning vs feature extraction
- Model selection from Hugging Face
- Understanding model cards
- Trade-offs between model size and accuracy

**Code focus:**
- Loading pretrained models
- Basic inference code
- Understanding tokenization
- Data format preparation for pretrained models
- Interpreting model outputs

---

## Quality Checklist

Before finalizing a quiz, verify:

- [ ] Total points add up correctly (typically 25-50)
- [ ] Conceptual and code sections are roughly balanced (±5 points)
- [ ] Time estimate is reasonable (30-45 min)
- [ ] All necessary imports are listed for code section
- [ ] Questions progress from simpler to more complex
- [ ] Multi-part questions use consistent formatting (a, b, c)
- [ ] Conceptual questions require reasoning, not just recall
- [ ] Code questions are realistic to write by hand
- [ ] Grading rubric is clear and complete
- [ ] Note about syntax errors is included
- [ ] Questions align with module learning objectives
- [ ] Scenarios are realistic and relatable
