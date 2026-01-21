# 🛒 Market Basket Optimization using Apriori Algorithm

![Python](https://img.shields.io/badge/Python-3.x-blue.svg)
![Library](https://img.shields.io/badge/Library-MLxtend-orange.svg)
![Visualization](https://img.shields.io/badge/Visualization-Plotly-green.svg)

## 📌 Overview
This project implements **Market Basket Analysis** using the **Apriori Algorithm** to identify associations between products in a retail dataset. By analyzing transaction history, the model discovers strong rules (e.g., *“If a customer buys X, they are likely to buy Y”*) to optimize store layouts, cross-selling strategies, and recommendation engines.

## 🚀 Key Features
* **Data Preprocessing:** Converts raw transaction lists into a One-Hot Encoded boolean matrix using `TransactionEncoder`.
* **Frequent Itemset Mining:** Utilizes the Apriori algorithm to filter items meeting a specific support threshold.
* **Association Rule Generation:** Derives rules based on **Lift**, **Confidence**, and **Support**.
* **Targeted Analysis:** Includes functionality to filter rules for specific items (e.g., analyzing what pairs well with "Eggs").
* **Interactive Visualization:** Visualizes the relationship between Support, Confidence, and Lift using Plotly scatter plots.

## 🛠️ Technologies Used
* **Python**: Core programming language.
* **Pandas**: Data manipulation and structure.
* **MLxtend**: Implementation of Apriori and Association Rules.
* **Plotly**: Interactive data visualization.

## 📊 Methodology

### 1. Metrics Explained
To evaluate the strength of the relationships, we use three key metrics:
* **Support**: How frequently an itemset appears in the dataset.
* **Confidence**: The likelihood of item B being purchased when item A is purchased.
* **Lift**: The ratio of the observed support to that expected if X and Y were independent. A lift > 1 indicates a strong positive correlation.

### 2. Workflow
1.  **Data Loading**: Ingests the `Market_Basket_Optimisation.csv` dataset.
2.  **Preprocessing**: Transforms the list of transactions into a format suitable for the algorithm (One-Hot Encoding).
3.  **Model Training**:
    * `min_support = 0.01` (1%)
    * `metric = "lift"`
    * `min_threshold = 1.2`
4.  **Visualization**: Plots Support vs. Confidence, where color represents Lift.

## 📈 Results & Insights
Based on the analysis of the dataset, several strong association rules were discovered. Top performing rules include:

* **Herb & Pepper ➔ Ground Beef**: High Lift (~3.29), indicating a very strong relationship.
* **Spaghetti & Mineral Water ➔ Ground Beef**: Significant correlation.
* **Frozen Vegetables ➔ Tomatoes**: Frequently purchased together.

### Example Output (Top Rules)
| Antecedents | Consequents | Support | Confidence | Lift |
| :--- | :--- | :--- | :--- | :--- |
| (herb & pepper) | (ground beef) | 0.016 | 0.323 | 3.29 |
| (spaghetti, mineral water) | (ground beef) | 0.017 | 0.286 | 2.91 |

## 📷 Visualization
The project includes an interactive scatter plot generated via Plotly to visualize the trade-off between Support and Confidence for the generated rules.

---
**Author:** [Samir Mohamed]
