# Image Placeholders for Module 4 - Regression Models

## Required Images

### 1. residual-patterns-placeholder.png
**Description:** Common patterns in residual plots and what they indicate
**Suggested content:**
- 2x3 grid showing six residual vs. fitted plots:
  - **Top Left - Good:** Random scatter around zero (no pattern)
    - Title: "Assumptions Met"
  - **Top Middle - Non-linearity:** Curved pattern (U-shaped or inverted-U)
    - Title: "Non-linear Relationship"
  - **Top Right - Heteroscedasticity:** Funnel shape (variance increases)
    - Title: "Non-constant Variance"
  - **Bottom Left - Outliers:** Most points near zero, few far away
    - Title: "Outliers Present"
  - **Bottom Middle - Clusters:** Distinct groups of points
    - Title: "Missing Categorical Variable"
  - **Bottom Right - Systematic Pattern:** Clear trend (upward or downward)
    - Title: "Missing Variable"
- Each plot: X-axis = "Fitted Values", Y-axis = "Residuals"
- Horizontal line at y=0 on each plot
- Red points for emphasis on problem areas

**Dimensions:** ~1200x800px

---

### 2. multicollinearity-example-placeholder.png
**Description:** Visualization showing multicollinearity and its effects
**Suggested content:**
- Two side-by-side visualizations:
  - **Left Panel - Correlation Heatmap:**
    - 5x5 correlation matrix
    - Color-coded (dark blue = -1, white = 0, dark red = +1)
    - Highlight one pair with correlation ~0.95
    - Labels: "Feature 1", "Feature 2", "Feature 3", "Feature 4", "Feature 5"
  - **Right Panel - Coefficient Instability:**
    - Bar plot showing coefficients for the same model fit on slightly different data
    - Two sets of bars (Data Sample 1 vs Data Sample 2)
    - Large differences between the two samples for highly correlated features
    - Stable coefficients for uncorrelated features
    - Title: "Unstable Coefficients with Multicollinearity"

**Dimensions:** ~1000x500px

---

### 3. regression-workflow-placeholder.png
**Description:** Flowchart showing complete regression analysis workflow
**Suggested content:**
- Flowchart with boxes and arrows:
  1. **Start:** "Fit Linear Regression"
  2. **Check:** "Create Diagnostic Plots" (residuals, Q-Q, etc.)
  3. **Decision Diamond:** "Assumptions Met?"
     - **Yes arrow** → "Validate Performance" → "Report Results"
     - **No arrow** → "Identify Problem"
  4. **Problem boxes:**
     - "Non-linear?" → "Add Polynomial Features"
     - "Multicollinearity?" → "Use Ridge/Lasso"
     - "Outliers?" → "Investigate/Transform"
  5. All problem solutions loop back to "Fit Model" (step 1)
- Use different colors for different stages (blue=fit, orange=diagnose, green=fix)
- Arrows showing the iterative nature

**Dimensions:** ~800x1000px

---

### 4. regularization-comparison-placeholder.png (Optional)
**Description:** Visual comparison of Ridge, Lasso, and Linear Regression coefficients
**Suggested content:**
- Three bar plots side-by-side:
  - **Left:** Linear Regression coefficients (some very large positive/negative)
  - **Middle:** Ridge coefficients (all shrunk toward zero, none exactly zero)
  - **Right:** Lasso coefficients (some shrunk to exactly zero)
- Same features on x-axis for all three
- Y-axis: coefficient value
- Different colors for each bar
- Clear labels showing which features Lasso set to zero
- Title above each: "Linear Regression", "Ridge (α=1)", "Lasso (α=1)"

**Dimensions:** ~1200x400px

---

### 5. coefficient-path-placeholder.png (Optional)
**Description:** Regularization path showing how coefficients change with alpha
**Suggested content:**
- Line plot with:
  - X-axis: log(alpha) from small (0.001) to large (1000)
  - Y-axis: coefficient value
  - Multiple lines, one for each feature (different colors)
  - Lines shrinking toward zero as alpha increases (Ridge) or dropping to exactly zero at different alphas (Lasso)
- Legend identifying each feature
- Vertical dashed line showing optimal alpha selected by cross-validation
- Title: "Lasso Regularization Path"

**Dimensions:** ~800x600px

---

## Notes

- Images should be placed in this `/images/` folder
- Use `.png` format for diagrams and screenshots
- Use descriptive filenames
- Ensure images are readable when embedded in Quarto HTML output
- For diagnostic plots, use realistic-looking synthetic data
- Color code consistently (e.g., red for problems, green for good)
- Include clear labels and titles on all plots
