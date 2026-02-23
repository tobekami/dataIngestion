# Data Ingestion and EDA Pipeline

This project provides a robust Jupyter Notebook for loading, cleaning, and performing preliminary Exploratory Data Analysis (EDA) on structured data files. It is designed to handle multiple file types flexibly while standardizing the initial data preparation steps.

## What It Does

1. **Dynamic Ingestion & Fetching:** Automatically downloads a sample dataset (the Titanic dataset) if no local file is present. It can read `.csv`, `.json`, and `.txt` files (using pandas' built-in delimiter sniffer for `.txt`).
2. **Column Normalization:** Converts all column headers to a standardized `snake_case` format for easier programmatic access.
3. **Configurable Cleaning:** Allows the user to toggle how missing values are handled (e.g., dropping them, or filling numerical values with the mean and categorical values with the mode).
4. **Automated EDA:** Generates a quick overview of the data, including previews, statistical summaries, and categorical distributions.
5. **Export:** Saves the cleaned and processed DataFrame to a new `cleaned_data.csv` file.

## Prerequisites

* Python 3.8+
* Conda (recommended) or `pip`

## Setup Instructions

1. Open your terminal and navigate to the project directory.
2. Create and activate a Conda environment (or use an existing one):
```bash
conda create --name data_pipeline python=3.9
conda activate data_pipeline

```


3. Install the required libraries (ensuring Jupyter is installed within the environment):
```bash
conda install jupyter
pip install -r requirements.txt

```



## How to Run

1. Start the Jupyter Notebook server:
```bash
jupyter notebook

```


2. Open `data_ingestion.ipynb` in your browser.
3. The notebook will automatically fetch the Titanic dataset in the first block. Set your preferred `MISSING_STRATEGY`, then run the cells sequentially to execute the pipeline.