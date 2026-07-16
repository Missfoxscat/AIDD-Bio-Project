# Breast-Cancer-AI-Target-Discovery
> **An End-to-End AI-driven Pipeline: From RNA-Seq Differential Expression to Clinical Target Discovery & Robust Machine Learning Diagnosis**

---

## 🌟 Executive Summary
This project delivers a complete, end-to-end bioinformatics and machine learning pipeline to identify high-confidence clinical biomarkers for breast cancer and construct a highly robust diagnostic classifier. 

Starting from raw expression matrices (GSE183947), we isolated **110 statistically significant candidate targets**, mapped their systemic biological mechanisms via **KEGG enrichment**, and trained a **Random Forest Classifier** that achieves a state-of-the-art diagnostic accuracy.

---

## 🚀 Pipeline Workflow & Key Results

### 1. Differential Expression Analysis (DEA)
Using standard Student's t-test and Fold-Change filtering ($\vert{}log_2FC\vert{} > 2$, $p < 0.01$), we identified **110 robustly altered genes** (53 up-regulated, 57 down-regulated in breast cancer tissues).
* **Key Visual**: 
  ![Volcano Plot](./volcano_plot.png) *(注：这里替换成你画的那张高颜值火山图文件名)*
* **Deliverable**: Generated an industry-standard clinical candidate report: `GSE183947_Breast_Cancer_Target_Report.xlsx` with top targets highlighted.

### 2. Functional Enrichment & Pathway Analysis (Biological Interpretation)
To uncover the molecular mechanisms of our 110 target genes, we performed **KEGG Pathway Enrichment analysis** via the Enrichr API.
* **Key Visual**: 
  ![KEGG Enrichment](./kegg_pathway_enrichment.png) *(注：替换成你的气泡图)*
* **Insight**: The targets are predominantly enriched in **Cell Cycle ($p < 10^{-5}$)**, **Cellular Senescence**, and immune-related pathways, providing strong biological verification of their oncogenic driving roles.

### 3. AI Diagnostic Classifier & Explainable AI (XAI)
We trained a **Random Forest Classifier** utilizing only the **top 10 target genes** as features. 
* **Explainable AI**: Features were ranked by Gini Importance. **MMP11 (27.1%)** emerged as the single most critical diagnostic feature, aligning perfectly with its clinical role in cancer metastasis.
* **Key Visual**: 
  ![Feature Importance](./feature_importance.png) *(注：替换成特征重要性条形图)*

### 4. Rigorous Clinical Validation (5-Fold Cross-Validation)
To guarantee clinical generalizability and prevent overfitting, we subjected the model to a **Stratified 5-Fold Cross-Validation**.
* **Performance**: Achieved an outstanding **Mean AUC of 0.96 ± 0.05**, with multiple folds reaching a perfect AUC of 1.00.
* **Key Visual**: 
  ![5-Fold ROC](./5fold_cross_validation_roc.png) *(注：替换成你刚刚生成的 ROC 曲线图)*

---

## 🛠️ Tech Stack & Dependencies
* **Bioinformatics**: `Pandas`, `NumPy`, `SciPy (t-test)`, `Requests (Enrichr API)`
* **Machine Learning**: `Scikit-Learn (Random Forest, K-Fold, Metrics)`
* **Visualization**: `Matplotlib`, `Seaborn` (Configured to academic-publication style)

---

## 📂 Repository Structure
```text
├── data/                  # Placeholder for raw expression matrix
├── src/
│   ├── data_cleaning.py   # Data preprocessing & DEA
│   ├── enrichment.py      # KEGG Enrichment API pipeline
│   └── classifier.py      # Random Forest & 5-Fold Cross-validation
├── results/               # Saved figures and Excel reports
├── README.md
