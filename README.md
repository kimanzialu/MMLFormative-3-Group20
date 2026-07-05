# Formative 3 - Probability Distributions, Bayesian Probability, and Gradient Descent Implementation

This repository contains our team's complete implementation for Parts 1 through 4 of the assignment. We have built all core machine learning models from scratch using foundational mathematics and pure, native Python code.

---

## 1. Group Information & Contributions

| Team Member | Core Project Role & Responsibility | Assigned Tasks Covered |
| :--- | :--- | :--- |
| **Sahra** | EM Algorithm Lead & Documentation Coordinator | Part 1 Code, Main README Hub |
| **Kenny** | Text Pipeline Designer & Core Environment Setup | Part 2 Setup & Word Processing |
| **Denyse** | Mathematics Lead & Manual Derivations | Part 2 Bayes Logich |
| **Robert** | Automation Engineer & Graphics Specialist | Part 4 Code & Plot |

---

## 2. Part 1: EM Algorithm (Grouping Height Data)

### Core Analysis Question
* **Should you or should you not simply draw a line at the dataset's global mean to split the data into two piles, and then calculate the mean of each pile?**
* **Answer:** **No, you should not.** Splitting data strictly at a single middle line fails because real-world population data overlaps. A rigid cutoff line misclassifies data points near the center, creates high volatility, and ignores the true variance of the separate populations. The EM algorithm solves this by using soft probabilistic curves instead of a hard cutoff.

### Our Live Test Case Result (72.0 inches)
* **Probability it is a Child:** 0.47%
* **Probability it is a Parent:** 99.53%
* **Conclusion:** The model correctly and confidently classifies a 6-foot-tall individual into the parent distribution rather than the child distribution.

---

## 3. Part 2: Bayesian Sentiment Inference

### Project Boundaries
Per the assignment constraints, this text analyzer is built using **pure, basic Python math operations**—no hidden machine learning libraries like Scikit-Learn were used. 

### Final Keyword Probability Balance
We tracked specific positive and negative keywords to weigh movie review sentiment using Bayes' Theorem:

$$\text{Final \% Chance Review is Positive} = \frac{\text{How often the word is used in Positive reviews} \times \text{Baseline Positive rate}}{\text{Total times the word appears anywhere}}$$

* Tracking **positive words** (*excellent*, *wonderful*, *amazing*) successfully drives the final probability toward **100%**.
* Tracking **negative words** (*waste*, *awful*, *boring*) successfully drops the final probability toward **0%**.

---

## 4. Part 3 & 4: Gradient Descent Optimization

### Software Design (The DRY Principle)
To ensure the code is clean and completely unabstracted, we avoided pre-built, automated regression toolkits. We maintained the **DRY (Don't Repeat Yourself)** principle by packaging our matrix formulas inside a single execution `for` loop.

### Trajectory Interpretation
* **Loss Optimization:** Our calculated Mean Squared Error dropped rapidly from an initial **61.0000** down to a stabilized **2.3904** by the 4th iteration. This steep curve proves our gradient math successfully minimized system error.
* **Why Code and Manual Steps Differ:** The manual calculus steps in Part 3 were processed row-by-row to make individual group step handoffs manageable. The automated Python code utilizes true **Batch Gradient Descent**, evaluating all data constraints simultaneously. Both paths successfully arrive at the optimal solution.

---

## 5. Project Deliverables Checklist
**Main Notebook:** `gradient_descent_analysis.ipynb` (All code blocks fully executed)
**Manual Math Document:** `manual_calculations.pdf` (Handwritten matrix calculus steps)
**Project Hub:** `README.md` (This master summary file)
