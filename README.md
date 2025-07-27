# Fairness-Aware-Logistic-Regression-Using-Demographic-Parity-and-Balance-Metrics
Evaluate and improve fairness in ML models using demographic parity and balance metrics on synthetic data.

![Python](https://img.shields.io/badge/Python-3.10-blue?logo=python&logoColor=white)
![Logistic Regression](https://img.shields.io/badge/Model-Logistic%20Regression-brightgreen)
![Fairness](https://img.shields.io/badge/Fairness-Metrics-critical?logo=scikitlearn&logoColor=white)
![Status](https://img.shields.io/badge/Accuracy-100%25-success)

**Notebook**: [Open in Google Colab ](https://colab.research.google.com/drive/14DfOfYuAfOkBKMTI6GnhahWnWG8EUlSP?usp=sharing)

---

##  Project Overview

This project demonstrates fairness evaluation using a binary classification model. The task involves:

- Building a **Logistic Regression** model  
- Measuring **Demographic Parity** and **Balance**
- **Visualizing** group and class distributions
- Performing **data interventions** to reduce bias

---

## Dataset Summary

| Group | Selected (Class 1) | Rejected (Class 0) | Total |
|-------|--------------------|--------------------|-------|
| A     | 207                | 135                | 342   |
| B     | 143                | 215                | 358   |
| **Total** | **350**         | **450**            | **700** |

---

## Results Snapshot

### Before Intervention
| Metric              | Value      |
|---------------------|------------|
| Accuracy            | ✅ **100%** |
| Demographic Parity  | ❌ 0.2698   |
| Balance             | ⚠️ 0.6971   |

### After Intervention
| Metric              | Value      |
|---------------------|------------|
| Accuracy            | ✅ **100%** |
| Demographic Parity  | ✅ 0.1763   |
| Balance             | ✅ 0.7668   |

---

## Intervention Strategy

To reduce disparity:
-  Added **positive samples** to **Group B** to raise its selection rate.
-  Added **negative samples** to **Group A** to prevent over-selection.

 This **improved fairness** metrics **without compromising** model accuracy.

---

##  Visualizations

### 1. Scatter Plot of Groups and Selection Outcomes

![Scatter Plot](fairml_scatter_plot.png)

### 2. Fairness Metrics Comparison (Before vs After)

![Metrics Comparison](fairml_metrics_comparison.png)

---

##  How to Run

1. Click the notebook link above   
2. Run all cells sequentially  
3. Try modifying sample ratios to observe real-time fairness metric changes

---

## License

This project is for educational purposes only as part of **Fair ML (CIS 6930)** at the **University of South Florida**.
