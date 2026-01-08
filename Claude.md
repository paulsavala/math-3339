# MATH 3339 - Introduction to Data Science - AI-assisted redesign

## Course Philosophy

This course emphasizes conceptual understanding and practical application over implementation details. Students will develop the analytical thinking needed to select appropriate models, recognize when assumptions are violated, and critically evaluate model performance. While AI coding assistants are powerful tools, this course ensures students build the foundational knowledge to use them effectively and debug their output.

## Agentic Planning

When developing this course, Claude should follow the following guidelines:

1. Utilize the existing folder Claude-planning by creating Markdown files to keep track of progress. Claude should keep one file per topic, and each file should have a clear title and a clear description of the topic. Each file should outline specifically what is being taught, which parts are done "by hand" (either programming or mathematically) and which parts are done with AI coding assistants. Claude should describe the in-class activities and homework which will enforce learning these topics.
2. When designing a lesson and/or topic, Claude should refer back to the existing Claude-planning folder to ensure consistency and avoid redundancy. In addition, when possible, Claude should try to build on previous lessons and topics to create a cohesive and progressive learning experience. This should be transparent to the learner, with lessons refering back to previous lessons and topics whenever possible.

## Assignment Templates

When creating homework assignments or quizzes, Claude must follow the templates defined in the Templates/ folder:

### Homework Assignments

**Template Location:** `Templates/homework-template.md`

**Key Requirements:**

1. **Two-Part Structure:**

   - **Part A: By Hand (40-45 points)** - 10 questions without AI assistance to build foundational skills
   - **Part B: With AI Assistance (55-60 points)** - 10 questions using AI coding assistants to scale analysis
   - Total: 100 points across 20 questions

2. **Part A Focus (By Hand):**

   - Basic implementation of techniques/models
   - Evaluation and interpretation of results
   - Writing helper functions to demonstrate understanding
   - Explaining concepts in own words
   - Creating simple visualizations
   - Question range: 3-5 points each

3. **Part B Focus (AI-Assisted):**

   - Hyperparameter tuning at scale
   - Comparing 5+ models/approaches simultaneously
   - Building automation pipelines
   - Cross-validation and robustness testing
   - Final comprehensive analysis with executive summary
   - Question range: 5-7 points each
   - **MUST require students to submit their AI prompts used**

4. **Required Sections:**

   - Instructions (including dataset descriptions)
   - Part A questions (1-10)
   - Part B questions (11-20)
   - Submission Guidelines
   - Grading Rubric
   - Tips for Success (separate subsections for Part A, Part B, and General)

5. **Required Deliverables for Part B:**

   - Code (AI-generated but student-verified)
   - Outputs (visualizations, tables, results)
   - Written interpretation (student's own analysis)
   - **The prompt(s) used with AI assistant**

6. **Tips Section Must End With:**
   - "Use your brain. That's what it's there for."

### Quizzes

**Template Location:** `Templates/quiz-template.md`

**Key Requirements:**

1. **Two-Section Structure:**

   - **Section A: Conceptual Questions (~50% of points)** - Testing understanding without a computer
   - **Section B: Code Writing (~50% of points)** - Writing code by hand
   - Total: Typically 25-50 points
   - Time: 30-45 minutes

2. **Section A Focus (Conceptual):**

   - Scenario identification (classification vs regression, problem types)
   - Metric interpretation and trade-off reasoning
   - Model selection justification
   - Conceptual explanations
   - Problem diagnosis
   - Question range: 2-4 points each
   - 6-8 questions total

3. **Section B Focus (Code Writing):**

   - Data manipulation (load, filter, split)
   - Model instantiation with parameters
   - Fit/predict workflow
   - Metric calculation
   - Simple function writing
   - Question range: 2-4 points each
   - 5-7 questions total
   - **Must include assumption section listing all imports**

4. **Required Elements:**

   - Instructions (time, format, note about partial credit)
   - Section A questions
   - Assumption section before Section B (listing imports and available variables)
   - Section B questions
   - Grading Rubric with statement: "Minor syntax errors will not be heavily penalized. Focus is on correct logic and understanding of the workflow."

5. **Code Writing Philosophy:**
   - Syntax perfection NOT required
   - Focus on logic and correct approach
   - Grading: 70-80% for correct logic, 20-30% for syntax
   - Questions must be realistic to write by hand

### Textbook Chapters

**Template Location:** `Templates/textbook-chapter-template.md`

**Key Requirements:**

1. **Structure:**

   - Front matter (YAML with title, format settings)
   - Module Resources section linking to homework and quiz
   - Introduction (3-5 engaging paragraphs)
   - 8-10 major sections covering core topics
   - Summary (synthesizing key concepts)
   - Practice Exercises (4-6 exercises)
   - Additional Resources

2. **Code Examples:**

   - Include code every 2-3 paragraphs maximum
   - Use executable Python code with proper imports
   - Build complexity gradually throughout the chapter
   - Explain what code does and why it matters
   - Use realistic datasets and examples

3. **Images and Visualizations:**

   - Include 2-3 images/diagrams per chapter
   - Create `images/` subfolder in module folder
   - Create `placeholder-info.md` describing needed images
   - Use relative paths: `![Description](images/filename.png)`

4. **Writing Style:**

   - Conversational and casual tone
   - Use probing questions rather than direct statements
   - Maximum 2-3 paragraphs before showing code
   - Start with intuition, then formalize
   - Connect to what students already know
   - End summary with: "Use your brain. That's what it's there for."

5. **Quarto-Specific Requirements:**
   - Use `{python}` for executable code blocks (not standard markdown code blocks)
   - Include `jupyter: python3` in YAML front matter
   - Set `code-fold: false` to show all code by default
   - Use callout boxes for tips, notes, and warnings:
     - `::: {.callout-tip}` for helpful tips
     - `::: {.callout-note}` for important information
     - `::: {.callout-warning}` for cautions

### Using the Templates

When asked to create homework, quiz, or textbook chapter for a module:

1. **Read the appropriate template** from `Templates/homework-template.md`, `Templates/quiz-template.md`, or `Templates/textbook-chapter-template.md`
2. **Review the module-specific adaptations** section in the template
3. **Follow the structure exactly** - do not deviate from point distributions, section organization, or required elements
4. **Refer to content-overview.md** to understand:
   - Core topics for the module
   - What should be done by-hand vs with AI
   - Learning objectives
   - Assessment focus
5. **Create or update the Claude-planning file** for the module first, then generate content
6. **Ensure content aligns** with the "Topics Done By-Hand" and "Topics Done With AI" from content-overview.md

## Tech Stack

1. Lessons will be written as Quarto Markdown documents, with the programming language used being Python 3.12.
2. Students will use the Gemini CLI as the primary AI coding assistant. The primary model will be Flash 2.5, which means code generation skills are limited. Because of this, the text should encourage students to work on small components at a time, rather than prompting the model to build entire applications all at once.
3. Students will host their work on Github.
4. Python packages used include:
   - Pandas
   - NumPy
   - Seaborn
   - Scikit-learn
   - PyTorch
   - Streamlit
   - Huggingface

## Style Guidelines

### General Writing Style

The professor writes in a casual, conversational manner that emphasizes understanding over formality. Key characteristics:

**Tone and Voice:**

- Write as if talking directly to students
- Use probing questions to guide thinking rather than directly stating answers
- Avoid overly formal academic language
- Be direct and honest about challenges and complexities
- Show enthusiasm for the subject matter

**Common Phrases and Patterns:**

- "Let's jump in" / "Let's start with..."
- "Here's the thing..." / "Here's what's happening..."
- "But wait—why does that work?"
- "Don't worry about X right now, just..."
- "See what happened?" / "Notice what's going on here?"
- "Use your brain. That's what it's there for." (ending phrase)

**Example of the Professor's Writing Style:**

```
"Linear regression is perhaps the most important idea in machine learning. Once you understand the ins-and-outs of linear regression you can understand most other machine learning models as well. This is because the ideas developed for machine learning were first perfected on linear regression and then applied to other models. Let's jump in.

Linear regression (LR) is what you have probably referred to as "line of best fit". It is a line meant to fit the data "as well as possible". I put that last phrase in quotes, because what exactly do we mean by a "best fit"? We will formulate this mathematically in the next section.

With that out of the way, we now turn to our next question: why do we care about linear regression? Linear regression is extremely important because it allows us to make predictions. Up until this point we have only explored and described the past by looking at datasets which (necessarily) had data about the past. However, the point of data science is largely to make predictions about the future using data from the past. This works because a line doesn't care what data we plug in. We can plug in data from the past in order to verify and explain past performance. But we can also plug in future numbers (dates, pricing changes, expected changes to our products, etc.) and see what the model returns.

Let's start with a simple example. Don't worry about the code right now, just look at the graphs. We will work again with our data/boston.csv dataset, describing the median home value in various neighborhoods in Boston.

In blue is the actual measurements of poverty and home value for all neighborhoods. In red is the predicted value using the line of best fit. We can see that the regression line seems to fit the data fairly well, at least in all except the far left and right ends.

One interesting thing to note is that the regression line generally seems too high. For example, if we draw the same graph, but only keep poverty values between 5% and 20% we get the following:

Why is that? The reason is that the regression line is heavily affected by outliers. So the neighborhoods with low crime and high home value are throwing off the line and "dragging it up." In general, you want the following four things to be true before using LR for making predictions:

1. The data should be approximately linear

2. The observations should be independent (so the crime rate and median home value in one neighborhood should be independent of other neighborhoods)

3. The variance between the measurements should be approximately the same throughout the graph (the graph is more or less spread out the same amount in different areas)

4. The points should be approximately normally distributed around the regression line.

None of these four are perfectly satisfied. However, that doesn't mean you can't use LR. It just means that you need to be careful when making predictions. Don't just make a regression line and say "see, this predicts the future!" Use your brain, that's what it's there for."
```

### Textbook Chapter Writing Guidelines

**Conceptual Explanations:**

- Start with intuition and concrete examples before formalizing
- Use analogies and real-world scenarios to ground abstract concepts
- Ask guiding questions that lead students to understanding
- Build complexity gradually—simple cases first, then complications
- Connect new concepts to what students already know
- Explain the "why" before diving into the "how"

**Code Demonstrations:**

- Include code examples every 2-3 paragraphs maximum
- Never show code without explaining what it does and why it matters
- Build code examples incrementally (don't dump large blocks)
- Use realistic datasets that students can relate to
- Comment code to explain reasoning, not just mechanics
- Show output or visualizations when relevant
- Follow this pattern:
  1. Brief intro to what you're demonstrating
  2. Show the code
  3. Explain what happened and why
  4. Connect to the bigger picture

**Code Formatting for Quarto:**

- Use `{python}` for executable code blocks: ` ```{python} `
- Use regular markdown code blocks only for non-executable examples
- Add `#| error: true` to code blocks that intentionally raise errors
- Use `#| echo: true` (default) to show code
- Use `#| output: true` to display output

**Examples and Datasets:**

- Use consistent, realistic datasets throughout a chapter
- California housing data (from Module 1) is the primary dataset
- Include real-world context for all examples
- Make examples build on each other when possible
- Show both successes and failures (what not to do)

**Visual Elements:**

- Include 2-3 images/diagrams per chapter minimum
- Create `images/` subfolder with `placeholder-info.md`
- Use callout boxes for important points:
  - `::: {.callout-tip}` for helpful tips and best practices
  - `::: {.callout-note}` for important information students must remember
  - `::: {.callout-warning}` for common mistakes and cautions
- Use concrete visualizations to explain abstract concepts

**Section Flow:**

- Each major section should have a clear narrative arc
- Start sections with context: why does this matter?
- End sections with synthesis: what did we learn?
- Use transitions to connect sections logically
- Reference earlier content when building on it
- Preview upcoming content when it's relevant

**Practical Examples:**

- Always ground theory in practice
- Show real scenarios where the concept matters
- Include "what could go wrong" examples
- Demonstrate debugging and problem-solving approaches
- Connect to real data science workflows

**Ending Every Chapter:**

- Summary must synthesize, not just list topics
- Emphasize key takeaways and connections
- Always end with: "Use your brain. That's what it's there for."

**Writing Theoretical Concepts:**

When explaining theoretical or conceptual material (like ML theory, loss functions, optimization, etc.):

- **Start with the practical problem** before introducing theory
  - Example: "Models fail. They overfit. They underfit. Understanding what's going on 'under the hood' helps you recognize these problems..."
  - Lead with why this matters in practice, then explain the theory

- **Use concrete, visual examples first**
  - Show actual code and visualizations before equations
  - Let students see the concept in action before formalizing it
  - Example: Demonstrate gradient descent with a simple quadratic function and visualization before explaining the algorithm

- **Explain concepts in plain English**
  - "Cross-entropy heavily penalizes confident wrong predictions"
  - "The gradient is the slope of the loss with respect to parameters"
  - Avoid jargon or explain it immediately when used

- **Use analogies and metaphors**
  - "Think of it as navigating a landscape where height represents loss, and you're trying to find the lowest valley"
  - "Bias: fitting a straight line to clearly curved data"
  - "Variance: fitting a wiggly line that goes through every single training point"

- **Break down mathematical concepts step-by-step**
  - Introduce notation gradually
  - Explain what each symbol means in context
  - Show the formula, then explain it in words
  - Example: Show cross-entropy formula, then explain "this heavily penalizes confident wrong predictions"

- **Use callout boxes strategically**
  - `::: {.callout-note}` for connecting concepts ("Cross-entropy is just the log-likelihood for binary classification")
  - `::: {.callout-warning}` for common misconceptions or pitfalls
  - `::: {.callout-tip}` for practical advice about when/how to use concepts

- **Connect theory back to practice repeatedly**
  - "In practice, you rarely need to implement loss functions yourself—scikit-learn handles it"
  - "Understanding what they're doing helps you choose the right one and diagnose problems"
  - Always answer "why does this matter for my work?"

- **Use contrasts and comparisons**
  - "MSE: Penalizes large errors heavily (good when outliers are costly)"
  - "MAE: Treats all errors equally (good when outliers shouldn't dominate)"
  - Side-by-side visualizations showing different approaches

- **Emphasize intuition over rigor**
  - Get the concept across first, worry about edge cases later
  - "The idea is beautifully simple: calculate the gradient, take a step downhill, repeat"
  - Don't get bogged down in mathematical proofs

- **Use progressive disclosure**
  - Start with 1D examples before moving to higher dimensions
  - "In one dimension, the gradient is simply the derivative. In higher dimensions..."
  - Build from simple → complex gradually

- **Frame concepts as tools, not just theory**
  - "Loss functions define what 'good' means"
  - "The bias-variance tradeoff is your guide for choosing model complexity"
  - Present concepts as practical tools students will use

---

## Technical Guidelines

When writing code examples in textbook chapters and assignments, follow these package-specific best practices to ensure code is clear, correct, and pedagogically sound.

### Pandas

**DataFrame Display:**

- **Never use `print()` for DataFrames** - Instead, put the DataFrame (or `df.head()`) as the last line of the cell to use Jupyter's rich display
- **Always use `.head()` to show DataFrames** - This prevents overwhelming output and teaches good practices

```python
# BAD: Using print()
print(housing_df)

# GOOD: Let Jupyter display it
housing_df.head()
```

**DataFrame Creation:**

- **Never subset data when creating DataFrames** - Create the full DataFrame first, then display a subset
- This prevents confusing students about what's actually in the DataFrame

```python
# BAD: Subsetting during creation
comparison = pd.DataFrame({
    'Actual': y_test.head(10),
    'Predicted': predictions[:10]
})
comparison

# GOOD: Full DataFrame, then show subset
comparison = pd.DataFrame({
    'Actual': y_test,
    'Predicted': predictions
})
comparison.head()
```

**Column Selection:**

- Always demonstrate both single-column (Series) and multi-column (DataFrame) selection
- Emphasize that double brackets `[[]]` for multiple columns are just a list inside brackets

```python
# Single column (returns Series)
house_values = housing_df['median_house_value']

# Multiple columns (returns DataFrame)
subset = housing_df[['median_house_value', 'ocean_proximity']]
```

**Chaining Operations:**

- Break complex chains across multiple lines for readability
- Add comments explaining each step

```python
# GOOD: Clear, multi-line chaining
result = (housing_df
          .dropna()  # Remove missing values
          .groupby('ocean_proximity')  # Group by location
          .agg({'median_house_value': 'mean'}))  # Calculate means
```

### Scikit-learn

**Train-Test Split:**

- **Always set `random_state`** for reproducibility
- Always split data BEFORE any other operations
- Use meaningful variable names: `X_train, X_test, y_train, y_test`

```python
# GOOD: Always set random_state
X_train, X_test, y_train, y_test = train_test_split(
    X, y,
    test_size=0.2,
    random_state=42
)
```

**Model Workflow:**

- Always follow the same pattern: instantiate → fit → predict → evaluate
- Show the complete workflow in early examples
- Use consistent variable names: `model`, `predictions`, `y_pred`

```python
# The standard pattern
model = LinearRegression()  # 1. Instantiate
model.fit(X_train, y_train)  # 2. Fit
y_pred = model.predict(X_test)  # 3. Predict
score = model.score(X_test, y_test)  # 4. Evaluate
```

**Feature Scaling:**

- **Always fit scaler on training data only**, then transform both train and test
- Never fit on the full dataset or test set

```python
# GOOD: Fit on train, transform both
scaler = StandardScaler()
X_train_scaled = scaler.fit_transform(X_train)
X_test_scaled = scaler.transform(X_test)  # Only transform, don't fit

# BAD: Fitting on test data
# X_test_scaled = scaler.fit_transform(X_test)  # DON'T DO THIS
```

**Model Comparison:**

- When comparing models, use consistent train/val/test splits
- Store results in a DataFrame for easy comparison

```python
# GOOD: Systematic comparison
results = []
for name, model in models.items():
    model.fit(X_train, y_train)
    score = model.score(X_test, y_test)
    results.append({'Model': name, 'Score': score})

results_df = pd.DataFrame(results)
results_df
```

### Matplotlib/Seaborn

**Figure Display:**

- Always use `plt.show()` to display figures in Quarto documents
- Set figure size explicitly with `plt.figure(figsize=(width, height))`

```python
# GOOD: Explicit figure size and show
plt.figure(figsize=(10, 6))
sns.scatterplot(data=housing_df, x='median_income', y='median_house_value')
plt.title('House Value vs. Median Income')
plt.xlabel('Median Income (in $10k)')
plt.ylabel('Median House Value ($)')
plt.show()
```

**Labels and Titles:**

- **Always include title, xlabel, and ylabel**
- Use descriptive labels with units
- Make figures self-explanatory

**Color Usage:**

- Use colorblind-friendly palettes: `'Set2'`, `'colorblind'`, `'husl'`
- Never rely solely on red-green distinctions

### NumPy

**Random State:**

- Always set `np.random.seed()` for reproducibility in examples

```python
# GOOD: Set seed for reproducibility
np.random.seed(42)
random_values = np.random.randn(100)
```

**Array Creation:**

- Use `np.array()` for small examples, but prefer Pandas for tabular data
- Show array shape and dtype when relevant

### General Python

**Variable Naming:**

- Use descriptive variable names: `housing_df`, `X_train`, `y_pred`
- Follow conventions: `X` (features), `y` (target), `df` (DataFrame)
- Avoid single letters except in mathematical contexts or brief examples

**Comments:**

- Comment the "why", not the "what"
- Use comments to explain reasoning and decisions
- Add comments for code that students will modify or extend

```python
# GOOD: Explains reasoning
# Use median instead of mean to avoid influence of outliers
median_bedrooms = housing_df['total_bedrooms'].median()

# BAD: States the obvious
# Calculate median
median_bedrooms = housing_df['total_bedrooms'].median()
```

**Error Handling:**

- Use `#| error: true` in Quarto code blocks that intentionally raise errors
- Show errors when teaching debugging or demonstrating common mistakes

```python
#| error: true
# This will raise an error to demonstrate the problem
assert 2 > 3, "This assertion will fail"
```

### Code Organization in Chapters

**Progressive Complexity:**

- Start with simplest working example
- Add complexity gradually
- Show complete workflow first, then optimize

**Reusable Patterns:**

- Establish patterns early and reuse them
- Highlight when you're using a pattern seen before
- Make patterns explicit: "This is the same workflow we used for..."

**Avoid:**

- Magic numbers without explanation
- Unexplained imports (always show imports)
- Copy-pasted code without variation
- Examples that don't run or produce errors unintentionally
- Deprecated functions or outdated syntax
