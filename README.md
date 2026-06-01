# Social Media Engagement Prediction Using NLP
NLP-based prediction of social media engagement using Trump tweets dataset and SHAP analysis. This project is developed as part of the Computational Intelligence Methods course.

## Project Goal

The main goal of this project is to predict social media engagement based on tweet content using Natural Language Processing (NLP) and machine learning techniques.

The project focuses on analyzing tweet text and identifying factors that influence user engagement, measured primarily by retweet counts.

Additionally, the project includes explainability analysis using SHAP to better understand the impact of different textual features on model predictions.

## Dataset

This project uses the **Trump Tweets dataset** available on Kaggle:

https://www.kaggle.com/datasets/austinreese/trump-tweets

The dataset contains tweets published by Donald Trump along with metadata such as retweet counts, favorites, timestamps, and tweet sources.

### Download instructions
- Go to the Kaggle dataset page
- Download the dataset as a .zip file
- Extract the files locally

### Required file structure

After extraction, place the dataset files into the following directory:

````
data/
└── raw/
    ├── realdonaldtrump.csv
    └── trumptweets.csv
````

### Note

The raw dataset is not included in this repository due to file size constraints and reproducibility best practices.
Each user is required to download the dataset independently from Kaggle.

### Reproducibility

To reproduce the results, ensure that the dataset is placed in the correct directory before running the notebooks.

## Technologies and Tools

- Pandas
- NumPy
- Scikit-learn
- XGBoost / LightGBM
- SHAP
- Matplotlib
- Jupyter Notebook

## Setup

```bash
uv venv
source .venv/bin/activate
uv pip install -r requirements.txt
```


## Jupyter / PyCharm Configuration

If notebook imports (e.g. pandas) do not work, ensure that:

- the correct .venv interpreter is selected in PyCharm,


## Authors

- Alicja Borek
- Dobrawa Rumszewicz
- Patryk Kowalczyk
