# Image Placeholders for Chapter 5: Classification Models

This document describes the images/diagrams that should be created for Chapter 5 on Classification Models.

## 1. confusion-matrix-diagram.png

**Purpose**: A clean, annotated diagram explaining the structure of a confusion matrix

**Description**:
- 2x2 grid showing Predicted (columns) vs Actual (rows)
- Clearly labeled quadrants:
  - Top-left: True Negative (TN) - predicted negative, actually negative
  - Top-right: False Positive (FP) - predicted positive, actually negative (Type I error)
  - Bottom-left: False Negative (FN) - predicted negative, actually positive (Type II error)
  - Bottom-right: True Positive (TP) - predicted positive, actually positive
- Color coding: greens for correct predictions (TN, TP), reds for errors (FP, FN)
- Arrows showing how metrics are calculated:
  - Accuracy = (TP + TN) / Total
  - Precision = TP / (TP + FP)
  - Recall = TP / (TP + FN)

**Style**: Clean, professional diagram with clear labels. Use icons or simple graphics to make it visually appealing.

---

## 2. decision-boundary-comparison.png

**Purpose**: Side-by-side comparison of decision boundaries for different classifiers

**Description**:
- 2x3 grid of scatter plots (or 3x2)
- Each subplot shows the same 2D classification dataset (e.g., two classes in different colors)
- Six subplots showing decision boundaries for:
  1. Logistic Regression (linear boundary)
  2. Decision Tree depth=3 (rectangular/axis-aligned splits)
  3. Decision Tree depth=10 (more complex rectangular regions)
  4. Random Forest (smooth but irregular boundary)
  5. SVM with linear kernel (straight line)
  6. SVM with RBF kernel (curved boundary)
  7. k-NN with k=1 (very jagged, local boundary)
  8. k-NN with k=20 (smoother boundary)
- Each subplot clearly labeled with the model type
- Decision boundary shown as a bold line or colored region
- Data points shown as scattered dots with class colors

**Style**: Consistent color scheme across all subplots. Make it easy to compare the shapes of different boundaries.

---

## 3. roc-curve-interpretation.png

**Purpose**: Annotated ROC curve explaining how to interpret it

**Description**:
- Classic ROC curve plot (True Positive Rate vs False Positive Rate)
- Shows three example curves:
  1. Perfect classifier (hugs the top-left corner, AUC = 1.0)
  2. Good classifier (bow-shaped curve above diagonal, AUC ≈ 0.85)
  3. Random classifier (diagonal line, AUC = 0.5)
- Annotations pointing out:
  - "Best possible performance" at top-left corner (TPR=1, FPR=0)
  - "Random guessing" along the diagonal
  - Shaded area under curve with "AUC = Area Under Curve"
  - Arrow showing "Better models" direction (toward top-left)
- Optionally show a few threshold values along the good classifier curve

**Style**: Clear, educational diagram. Use different line styles (solid, dashed, dotted) for the three curves.

---

## 4. precision-recall-tradeoff.png

**Purpose**: Visualize the precision-recall tradeoff with threshold adjustment

**Description**:
- Two panels side-by-side or stacked:
  - Left/Top: Precision-Recall curve showing how precision and recall change as threshold varies
  - Right/Bottom: Line plot showing precision and recall as separate lines vs threshold value
- Annotations showing:
  - "High threshold → High precision, Low recall"
  - "Low threshold → Low precision, High recall"
  - The optimal F1 score point
- Visual example showing why the tradeoff exists (e.g., small threshold = predict positive more often = catch more positives but more false positives too)

**Style**: Clear, intuitive visualization. Use contrasting colors for precision vs recall lines.

---

## 5. class-imbalance-problem.png

**Purpose**: Illustrate why class imbalance is problematic

**Description**:
- Side-by-side comparison of balanced vs imbalanced datasets
- Left panel: Balanced dataset (50/50 split)
  - Pie chart or bar chart showing class distribution
  - Example confusion matrix from a reasonable classifier
  - Metrics: Accuracy = 85%, Precision = 83%, Recall = 87%
- Right panel: Imbalanced dataset (95/5 split)
  - Pie chart or bar chart showing class distribution
  - Example confusion matrix from a naive classifier (predicts majority class)
  - Metrics: Accuracy = 95% (misleading!), Precision = 0%, Recall = 0%
- Visual highlighting showing "95% accuracy but useless for minority class!"

**Style**: Use visual contrast to show the problem. Make it clear that high accuracy doesn't mean good performance on imbalanced data.

---

## 6. ensemble-method-illustration.png

**Purpose**: Conceptual diagram showing how Random Forests combine multiple decision trees

**Description**:
- Show the Random Forest process:
  1. Original dataset (shown as a grid or table icon)
  2. Arrows pointing to multiple bootstrap samples (3-5 copies with slight variations)
  3. Each sample trains a decision tree (show simplified tree diagrams)
  4. Trees make individual predictions (show thumbs up/down or class labels)
  5. Final prediction combines via voting (show majority vote mechanism)
- Annotations explaining:
  - "Bootstrap sampling (with replacement)"
  - "Random feature subset at each split"
  - "Majority vote for final prediction"
- Visual emphasis on diversity: show that trees are different from each other

**Style**: Flow diagram with clear arrows showing the process. Use icons and simple graphics to make it intuitive.

---

## Optional Additional Images

### 7. svm-margin-concept.png
- Diagram showing support vectors and the maximum margin
- Two parallel lines showing the margin
- Support vectors highlighted
- Decision boundary in the middle

### 8. knn-visualization.png
- Scatter plot showing a new point to classify
- Circles of different radii showing k=1, k=3, k=5 neighbors
- Visual showing how the class is determined by majority vote

### 9. sigmoid-function-detailed.png
- Plot of sigmoid function
- Annotations showing asymptotic behavior (approaches 0 and 1)
- Connection to logistic regression (linear combination → sigmoid → probability)

---

## Notes

- All images should use a consistent color palette throughout the chapter
- Use colorblind-friendly colors (avoid red-green only distinctions)
- Include clear labels and legends on all plots
- Keep diagrams simple and focused on one concept at a time
- Use professional fonts and consistent styling
- Save images as PNG with transparent backgrounds where appropriate
- Recommended size: 1200-2000 pixels wide for main diagrams
