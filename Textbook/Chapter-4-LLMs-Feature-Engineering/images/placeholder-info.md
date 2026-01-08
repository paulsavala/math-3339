# Image Placeholders for Chapter 4: LLMs for Feature Engineering and Data Extraction

This document describes the images needed for Chapter 4. These should be created and placed in this directory.

## Required Images

### 1. llm-extraction-workflow.png
**Location in chapter:** Section 1.4 "The LLM Advantage: Zero-Shot Extraction"

**Description:**
A flowchart showing the complete LLM extraction workflow:
- **Input:** Unstructured text (review, ticket, post)
- **Step 1:** Write prompt + include text
- **Step 2:** Call LLM API
- **Step 3:** Receive JSON response
- **Step 4:** Parse and validate
- **Step 5:** Convert to DataFrame
- **Step 6:** Feed to ML model
- **Output:** Predictions

Use boxes and arrows to show flow from left to right. Include icons or visual indicators for each step (text icon, API icon, JSON icon, table icon, model icon).

**Purpose:** Give students the big picture of how LLM extraction fits into an ML pipeline

**Suggested tools:** Draw.io, Lucidchart, PowerPoint, or Figma

---

### 2. prompt-comparison.png
**Location in chapter:** Section 3.1 "The Anatomy of a Good Extraction Prompt"

**Description:**
Side-by-side comparison showing:

**Left side - BAD PROMPT:**
```
Tell me about this review:
[review text]
```
Response: *Vague, unstructured answer*

**Right side - GOOD PROMPT:**
```
Extract sentiment from this review.
Answer with: positive, negative, or neutral

Review: [review text]

Sentiment:
```
Response: *"positive"*

Use red ✗ for bad prompt, green ✓ for good prompt. Highlight the key differences (specificity, format, clarity).

**Purpose:** Visually demonstrate what makes a good extraction prompt

**Suggested tools:** Screenshot and annotate, or create in PowerPoint/Keynote

---

### 3. cost-comparison-chart.png
**Location in chapter:** Section 6.1-6.2 "Understanding Token-Based Pricing" and "Calculating Extraction Costs"

**Description:**
Bar chart comparing costs for processing 10,000 reviews across different LLMs:
- X-axis: LLM model (GPT-3.5-turbo, GPT-4, Claude Sonnet, Gemini)
- Y-axis: Total cost in dollars (logarithmic scale)
- Bars showing relative costs with actual dollar amounts labeled

Example values:
- GPT-3.5: $0.50
- GPT-4: $5.00
- Claude: $2.50
- Gemini: $0.40

Use color coding: green for cheapest, yellow for moderate, red for expensive.

**Purpose:** Make the dramatic cost differences between models immediately visible

**Suggested approach:** Create with matplotlib/seaborn or Excel/Google Sheets

---

### 4. quality-vs-cost.png
**Location in chapter:** Section 6.3 "When to Use Which Model"

**Description:**
Scatter plot showing the quality-cost tradeoff:
- X-axis: Extraction quality/accuracy (70% - 95%)
- Y-axis: Cost per extraction (logarithmic scale, $0.0001 - $0.01)
- Points for different approaches:
  - Regex/Keywords: Low cost, moderate quality (bottom left)
  - GPT-3.5: Low-moderate cost, good quality (middle)
  - GPT-4: High cost, high quality (top right)
  - Traditional ML: Low cost (once trained), good quality (bottom middle-right)

Add labels for each point. Draw a "sweet spot" circle around GPT-3.5 area.

**Purpose:** Help students visualize the tradeoff between cost and quality

**Suggested approach:** matplotlib scatter plot with annotations

---

### 5. extraction-validation.png
**Location in chapter:** Section 7.1 "Measuring Extraction Accuracy"

**Description:**
Visual example showing correct vs incorrect extractions:

**Top section - Correct Extractions (✓):**
- Review: "Love this product!" → Extracted: "positive" → Ground truth: "positive"
- Review: "Terrible quality." → Extracted: "negative" → Ground truth: "negative"

**Bottom section - Incorrect Extractions (✗):**
- Review: "It's not bad." → Extracted: "negative" → Ground truth: "positive"
  - Annotation: "Missed double negative"
- Review: "I expected amazing quality..." → Extracted: "positive" → Ground truth: "negative"
  - Annotation: "Only read first part"

Use green checkmarks for correct, red X's for incorrect. Add brief explanations for why errors occurred.

**Purpose:** Show students what to look for when validating extractions

**Suggested tools:** PowerPoint, Google Slides, or design tool

---

### 6. when-to-use-llms.png
**Location in chapter:** Section 8.1 "Decision Framework"

**Description:**
Decision tree flowchart for choosing extraction method:

Start: "Need to extract information from text"
↓
Question 1: "Is it simple pattern matching (emails, phone numbers)?"
→ YES: Use Regex
→ NO: Continue

Question 2: "Do you have 1000+ labeled examples?"
→ YES: Train Traditional ML
→ NO: Continue

Question 3: "Need to understand context/nuance?"
→ YES: Use LLM
→ NO: Try Regex/Keywords first

Use diamond shapes for questions, rectangles for decisions. Color-code paths (green for simple solutions, yellow for moderate complexity, blue for LLM).

**Purpose:** Give students a practical decision-making framework

**Suggested tools:** Draw.io, Lucidchart, or flowchart software

---

## Image Style Guidelines

All images should follow these guidelines:

1. **Resolution:** At least 1200px wide for diagrams, 1000px wide for plots
2. **Format:** PNG with transparent background where appropriate
3. **Colors:** Use colorblind-friendly palettes
   - Blue (#3498db) for primary elements
   - Orange (#e67e22) for secondary elements
   - Green (#2ecc71) for success/correct elements
   - Red (#e74c3c) for errors/warnings
4. **Fonts:** Use clear, readable fonts (Arial, Helvetica, or similar)
5. **Style:** Professional but approachable—match the textbook's conversational tone
6. **Labels:** All axes, boxes, and elements should be clearly labeled
7. **Size:** Large enough text that it's readable when embedded in the document

## Priority Order

If time is limited, create images in this priority order:

1. **llm-extraction-workflow.png** - Most important for understanding the overall process
2. **prompt-comparison.png** - Critical for teaching effective prompting
3. **cost-comparison-chart.png** - Essential for understanding cost implications
4. **when-to-use-llms.png** - Practical decision-making tool
5. **quality-vs-cost.png** - Helps with model selection
6. **extraction-validation.png** - Nice to have for quality control section

## Notes

- Cost comparison chart can be generated directly from Python using matplotlib
- Quality vs cost scatter plot should also be generated programmatically
- The workflow diagram and decision tree need to be created manually with diagramming tools
- Prompt comparison can be screenshots from actual code/API calls with annotations added
- Use consistent color schemes across all images for professional appearance
- Consider creating a Python script to generate the data visualization plots for consistency
