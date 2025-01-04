# **Decision Tree Algorithm Project**

## **Overview**
This repository contains the implementation of a Decision Tree algorithm for classification tasks, applied to two datasets:
1. Fraud Detection: Classifies individuals as "Risky" or "Good" based on taxable income and other attributes.
2. Sales Analysis: Identifies attributes contributing to high sales for a cloth manufacturing company.

---

## **Datasets**
1. **Fraud Detection Dataset:**
   - Attributes: Undergrad, Marital.Status, Taxable.Income, Work Experience, Urban.
   - Target: "Risky" (Taxable.Income ≤ 30,000) or "Good".

2. **Sales Dataset:**
   - Attributes: Sales, CompPrice, Income, Advertising, Population, Price, ShelveLoc, Age, Education, Urban, US.
   - Target: Categorical variable derived from `Sales`.

---

## **Project Structure**
```
📂 Decision-Tree-Algorithm
├── 📁 data                # Dataset files
│   ├── fraud_data.csv
│   ├── sales_data.csv
├── 📁 notebooks           # Jupyter notebooks for data exploration and model building
│   ├── fraud_detection.ipynb
│   ├── sales_analysis.ipynb
├── 📁 scripts             # Python scripts for modular code
│   ├── preprocess.py      # Data preprocessing functions
│   ├── train_model.py     # Model training and evaluation
│   ├── visualize_tree.py  # Decision tree visualization
├── 📁 results             # Outputs such as visualized trees and metrics
│   ├── fraud_tree.png
│   ├── sales_tree.png
├── README.md              # Project overview
├── requirements.txt       # Python dependencies
├── LICENSE                # License details
└── .gitignore             # Files to ignore in Git
```

---

## **Key Features**
1. **Fraud Detection Model:**
   - Accuracy on Training Set: 1.0
   - Cross-Validation Score: 0.998
   - Visualized decision tree for interpretability.

2. **Sales Analysis Model:**
   - Identifies critical factors driving high sales.
   - Feature Importance:
     - Advertising: 16.01%
     - Population: 16.72%
     - ShelveLoc: 12.25%

---

## **Setup**
1. Clone this repository:
   ```bash
   git clone https://github.com/R-Mahesh45/Decision-Tree-Algorithm.git
   cd Decision-Tree-Algorithm
   ```
2. Install dependencies:
   ```bash
   pip install -r requirements.txt
   ```
3. Run the scripts:
   - For fraud detection:
     ```bash
     python scripts/train_model.py --dataset data/fraud_data.csv
     ```
   - For sales analysis:
     ```bash
     python scripts/train_model.py --dataset data/sales_data.csv
     ```

---

## **Results**
- **Fraud Detection Tree:**
  ![Fraud Tree](![download (2)](https://github.com/user-attachments/assets/86612b54-c1dc-463f-8a1a-d993e31db6df))

- **Sales Analysis Tree:**
  ![Sales Tree](![download (3)](https://github.com/user-attachments/assets/deaa34a1-cb4a-4cfd-a54e-d041a26abec7))


---

## **Visualization**
- Visualize decision trees:
  ```python
  from sklearn.tree import plot_tree
  import matplotlib.pyplot as plt

  plt.figure(figsize=(15, 10))
  plot_tree(model, filled=True, feature_names=X.columns, class_names=["Risky", "Good"])
  plt.show()
  ```
---
