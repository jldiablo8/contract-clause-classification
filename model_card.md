# Model Card: Contract Clause Classification

## Model Overview
This model classifies legal contract clauses into predefined types using classical machine learning techniques. It has been trained on a dataset of labeled clauses and utilizes TF-IDF vectorization followed by a classifier (e.g., Logistic Regression, SVM).

## Intended Use
- **Use Cases**:
  - Automating legal document review
  - Clause classification in contracts for risk assessment
  - Legal clause extraction for compliance tools

- **Users**:
  - Legal tech developers
  - Contract analysts
  - NLP researchers

## Dataset
- **Source**: `data/contract_clauses.csv`
- **Fields**:
  - `clause_text`: The full text of the clause
  - `clause_type`: The label indicating clause category

## Preprocessing
- Removed nulls
- Applied TF-IDF vectorization with stop word removal
- Label encoded `clause_type`

## Model Architecture
- **Baseline**: Logistic Regression
- **Optimized Model**: Support Vector Machine (SVC) with hyperparameters tuned using Bayesian Optimization

## Evaluation Metrics
- **Accuracy**
- **Precision, Recall, F1-score**
- **Confusion Matrix**
- Macro and weighted F1 scores used for imbalanced class evaluation

## Performance Summary
| Model         | Accuracy | Macro F1 | Weighted F1 |
|---------------|----------|----------|-------------|
| Logistic Reg. | XX%      | XX       | XX          |
| SVC (BayesOpt)| XX%      | XX       | XX          |

> Replace XX with actual results

## Limitations
- Performance depends on clause variety and label balance
- Not tested on multilingual or non-legal clauses
- Does not handle very long or deeply contextual clauses (consider BERT for that)

## Ethical Considerations
- Misclassification of legal clauses may impact compliance or legal understanding
- Model should be used to assist humans, not replace them

## Citation
If you use this model or dataset, please cite or acknowledge this repository.

