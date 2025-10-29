# Bank Marketing Project

**Predictive analytics for direct bank marketing campaigns using Machine Learning models.**

## 📋 Description

Academic project to predict whether a client will subscribe to a financial product after a direct marketing campaign. Implements multiple classification algorithms with comprehensive performance evaluation.

**Professor:** Salvador García (UGR)
**Data:** Private (confidentiality commitment with partner university)

---

## 🗂️ Project Structure
```
Bank_Marketing_Project/
├── 00_setup/                  # Configuration and initialization
│   ├── _setup.R              # Main setup script
│   └── utils.R               # Reusable functions
├── 01_data/                  # Data (NOT included in repository)
│   └── raw/
│       ├── bank-full.csv     # ⚠️ PRIVATE - Complete dataset
│       └── bank.csv          # ⚠️ PRIVATE - Reduced dataset
├── 02_eda/                   # Exploratory Data Analysis
├── 03_models/                # Individual models
├── 04_comparison/            # Model comparison
├── 05_outputs/               # Results (NOT included in repository)
├── .gitignore                # Git exclusions
├── README.md                 # This file
└── Guion_BankMarketing.pdf   # Activity description
```

---

## ⚠️ Private Data

**Data files are NOT included in this repository** due to confidentiality commitment with external collaborators.

### How to obtain the data:

1. **Contact the professor (Salvador García)** to request access to:
   - `bank-full.csv` (45,211 records, 20 variables)
   - `bank.csv` (4,521 records, 20 variables)

2. **Place the files in:**
```
   01_data/raw/bank-full.csv
   01_data/raw/bank.csv
```

3. **Scripts will automatically search** in these locations

---

## 🚀 Quick Start

### Requirements

- **R >= 4.0**
- **Packages:** See `00_setup/_setup.R`

### Installation
```r
# 1. Clone the repository
git clone https://github.com/EzequielLopezF/Bank_Marketing_Project.git
cd Bank_Marketing_Project

# 2. Obtain private data (contact the professor)
# Place bank-full.csv and bank.csv in 01_data/raw/

# 3. Run setup in R
source("00_setup/_setup.R")

# 4. Verify project structure
verify_project_structure()
print_project_info()
```

---

## 📦 Required Packages

Automatically loaded by `load_pkgs()`:

**Data & ML:**
- `readr`, `dplyr`, `tidyr`, `forcats` - Data manipulation
- `caret` - ML framework
- `ranger` - Random Forest
- `rpart`, `rpart.plot` - Decision trees
- `pROC` - ROC curves
- `kernlab`, `e1071` - SVM
- `glmnet` - Regularized logistic regression

**Visualization:**
- `ggplot2` - Graphics
- `patchwork` - Plot composition
- `pheatmap`, `RColorBrewer` - Heatmaps

**Utilities:**
- `tibble`, `fs`, `withr`

---

## 🔧 Main Functions

### Setup (`_setup.R`)
- `verify_project_structure()` - Validates project directories
- `print_project_info()` - Reproducibility information
- `log_project_section()` - Structured logging

### Utilities (`utils.R`)

**Data:**
- `load_bank_data()` - Load and preprocess data
- `create_train_test_split()` - Stratified split
- `apply_onehot_encoding()` - One-hot encoding

**Metrics:**
- `.metrics_from_cm()` - Extract metrics from confusion matrix
- `metricas_bin()` - Custom binary metrics
- `cramersV()` - Cramér's V for categorical association

**Visualization:**
- `plot_roc()` - ROC curve
- `plot_variable_importance()` - Variable importance
- `plot_metrics_comparison()` - Model comparison

**I/O:**
- `save_model()`, `load_model()` - Model persistence
- `save_metrics()`, `save_plot()` - Save results

---

## 📊 Reproducibility

All scripts use:
- **Global seed:** `13` (configurable in `_setup.R`)
- **Structured logging** to track execution
- **Structure validation** before starting

To reproduce exactly:
```r
source("00_setup/_setup.R")  # Configures everything automatically
```

---

## 📈 Implemented Models

- ✅ Logistic Regression
- ✅ Decision Trees
- ✅ Random Forest
- ⏳ SVM (in development)
- ⏳ Neural Network (in development)

---

## 📝 Notes

- This project follows professional guidelines for reproducibility and best practices
- Data is **confidential** and cannot be publicly shared
- Generated models (`05_outputs/`) are excluded from Git (regenerable)

---

## 👤 Author

**Ezequiel S. López Fernández** - Student  
**Professor:** Salvador García (UGR)

---

## 📄 License

Private - Academic use only
