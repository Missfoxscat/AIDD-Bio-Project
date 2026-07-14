## AIDD-Bio-Project (GSE183947 Target Discovery)

Welcome to my AI-driven Drug Discovery (AIDD) foundational repository. This project demonstrates end-to-end bioinformatics workflows, moving from raw gene expression data processing to therapeutic target identification.

## Project Roadmap
- [x] **Phase 1: Project Scaffolding** - Establish a modular Python pipeline for bioinformatics.
- [ ] **Phase 2: DEG Analysis** - Differential Expression Gene analysis on GSE183947.
- [ ] **Phase 3: Visualization** - Generate volcano plots & heatmaps for key oncogenes (e.g., TP53, BRCA1).
- [ ] **Phase 4: Web Deployment** - Build and host a dynamic Streamlit-based target discovery app.

##  Tech Stack & Modular Architecture
- **Language:** Python
- **Data Engineering:** Pandas, NumPy
- **Statistics:** SciPy (T-test)
- **Visualization:** Matplotlib, Seaborn
- **Architecture:** Modular toolbox (`my_bio_tools.py`)

## Directory Structure
```text
AIDD_Bio_Project/
├── data/         # Raw gene expression matrix (GSE183947)
├── src/          # Custom modular python tools (my_bio_tools.py)
└── notebooks/    # Jupyter interaction & step-by-step analysis
