# Homework Assignment Template

## Template Guidelines

### Overall Structure

All homework assignments should follow this two-part structure:
- **Part A: By Hand (40-45 points)** - No AI assistance, 10 questions
- **Part B: With AI Assistance (55-60 points)** - Using AI coding assistants, 10 questions

Total: 100 points across 20 questions

### Point Distribution

**Part A (40-45 points):**
- Questions should range from 3-5 points each
- Simpler questions (identifying concepts, basic code): 3-4 points
- More complex questions (writing functions, multi-step analysis): 4-5 points

**Part B (55-60 points):**
- Questions should range from 5-7 points each
- Standard AI-assisted tasks: 5-6 points
- Comprehensive final question with executive summary: 7 points

### Question Types

**Part A - By Hand:**
1. **Conceptual identification** (3 points): Identify problem types, match concepts
2. **Basic implementation** (3-4 points): Load data, implement single model/technique
3. **Evaluation and interpretation** (4-5 points): Calculate metrics, create visualizations, interpret results
4. **Function writing** (4-5 points): Write reusable functions that demonstrate understanding
5. **Explanation questions** (4-5 points): Explain concepts in own words, justify decisions

**Part B - AI Assisted:**
1. **Hyperparameter tuning** (5-6 points): Test multiple parameter combinations systematically
2. **Large-scale comparison** (5-6 points): Compare many models/approaches simultaneously
3. **Automation** (5-6 points): Create functions that automate repetitive tasks at scale
4. **Feature engineering/exploration** (5-6 points): Test multiple feature combinations or data transformations
5. **Cross-validation/robustness** (5-6 points): Evaluate across multiple splits or conditions
6. **Comprehensive pipeline** (6-7 points): End-to-end workflow combining multiple steps
7. **Final integrated project** (7 points): Complete analysis with executive summary

### Part A Characteristics

**Goals:**
- Build foundational skills that cannot be outsourced to AI
- Ensure students understand the underlying concepts
- Practice the basic workflow that AI will scale up in Part B
- Develop intuition for when something is wrong

**Topics covered by-hand:**
- Basic library usage and syntax
- Single-model implementation
- Metric calculation and interpretation
- Simple visualizations
- Understanding what code does and why
- Explaining concepts in own words
- Recognizing patterns and problems

**Typical progression:**
1. Conceptual warm-up (identify problem types, match definitions)
2. Basic data loading and exploration
3. Implement 2-4 different techniques/models individually
4. Evaluate and compare using appropriate metrics
5. Create basic visualizations
6. Write helper functions demonstrating understanding
7. Explain concepts and justify decisions

### Part B Characteristics

**Goals:**
- Scale up the techniques learned in Part A
- Practice effective AI prompting
- Learn to verify and understand AI-generated code
- Tackle problems too large/tedious to do by hand
- Build comprehensive pipelines and workflows

**AI assistance is used for:**
- Testing many hyperparameters systematically
- Comparing 5+ models simultaneously
- Creating comprehensive visualization suites
- Automating repetitive tasks
- Building end-to-end pipelines
- Generating formatted reports
- Cross-validation and robustness testing

**Required deliverables for each question:**
- The code (AI-generated but verified by student)
- Outputs (visualizations, tables, results)
- Written interpretation (student's own analysis)
- **The prompt(s) used with AI assistant**

**Typical progression:**
1. Hyperparameter tuning for single model type
2. Compare multiple models at scale
3. Explore impact of different choices (features, scaling, etc.)
4. Build automation functions/pipelines
5. Perform robust evaluation (cross-validation, multiple conditions)
6. Comprehensive integrated analysis with executive summary

### Dataset Requirements

**Provide 1-2 datasets per assignment:**
- Should be realistic and somewhat messy (matching real-world data)
- Include both numerical and categorical features
- Should align with module topics
- Clearly specify which dataset to use for which questions
- Include complete column descriptions

**Example dataset formats:**
- Module 1 (EDA): housing_data.csv
- Module 2 (ML Models): employee_salaries.csv (regression) + customer_churn.csv (classification)
- Module 4 (Regression): Include features with multicollinearity, outliers
- Module 5 (Classification): Include class imbalance, multiple classes

### Writing Style and Tone

**Instructions:**
- Clear, direct, and specific
- Use numbered lists for multi-part questions
- Bold key terms and concepts
- Specify exact deliverables expected

**Questions:**
- Start with action verbs: "Calculate", "Create", "Explain", "Compare", "Write"
- Include context and reasoning prompts: "Why?", "How does X affect Y?", "What do you notice?"
- For Part B: explicitly request AI prompts as deliverables

**Tips sections:**
- Casual but helpful tone
- Practical, actionable advice
- Separate tips for Part A, Part B, and General
- End with: "Use your brain. That's what it's there for."

### Formatting Guidelines for Quarto Markdown

**IMPORTANT - List Rendering:**
- Lists preceded by bold text, headings, or other content **MUST** have a blank line before the list starts
- Without the blank line, Quarto will not render the list properly

**Correct formatting:**
```markdown
**Deliverables:**

- Code
- Visualizations
- Written interpretation
```

**Incorrect formatting (will not render as list):**
```markdown
**Deliverables:**
- Code
- Visualizations
- Written interpretation
```

**Apply this rule to:**
- Deliverables sections in Part B questions
- Dataset column descriptions
- Multi-part question items (a, b, c)
- Submission guidelines
- Tips sections
- Any list following text, bold text, or headings

### Grading Rubric

**Part A (40-45 points):**
- Code correctness and functionality: ~55%
- Proper implementation of techniques: ~25%
- Written interpretations and explanations: ~20%

**Part B (55-60 points):**
- Code functionality and correctness: ~45%
- Quality and specificity of AI prompts: ~25%
- Visualizations and comparative analysis: ~20%
- Written interpretations and insights: ~10%

### Standard Sections

**Every homework should include:**

1. **Title and metadata** (Quarto YAML header)
2. **Instructions section** with:
   - Due date (to be assigned)
   - Two-part structure explanation
   - Submission requirements (code, visualizations, written answers, AI prompts)
   - Dataset descriptions
3. **Part A: By Hand** (10 questions, 40-45 points)
4. **Part B: With AI Assistance** (10 questions, 55-60 points)
5. **Submission Guidelines** (ZIP file contents)
6. **Grading Rubric** (detailed breakdown)
7. **Tips for Success** (Part A, Part B, General)

---

## Homework Template Structure

```markdown
---
title: "Module [X] Homework: [Topic Name]"
format:
  html:
    toc: true
    toc-depth: 3
    code-fold: false
    theme: cosmo
jupyter: python3
---

## Instructions

**Due Date:** [To be assigned by instructor]

This homework is divided into two parts. Part A should be completed **without AI assistance** to build your foundational [skills/understanding of topic]. Part B should be completed **with AI assistance** (like Gemini CLI) to practice [scaling your work/tackling more comprehensive tasks].

For all questions, submit:

1. Your code (in a `.py` file or Jupyter notebook)
2. All visualizations generated
3. Written answers to interpretation questions (can be in markdown or comments)
4. For Part B: Include the prompts you used with the AI assistant

### Dataset(s)

[Provide 1-2 dataset descriptions with column explanations]

**[Dataset Name 1]:** `filename.csv` contains [description] with columns:

- `column1`: Description (note if TARGET variable)
- `column2`: Description
- [etc.]

---

## Part A: By Hand (No AI Assistance)

Complete questions 1-10 without using AI coding assistants. The goal is to build your foundational [skills in X].

### Question 1 ([3-5] points)

[Question text with clear instructions]

[Optional: Multi-part with a), b), c)]

---

### Question 2 ([3-5] points)

[Continue pattern for 10 questions total]

---

[Questions 3-10...]

---

## Part B: With AI Assistance

For questions 11-20, you should use an AI coding assistant (like Gemini CLI) to help you write and scale your [analysis/code/experiments]. The goal is to practice [specific AI-assisted skills].

**Important:** For each question, save the prompt(s) you used with the AI assistant. Part of your grade will be based on the quality of your prompts.

---

### Question 11 ([5-7] points)

[Question text]

**Deliverables:**

- Code
- [Visualizations/Tables/Results]
- Written interpretation ([X] sentences)
- Your AI prompt(s)

---

### Question 12 ([5-7] points)

[Continue pattern for 10 questions total]

---

[Questions 12-19...]

---

### Question 20 (7 points)

[Comprehensive final question requiring integration of multiple concepts]

Write a [length] executive summary ([word count] words) that explains:

- [Point 1]
- [Point 2]
- [Point 3]
- [etc.]

**Deliverables:**

- Complete [workflow/analysis] code (well-commented)
- All visualizations
- Executive summary
- Your AI prompt(s)
- Reflection: [Specific reflection question about AI-assisted vs by-hand work]

---

## Submission Guidelines

Submit a ZIP file containing:

1. **Code files:** All `.py` files or Jupyter notebooks
2. **Visualizations folder:** All plots and charts generated
3. **Written responses:** A single document (PDF or Markdown) with all your written answers, interpretations, and AI prompts used
4. **Data:** Include your processed datasets if you created any modifications

---

## Grading Rubric

**Part A: By Hand ([40-45] points)**

- Code correctness and functionality: [~22-25] points
- Proper implementation of [techniques/models]: [~10-11] points
- Written interpretations and explanations: [~8-10] points

**Part B: AI-Assisted ([55-60] points)**

- Code functionality and correctness: [~25-27] points
- Quality and specificity of AI prompts: [~14-15] points
- Visualizations and comparative analysis: [~11-12] points
- Written interpretations and insights: [~5-6] points

**Total: 100 points**

---

## Tips for Success

### For Part A:

- [3-5 specific, actionable tips relevant to the module]
- Test your code on small examples first
- Use meaningful variable names
- Comment your code to explain your reasoning

### For Part B:

- Write specific, detailed prompts
- If the AI's first attempt isn't quite right, refine your prompt
- Always review and test the AI-generated code
- Don't just accept AI output—understand what it's doing
- Include context in your prompts (e.g., "I'm working with a [dataset] with columns...")

### General:

- Start early—[module-specific reason]
- Your interpretations are just as important as your code
- If you find something interesting in the data, explore it further!
- Use your brain. That's what it's there for.
```

---

## Module-Specific Adaptations

### Module 1 (EDA):
- Focus: Data exploration, visualization, testing
- By-hand: Basic Pandas, Seaborn, simple statistics
- AI-assisted: Comprehensive profiling, many visualizations, complete test suites

### Module 2 (Intro ML Models):
- Focus: Model implementation, comparison, evaluation
- By-hand: Instantiate/fit/predict workflow, basic metrics
- AI-assisted: Hyperparameter tuning, comparing 5+ models, cross-validation

### Module 3 (ML Theory):
- Focus: Loss functions, optimization, bias-variance tradeoff
- By-hand: Implement simple loss functions, understand concepts
- AI-assisted: Compare many loss functions, visualize optimization landscapes

### Module 4 (Regression):
- Focus: Linear regression variants, regularization, diagnostics
- By-hand: Fit linear/ridge/lasso, residual analysis, interpret coefficients
- AI-assisted: Grid search over many alphas, polynomial feature testing, comprehensive diagnostics

### Module 5 (Classification):
- Focus: Multiple classifiers, evaluation metrics, class imbalance
- By-hand: Implement classifiers, confusion matrices, metric calculation
- AI-assisted: Hyperparameter tuning, handling imbalance strategies, comprehensive metric comparison

### Module 6 (Neural Networks):
- Focus: Network architecture, PyTorch, training loops
- By-hand: Read PyTorch code, understand architecture, plot training curves
- AI-assisted: Write training loops, architecture variations, extensive hyperparameter tuning

### Module 7 (Pretrained Models):
- Focus: Hugging Face, fine-tuning, transfer learning
- By-hand: Load and use pretrained models, basic inference
- AI-assisted: Fine-tuning pipelines, comparing many pretrained models, end-to-end applications
