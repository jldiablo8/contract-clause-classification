#  Contract Clause Classification

A machine learning pipeline to classify legal contract clauses using classical ML techniques. The project includes EDA, preprocessing, training, evaluation, and hyperparameter optimization.

---

## Project Structure

├── data/
│ └── contract_clauses.csv # Input dataset (clauses + labels)
├── 01_EDA_and_Preprocessing.ipynb # Exploratory data analysis + TF-IDF + train-test split
├── 02_Model_Training_and_Evaluation.ipynb # Logistic Regression + Evaluation
├── 03_Bayesian_Optimization.ipynb # SVM + Hyperparameter tuning via BayesSearchCV
├── MODEL_CARD.md # Detailed model card and performance metrics
├── README.md # This file
└── requirements.txt # Python dependencies


---

## Dataset

- **Filename**: `contract_clauses.csv`
- **Columns**:
  - `clause_text`: The raw text of a clause
  - `clause_type`: The category label (target)

> Note: Ensure the dataset is placed in the `data/` directory.

---

## 🔧 Setup Instructions

### 1. Clone the repository
```bash
git clone https://github.com/yourusername/contract-clause-classifier.git
cd contract-clause-classifier

### 2. Install dependencies
pip install -r requirements.txt

### 3. Run notebooks

Use Jupyter or VS Code to run the notebooks in order:

01_EDA_and_Preprocessing.ipynb

02_Model_Training_and_Evaluation.ipynb

03_Bayesian_Optimization.ipynb

## Models Used
Model	Purpose
LogisticRegression	Baseline classifier
SVC (SVM)	Optimized classifier with BayesSearchCV

Text vectorization via TfidfVectorizer (max 3000 features)

Labels encoded with LabelEncoder

## Evaluation Metrics

Accuracy

Precision / Recall / F1 (macro and weighted)

Confusion Matrix

Optional: Cross-validation & error analysis

## Hyperparameter Tuning

Used Bayesian Optimization via skopt.BayesSearchCV on the SVM classifier.

search_spaces = {
    'C': (1e-3, 1e3, 'log-uniform'),
    'gamma': (1e-4, 1e-1, 'log-uniform'),
    'kernel': ['rbf', 'poly', 'sigmoid']
}

## Saving Models

Trained models can be saved using:

from joblib import dump
dump(model, "model_name.joblib")

## Future Work

Integrate BERT or other transformer-based models

Build REST API (e.g., with FastAPI or Flask)

Deploy as a web app for clause classification

Add Named Entity Recognition (NER) for richer analysis

## Citation

If you use this project in your work, please cite:

@misc{yourusername2025contractclauses,
  author       = {Your Name},
  title        = {Contract Clause Classification},
  year         = {2025},
  publisher    = {GitHub},
  howpublished = {\url{https://github.com/yourusername/contract-clause-classifier}},
}

## License

This project is licensed under the MIT License.

## Acknowledgements

Scikit-learn

Scikit-optimize (skopt)

Seaborn

Matplotlib


---

### To Customize:

Replace:
- `yourusername` → your actual GitHub username
- `Your Name` → your name or organization
- Add your actual repo link in the citation and clone command

Let me know if you want help generating the `requirements.txt` or setting up a license file.
