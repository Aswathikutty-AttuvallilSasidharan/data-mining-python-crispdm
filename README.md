\# Data Mining Assignment Replication (WEKA → Python)



This repository reproduces a WEKA-based data mining assignment using \*\*Python\*\*, following the \*\*CRISP-DM\*\* framework.  

It includes classification (Titanic), association rule mining (Bookstore), and clustering (Volvo), with added visualizations and reproducible code.



\## Datasets

\- \*\*Titanic dataset\*\*: passenger attributes (class, age group, sex) and survival outcome.

\- \*\*Bookstore dataset\*\*: transaction-style binary purchases for association rule mining.

\- \*\*Volvo dataset\*\*: customer behavior features for clustering/segmentation.



\## Methods

\### 1) Titanic (Classification)

\- Model: \*\*Decision Tree (entropy)\*\* – equivalent to WEKA J48

\- Target variable: \*\*Survival status (Survived / Died)\*\*

\- Features: passenger class, age group, and sex

\- Evaluation: \*\*10-fold cross-validation\*\*

\- Class imbalance handling: \*\*class-weighted decision tree\*\*



\*\*Results\*\*

\- Baseline Decision Tree achieved ~78% accuracy but showed bias toward the majority class (Died).

\- Confusion matrix analysis revealed many survivors misclassified as died.

\- Applying `class\_weight="balanced"` significantly improved recall for the \*\*Survived\*\* class, reducing false negatives and providing a fairer model, at the cost of a moderate increase in false positives.

\- Survival recall improved from ~53% (unbalanced model) to ~71% after applying class weighting.

\- Key insight: \*Passenger sex and class are the strongest predictors of survival.\*





\### 2) Bookstore (Association Rule Mining)

\- Model: \*\*Apriori\*\*

\- Metrics: support, confidence, lift

\- Output: frequent itemsets and association rules for bundle/marketing insights



\### 3) Volvo (Clustering)

\- Model: \*\*K-Means\*\*

\- Model selection: Elbow method (WCSS)

\- Output: customer segments for targeted marketing strategies



\## Project Structure

data-mining-python-crispdm/

├── data/ # raw datasets

├── notebooks/ # Jupyter notebooks (analysis)

├── reports/

│ ├── figures/ # saved charts

│ └── results/ # outputs (tables, CSV)

├── requirements.txt

└── README.md





\## How to Run

1\. Create and activate a virtual environment:

&nbsp;  - Windows:

&nbsp;    ```bash

&nbsp;    python -m venv venv

&nbsp;    venv\\Scripts\\activate

&nbsp;    ```

2\. Install requirements:

&nbsp;  ```bash

&nbsp;  pip install -r requirements.txt

Start Jupyter:

jupyter notebook

Tools Used



Python: pandas, numpy



ML: scikit-learn, mlxtend



Visualization: matplotlib



Version control: Git + GitHub



Author



Aswathikutty Attuvallil Sasidharan









