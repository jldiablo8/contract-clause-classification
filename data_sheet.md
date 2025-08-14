# Dataset Datasheet

## Dataset Name
Contract Clause Classification Dataset

## Dataset Description
This dataset contains excerpts of legal contract clauses paired with their corresponding clause types. It is designed for use in text classification tasks aimed at automatically identifying clause categories within contracts.

## Dataset Source
- Originates from the CUAD (Contract Understanding Atticus Dataset) provided by The Atticus Project.
- Available at: https://huggingface.co/datasets/the_atticus_project/cuad

## Dataset Version
- Version: 1.0
- Date accessed: [Insert date you accessed/downloaded]

## Dataset Composition

| Feature Name | Description                              | Data Type | Example                          |
|--------------|---------------------------------------|-----------|---------------------------------|
| clause_text  | Text of a contract clause              | String    | "This Agreement shall remain..."|
| clause_type  | Category/label of the clause           | String    | "Confidentiality"               |

## Dataset Size
- Number of rows: Approximately 13,000 clauses (training set)
- Number of unique clause types: 41

## Data Collection Process
- The original dataset was created by manual annotation of contract clauses across various legal contracts.
- Each clause is associated with a question (clause type) and corresponding answer spans.

## Data Preprocessing
- Clauses with missing text or labels were removed.
- Text was cleaned and vectorized using TF-IDF in preprocessing notebooks.
- Target labels were encoded with LabelEncoder.

## Dataset Use
- Intended for supervised learning in legal NLP tasks such as clause classification.
- Useful for research and development of contract analytics tools.

## Distribution and Licensing
- The CUAD dataset is publicly available for research purposes under its own license.
- Please refer to The Atticus Project website and original dataset license for details.

## Ethical Considerations
- Dataset contains publicly available contract clauses.
- No personal or sensitive information included.
- Users should be aware of limitations in generalizing models trained on this dataset to all contract types.

## Limitations
- Dataset may have domain bias towards certain contract types.
- Clause categories may overlap or be ambiguous in some cases.
- Does not cover all possible clause types in the legal industry.

## Recommended Citation
If you use this dataset in your work, please cite:

@misc{hendrycks2021cuad,
title={CUAD: An Expert-Annotated NLP Dataset for Legal Contract Review},
author={Dan Hendrycks and Thomas Erickson and Mantas Mazeika and Andy Zou and Dawn Song},
year={2021},
url={https://github.com/TheAtticusProject/cuad}
}


---

## Contact Information
For questions about the dataset or this project, contact:

Lei Jiao
jzl9@hotmail.com  
