# 💧 Pump It Up — Water Pump Status Prediction

## 📌 Overview
This project addresses the **Pump It Up: Data Mining the Water Table** challenge, which focuses on predicting the operational status of water pumps in Tanzania using structured and geospatial data.

The solution leverages **Python-based data analysis and machine learning**, developed primarily through **Jupyter Notebooks**, to build, evaluate, and compare predictive models.

---

## 🏆 Competition Context
Access the competition details here:  
https://www.drivendata.org/competitions/7/pump-it-up-data-mining-the-water-table/

### Profile used to participate
https://www.drivendata.org/users/ivanrnarvaez/

### Objective
Predict the functional status of water pumps:
- `functional`
- `functional needs repair`
- `non functional`

Accurate predictions help improve **water access planning and maintenance prioritization**.

---

## 🎯 Project Goals
- Perform thorough **exploratory data analysis (EDA)**
- Engineer meaningful features from categorical, numerical, and geospatial data
- Train and evaluate multiple classification models
- Optimize model performance using appropriate metrics
- Generate predictions suitable for competition submission

---

## 📊 Dataset
The dataset is provided by the competition organizers and includes:

### Features
- Pump characteristics (type, installation year, management)
- Water source and quality
- Geographic data (region, district, latitude, longitude)
- Operational and administrative attributes

### Target Variable
- `status_group`

---

## 🔍 Methodology

### 1️⃣ Exploratory Data Analysis (EDA)
Performed using **Jupyter Notebooks**:
- Variable typology
- Distribution analysis of categorical and numerical variables, identify outliers
- Missing value assessment
- Class imbalance analysis
- Geospatial distribution of pump statuses

---

### 2️⃣ Data Preprocessing
- Missing value imputation: Mode and median
- Categorical encoding 
- Removal of low-information or redundant features

---

### 3️⃣ Feature Engineering
- Grouped categorical features (for unique categorical variables greater than 14 values -> codified as others)
- Age-related features (based on installation year)
- Geographical feature operations to extract/validate information

---

### 4️⃣ Model Training
Models evaluated include:
- RandomForestClassifier
- GaussianNB

- Model selection is based on cross-validation performance.
- Parameter selection based in GridSearchCV

---

## 📐 Model Evaluation
Evaluation metric used by the competition:
- **Classification Accuracy**

Additional diagnostics:
- Confusion matrix
[[7268  121  541]
 [ 585  283  144]
 [1284   70 4274]]
  
- Use of ROC AUC curve to evaluate results
  - Precision, recall, and F1-score per class

---

## 🧠 Tech Stack

### Data Science
- Python
- Pandas, NumPy
- Scikit-learn

### Visualization
- Matplotlib
- Seaborn

### Notebooks
- Jupyter Notebook

---

## 📁 Project Structure
```text
Tarea/
├── .DS_Store
├── .git/
├── .gitignore
├── .venv/
├── .vscode/
├── .reports/
├── .results/
├── env_setup/
│   └── environment.yml
├── PumpitUp.ipynb
├── README.md
├── SubmissionFormat.csv
├── Test.csv
├── X_test.csv
├── confusion_matrix.png
├── training_labels.csv
└── training_values.csv
```

---
## 🚀 How to Run the Project
### 1️⃣ Install dependencies
pip install -r env_setup/environment.yml

### 2️⃣ Run notebooks

Launch Jupyter:
```bash
jupyter notebook
```

Execute cells in PumpitUP notebook.

### 3️⃣ Generate submission

The final notebook produces a submission.csv file in the required competition format:

id,status_group
50785,non functional
51630,functional
17168,functional
45559,non functional
49871,functional

---

## 📈 Results

Best-performing model: RandomForestClassifier with the parameters:
- max_depth=20
- n_estimators=100

- Results:
  - Accuracy: 0.8115991763898421
  - Precision: 0.8073229631184476
  - Recall: 0.8115991763898421
  - F1 Score: 0.8018897597351886
Best-performing model: {Model Name}


### Key drivers of pump functionality:

- longitude
- quantity_dry
- latitude
- quantity_group_dry
- construction_year


---
## ⚠️ Limitations

- Missing or inconsistent geographic data
- Temporal or historical data was not captured


---
## 🔮 Future Improvements

- Incorporate advanced geographical analysis techniques
- Add spatial clustering or region-based models
- Integrate external geospatial or socio-economic data - Not possible in the context of the challenge.

---
## 📌 Project Status

✅ Completed - Competition results submited with results in the top 30% of submissions

---
## 👤 Author

Ivan R. Narvaez
> Software Engineer-AI | Data Scientist | Analytics & Digital Transformation

