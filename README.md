# End-to-End Heart Disease Risk Analysis

## 📖 Project Overview

This project is a comprehensive analysis of a heart disease dataset, completed as a capstone for the **IBM Machine Learning Professional Certificate**. The primary goal is to perform a full data analysis workflow, including data cleaning, exploratory data analysis (EDA), and statistical hypothesis testing to identify key risk factors associated with heart disease.

A key finding of this analysis was the discovery that the dataset is likely synthetic, as commonly accepted clinical and lifestyle risk factors showed no statistically significant correlation with heart disease status.

---

## 📊 Dataset

The dataset used contains 21 variables and 10,000 observations related to patient health, including lifestyle habits (smoking, exercise), clinical measurements (blood pressure, cholesterol), and demographic information (age, gender).

* **Source:** [Link to the Kaggle Dataset You Used]
* **Target Variable:** `Heart Disease Status` (Binary: Yes/No)

---

## 📁 Project Structure

The project is organized into a modular structure to ensure clarity and reproducibility:

```
├── data/
│   ├── raw/            # Contains the original, untouched dataset
│   └── processed/      # Contains the cleaned and encoded dataset
├── notebooks/
│   ├── 01_data_cleaning.ipynb    # Notebook for all cleaning and preprocessing steps
│   └── 02_exploratory_analysis.ipynb # Main notebook for EDA and hypothesis testing
├── reports/
│   ├── figures/        # Stores all plots and visualizations generated
│   └── final_report.pdf # The final project report for a non-technical audience
├── src/                # (Optional) For reusable Python scripts
├── pyproject.toml      # Project dependencies and metadata
└── README.md           # This project overview
```

---

## ⚙️ Installation and Setup

To run this analysis, clone the repository and install the required dependencies in a virtual environment.

```bash
# Clone the repository
git clone [Your GitHub Repository URL]
cd heart-disease-analysis

# Create and activate a virtual environment
python -m venv .venv
source .venv/bin/activate  # On Windows, use: .\.venv\Scripts\activate

# Install dependencies
pip install .
```

---

## 🚀 Usage

1.  **Data Cleaning:** Run the `notebooks/01_data_cleaning.ipynb` notebook first to process the raw data and generate the cleaned dataset in the `data/processed/` directory.
2.  **Analysis:** Run the `notebooks/02_exploratory_analysis.ipynb` notebook to perform the full exploratory data analysis and significance testing.

---

## 🎯 Key Findings & Insights

The most significant finding of this project was the **consistent lack of correlation** between major risk factors and heart disease status.

* **EDA:** Visual analysis of `BMI`, `Sleep Hours`, `Stress Level`, `Blood Pressure`, `Cholesterol Level`, and even `Family Heart Disease` showed no clear difference or pattern between individuals with and without heart disease.
* **Hypothesis Testing:** A **Chi-Square Test of Independence** was performed to test the association between `Family Heart Disease` and `Heart Disease Status`. The test yielded a **p-value of 0.4133**, leading us to fail to reject the null hypothesis. This statistically confirms that there is no significant relationship between these variables in this dataset.

**Conclusion:** The data does not reflect real-world clinical patterns, suggesting it is synthetic or has been heavily modified.

---

## 🛠️ Technologies Used

* **Python 3.11+**
* **Pandas:** For data manipulation and cleaning.
* **NumPy:** For numerical operations.
* **Matplotlib & Seaborn:** For data visualization.
* **SciPy:** For statistical analysis and significance testing.