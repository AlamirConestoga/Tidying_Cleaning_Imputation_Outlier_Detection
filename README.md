# Lab 2 – Tidying, Cleaning, Imputation, and Outlier Detection

**Course:** PROG8245 – Machine Learning Programming  
**Assignment:** Lab 2 (Group Project)

## Project Overview

This project demonstrates data preprocessing using four datasets. We apply data tidying, reshaping, missing-value analysis, imputation, visualization, and outlier detection. The work is documented in a Jupyter notebook so that the steps and results can be reproduced.

## Notebook Sections

### 1. Survey Data Tidying (PEW Section)

We used the `messy_survey_wide_50k.csv` dataset to explore data tidying techniques.

- Examined the dataset structure and missing values.
- Standardized province names to maintain consistency.
- Identified weekly spending columns (`wk1`–`wk26`).
- Used `melt()` to transform the data from wide format to long format.
- Visualized weekly spending patterns and provincial distributions.

### 2. Billboard Data Tidying

We used the `billboard.csv` dataset to explore data cleaning and transformation.

- Examined the dataset structure and column names.
- Standardized column names.
- Identified missing values in ranking information.
- Cleaned numerical ranking fields.
- Practised reshaping and aggregating song-chart data.

### 3. Cars Data Cleaning

We used the `auto-mpg.data` dataset to practise handling missing values.

- Identified missing values in the `Horsepower` column.
- Compared dropping rows and columns with imputation techniques.
- Applied mean, median, and mode imputation.
- Used Scikit-Learn's `SimpleImputer`.
- Compared dataset statistics before and after cleaning.
- Exported the cleaned dataset to `data/cars_cleaned.csv`.

### 4. Diabetes Outlier Detection

We used the `diabetes_prediction_dataset.csv` dataset to identify and analyze outliers.

- Explored numerical features including age, BMI, HbA1c level, and blood glucose level.
- Created box plots and scatter plots to visualize potential outliers.
- Applied Z-Score and Interquartile Range (IQR) methods.
- Compared the number of outliers identified by each method.
- Analyzed how filtering outliers affected descriptive statistics.

## Project Structure

The project contains the following files and folders:

- `week5Lab_Students.ipynb` – Main Jupyter notebook
- `README.md` – Project documentation
- `requirements.txt` – Python dependencies and versions
- `.gitignore` – Files and folders excluded from Git
- `data/` – Source datasets and generated output files

The `data/` folder contains:

- `messy_survey_wide_50k.csv`
- `billboard.csv`
- `auto-mpg.data`
- `diabetes_prediction_dataset.csv`
- `cars_cleaned.csv` (generated output)

## Technologies Used

The following tools and libraries were used:

- **Python:** Programming language for data preprocessing
- **Jupyter Notebook:** Interactive coding and documentation
- **Pandas:** Data loading, cleaning, and transformation
- **NumPy:** Numerical calculations
- **Matplotlib:** Data visualization
- **Seaborn:** Statistical visualization
- **Scikit-Learn:** Missing-value imputation
- **Git and GitHub:** Version control and group collaboration
- **Visual Studio Code:** Development environment

The required Python packages and their versions are listed in `requirements.txt`.

## How to Run the Project

### Step 1 – Clone the Repository

Clone the GitHub repository and open the project folder in Visual Studio Code.

### Step 2 – Create a Virtual Environment

Run the following command in the terminal:

`python -m venv .venv`

Activate the virtual environment in Windows PowerShell:

`.\.venv\Scripts\activate`

### Step 3 – Install Dependencies

Install the required Python libraries using:

`python -m pip install -r requirements.txt`

### Step 4 – Verify Dataset Files

Ensure that the required datasets are available inside the `data/` folder.

### Step 5 – Execute the Notebook

Open `week5Lab_Students.ipynb` in Visual Studio Code.

Select the Python virtual environment as the Jupyter kernel.

Run all cells from beginning to end and examine the results, graphs, and observations.

## Key Findings

### Cars Dataset

We identified six missing values in the `Horsepower` column.

We compared different missing-value handling techniques, including dropping records and replacing missing values using mean, median, and mode.

Median imputation was considered suitable because the Horsepower distribution was right-skewed and higher values could influence the mean.

### Diabetes Dataset

The Diabetes Prediction Dataset contained 100,000 records.

Using the Z-Score method with a threshold of `|z| > 3`, we identified **1,294 potential BMI outliers**.

Using the IQR method, we identified **7,086 potential BMI outliers**.

After filtering the IQR-flagged observations in a separate DataFrame, the number of records decreased from 100,000 to 92,914.

The analysis showed that extreme values can affect the mean and standard deviation, while the median is generally less sensitive.

We also observed that unusual medical measurements are not necessarily errors and should be investigated before removal.

## Reproducibility and Testing

Our group used a shared GitHub repository to collaborate on this assignment.

One team member created the repository, and other team members cloned it onto their computers.

We used `requirements.txt` to install the required Python libraries and executed our assigned notebook sections.

This process helped us verify that the project files and dependencies could be shared and used across different development environments.

The Jupyter notebook includes a separate Replicability Check section documenting the testing process and results.

## Conclusion

This assignment helped us improve our understanding of data preprocessing techniques.

We gained practical experience in data tidying, handling missing values, imputation, data visualization, and outlier detection.

We also practised software engineering principles through Markdown documentation, dependency management, GitHub collaboration, and reproducibility testing.

These techniques are important for preparing reliable datasets before applying machine learning algorithms.