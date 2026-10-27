# Water Potability Predictions Comparision Using Machine Learning

## Project Overview
This project applies machine learning classification algorithms to predict water potability using water-quality measurements. It compares four models—Logistic Regression, Gaussian Naive Bayes, K-Nearest Neighbors (KNN), and Random Forest—and evaluates their performance using accuracy scores and confusion matrices.

## Dataset
- **File:** `water_potability(2).csv` (rename to `water_potability.csv` if you want to use the filename in the source code unchanged)
- **Target column:** `Potability`
- **Features:** All other columns in the dataset are used as input features.

The source code fills missing numeric values with column means before preparing the features and target.

## Models Compared
The supplied accuracy comparison chart shows the following approximate results:

| Model | Approximate Accuracy |
|---|---:|
| Logistic Regression | 52% |
| Gaussian Naive Bayes | 55% |
| K-Nearest Neighbors (KNN) | 64% |
| Random Forest | 70% |

**Best result in the chart:** Random Forest, at approximately 70% accuracy.

These values are estimated visually from the supplied bar chart and may differ slightly from the exact values printed by the Python program.

## Workflow
1. Load the dataset using Pandas.
2. Fill missing numeric values with the mean of each numeric column.
3. Separate the features from the `Potability` target column.
4. Convert the feature and target data to NumPy arrays.
5. Apply SMOTE to address class imbalance.
6. Standardize the features using `StandardScaler`.
7. Split the data into training and testing sets, using a 70/30 split and `random_state=42`.
8. Train the four classification models.
9. Generate predictions and calculate accuracy and confusion matrices.
10. Compare the model accuracies with a bar chart.

## Technologies and Libraries
- Python
- Pandas
- NumPy
- Matplotlib
- Seaborn
- scikit-learn
- imbalanced-learn (SMOTE)

## Installation

Create and activate a virtual environment if desired.

**Linux/macOS**
```bash
python3 -m venv .venv
source .venv/bin/activate
```

**Windows**
```bash
python -m venv .venv
.venv\\Scripts\\activate
```

Install dependencies:
```bash
pip install pandas numpy matplotlib seaborn scikit-learn imbalanced-learn
```

## How to Run
1. Place the CSV dataset and Python script in the same project directory.
2. Make sure the dataset filename matches the path used in the script (`water_potability.csv`).
3. Run the script:
   ```bash
   python projectwaterquality.py
   ```
4. Check the terminal output for each model's confusion matrix and accuracy score.
5. View the generated model accuracy comparison chart.

## Results and Interpretation
The supplied chart indicates that Random Forest performs best among the four tested models, followed by KNN, Gaussian Naive Bayes, and Logistic Regression. The chart reports accuracy only; a full evaluation should also consider the confusion matrices and other classification metrics, particularly precision, recall, and F1-score.

## Project Files
Suggested repository structure:
```text
comparativemachine learning approach for water quality check/
├── .venv/
├── comparativemachine learning approach for water quality check/
│   ├── accuracy score graphical comparison.png
│   ├── output.pdf
│   ├── source code.pdf
│   └── water_potability.csv
└── README.md
```

Update the filenames in this structure to match the files you upload to GitHub.

## Author
**Ramkrishna Majumder**
