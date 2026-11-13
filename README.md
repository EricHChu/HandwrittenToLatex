# Handwritten Math to LaTeX Using AI

**Authors:** Eric Chu, Janani Ramadass  

## Overview
An AI agent that converts images of handwritten mathematical expressions into LaTeX code. The system recognizes individual symbols, spatial layouts, and nested structures (e.g., fractions, exponents, and brackets) to transcribe handwritten math without solving the expressions.

## Approach & AI Methods
- **K-Means Clustering:** Segments handwritten math into atomic components (digits, variables, basic operators) and quantizes image breakdowns for normalized input.
- **Recursive Logistic Regression:** Classifies image segments into either atomic symbols (`1`, `x`, `+`, `-`) or composite structures (fractions, exponents, nested brackets), recursively decomposing complex expressions into base elements.
- **Rule-Based Inference Engine:** Applies formatting rules to assemble classified math components into valid LaTeX syntax.

## Dataset & Tools
- **Datasets:** Custom labeled dataset of handwritten symbols and LaTeX expressions, supplemented with [MNIST](http://yann.lecun.com/exdb/mnist/) and [MathWriting](https://arxiv.org/abs/2404.10690).
- **Tools:** OpenCV, `idx2numpy`, and `inkml2img` for image preprocessing and NumPy array conversion.

## Validation & Evaluation
- **Metrics:** Symbol classification accuracy, full-expression conversion accuracy, and **Token Error Rate (TER)** (measuring token insertions, deletions, and substitutions against ground-truth LaTeX).
- **Validation:** *k*-fold cross-validation for symbol classification and hold-out evaluation on unseen handwritten expressions.

## Schedule & Milestones
| Week | Dates | Milestone |
| :--- | :--- | :--- |
| **Week 1** | Nov 09 – Nov 15 | Process training data; train and validate model on atomic symbols (`x`, `y`, `12`, `+`, `-`). |
| **Week 2** | Nov 16 – Nov 22 | Train and validate model on basic composite structures (e.g., simple fractions, exponents). |
| **Week 3** | Nov 23 – Nov 29 | Build recursive model to identify nested complex structures. |
| **Week 4** | Nov 30 – Dec 06 | Train and validate full equation component recognition. |
| **Week 5** | Dec 07 – Dec 11 | Final evaluation, project demonstration, implementation, and report. |
