# Data Ingestion and EDA Pipeline

This project provides a robust Jupyter Notebook for loading, cleaning, and performing preliminary Exploratory Data Analysis (EDA) on structured data files. It is designed to handle multiple file types flexibly while standardizing the initial data preparation steps.

## What It Does
1. **Dynamic Ingestion:** Automatically reads `.csv`, `.json`, and `.txt` files (using pandas' built-in delimiter sniffer for `.txt`).
2. **Column Normalization:** Converts all column headers to a standardized `snake_case` format for easier programmatic access.
3. **Configurable Cleaning:** Allows the user to toggle how missing values are handled (e.g., dropping them, or filling numerical values with the mean and categorical values with the mode).
4. **Automated EDA:** Generates a quick overview of the data, including previews, statistical summaries, and categorical distributions.
5. **Export:** Saves the cleaned and processed DataFrame to a new `cleaned_data.csv` file.

## Prerequisites
- Python 3.8+
- `pip` (Python package installer)

## Setup Instructions
1. Open your terminal and navigate to the project directory.
2. (Optional but recommended) Create and activate a virtual environment:
   ```bash
   python -m venv venv
   source venv/bin/activate  # On Windows, use: venv\Scripts\activate