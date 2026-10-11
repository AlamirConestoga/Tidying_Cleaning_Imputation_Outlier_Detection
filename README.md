# Lab 2 - Tidying, Cleaning, Imputation, and Outlier Detection
---

## Project Summary

This project takes a large, messy, **wide-format** survey file (`messy_survey_wide_50k.csv`: 50,000 respondents × 50 columns) and reshapes it into **tidy, long-format tables** using `pandas.melt()`. It then visualizes the tidy data to check whether province is related to weekly spending.


## Setup Instructions

### 1. Clone and enter the repo

```bash
git clone https://github.com/<your-username>/Tidying_Cleaning_Imputation_Outlier_Detection.git
cd Tidying_Cleaning_Imputation_Outlier_Detection_Lab#2

### 2. Create a virtual environment
python -m venv .venv

# Windows
.venv\Scripts\activate

# macOS / Linux
source .venv/bin/activate

### 3. Install dependencies
pip install -r requirements.txt


### 4. Run the notebook
Open week5Lab_Students.ipynb in VS Code or Jupyter, select the .venv kernel, and Run cell by cell.

The notebook will:


Load messy data (messy_survey_wide_50k.csv).
