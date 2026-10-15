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

                    Billboard Data Set
Project Overview
This section explores Billboard chart records using Python and Pandas. The notebook demonstrates data inspection, data-quality checks, cleaning, feature engineering, exploratory data analysis, aggregation, and data reshaping with pivot() and melt().
The dataset used in this notebook contains 52,150 rows and 7 columns.
Dataset
Place the CSV file in the data/ directory. The notebook's expected file path is:
data/billboard.csv
The dataset fields are:
Field	Description
date	Date of the chart record
rank	Current chart position
song	Song title
artist	Credited artist
last_week	Previous week's chart position, when available
peak_rank	Highest chart position reached
weeks_on_board	Number of weeks on the chart, as represented in the source data


Missing values in last_week are retained because they may indicate that a song had no recorded position in the previous chart week.
Notebook Contents
The Section two of notebook covers:
1. Initial data inspection and exploratory data analysis
2. Data structure and field mapping
3. Data-quality checks for duplicates, missing key values, and ranking ranges
4. Cleaning and validation of text, date, and numeric fields
5. Feature engineering, including date-based features and rank_improvement
6. Histograms and descriptive statistics for chart ranks and rank changes
7. Demonstration of pivot() and melt() using a sample of song–artist pairs
8. Weekly aggregation of chart entries and ranking statistics
9. Dataset documentation and conclusions
Requirements
- Python 3.9 or newer recommended
- Jupyter Notebook or JupyterLab
- pandas
- numpy
- matplotlib
Install the required packages with:
pip install pandas numpy matplotlib jupyter
How to Run
1. Clone or download this repository.
2. Create a folder named data beside the notebook if it does not already exist.
3. Save the CSV as data/billboard.csv.
4. Install the requirements listed above.
5. Open the notebook in Jupyter Notebook, JupyterLab, or VS Code.
6. Run the notebook cells from top to bottom.
Example project structure:
Billboard_Lab2/
├── data/
│   └── billboard.csv
├── billboard_section2_new_dataset.ipynb
├── README.md
└── requirements.txt
If your CSV has a different filename, update the file path in the notebook's data-loading cell.
Key Notes
- The raw dataset is kept separate from the cleaned and feature-engineered DataFrames.
- Exact duplicate rows are checked before cleaning.
- Missing previous-week ranks are not automatically imputed.
- Unusual rank changes are explored rather than automatically removed, because large movements can be legitimate chart events.
- The source dataset is already in long format. The pivot() and melt() demonstration uses a sample to show how data can be transformed between long and wide formats without changing the main feature-engineered dataset.
