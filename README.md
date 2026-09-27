# Advertising-Data
# Advertising Sales Prediction Engine 📊

Yeh repository ek end-to-end Machine Learning module implement karti hai jo testing aur structural validation metrics ke zariye multi-channel marketing campaigns (TV, Radio, Newspaper) ke budgets par **Continuous Product Sales** ko predict karta hai.

---

## 📋 Table of Contents
- [Project Overview](#project-overview)
- [Dataset Architecture](#dataset-architecture)
- [Core Preprocessing Pipeline](#core-preprocessing-pipeline)
- [Model Architecture & Framework](#model-architecture--framework)
- [Algorithmic Performance Evaluation](#algorithmic-performance-evaluation)
- [Interactive Interface Example](#interactive-interface-example)

---

## 🔍 Project Overview
Is predictive model ka buniyadi maqsad linear combination algorithm ka use karke continuous financial metrics ko interpret karna hai. Yeh application explicit feature isolation perform karti hai taake arbitrary budget variables ke target responses verify kiye ja sakein.

---

## 📊 Dataset Architecture
Model `Advertising.csv` [3] data stream consume karta hai jisme **200 global records** [3] aur distinct parameters darj hain:

| System Column | Data Type | Sub-Type Category |
| :--- | :--- | :--- |
| `ID` | `int64` | Identifier Key (Excluded) |
| `TV` | `float64` | Continuous Feature Vector |
| `Radio` | `float64` | Continuous Feature Vector |
| `Newspaper` | `float64` | Continuous Feature Vector |
| `Sales` | `float64` | Continuous Target Label |

---

## 🛠️ Core Preprocessing Pipeline
1. **Structural Isolation:** Data loading ke waqt continuous arrays ko inputs (`X`) aur core labels (`y`) mein matrix mapping par distribute kiya jata hai.
2. **Data Leakage Mitigation:** Module `train_test_split` parameter use karta hai jisme statistical split ratios fix hain:
   * **Training Allocation:** 80% matrix rows [3]
   * **Evaluation Testing:** 20% distinct rows [3]
   * **Deterministic Seed:** `random_state=42` [3]

---

## 🧠 Model Architecture & Framework
Predictive pipeline **Ordinary Least Squares Linear Regression** math engine implement karti hai:

* **Optimization Solver:** Explicit linear configuration vector alignment.
* **Execution Interface:** Matrix calculations direct memory optimization layers par parallel processed hain.

---

## 📈 Algorithmic Performance Evaluation
Validation benchmarks par model ne niche diye gaye operational evaluation outcomes display kiye hain:

* **Mean Absolute Error (MAE):** `~1.4608` units [3]
* **R-squared (R²) Variance Score:** `~89.94%` (`0.8994`) [3]

> **Insight:** R² metric runtime par verify karta hai ke humare inputs marketing channel investments ke lagbhag 90% variance ko safely explain kar rahe hain.

---

## 💻 Interactive Interface Example
Aap module ke andar default execution engine se custom query variables pass karke arbitrary testing run kar sakte hain:

```python
# Custom testing instance sequence execution
result = predict_sales(tv=100, radio=30, newspaper=20)
print("Predicted Sales Units:", result)
# Expected Vector Output: 13.1831
```
