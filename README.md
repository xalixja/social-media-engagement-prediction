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



# Konfiguracja Środowiska LaTeX (VSCODE | LINUX)

Krótki przewodnik jak przygotować system Linux oraz Visual Studio Code do pracy z dokumentem.

---

## 1. Instalacja kompilatora (Linux)

Do kompilacji dokumentów wymagana jest dystrybucja **TeX Live**:

```bash
sudo apt update
sudo apt install texlive-full
sudo apt install python3-pygments
```

## 2. Wtyczka do Visual Studio Code

Do wygodnego pisania i automatycznego podglądu dokumentu używamy oficjalnego standardu:

1. Otwórz VS Code.
2. Wejdź w zakładkę rozszerzeń (skrót: `Ctrl + Shift + X`).
3. Wyszukaj i zainstaluj wtyczkę: **LaTeX Workshop** (autor: *James Yu*).

## 3. Setup minted używającego Pygments napisanego w Pythonie

Domyślnie LaTeX ze względów bezpieczeństwa ma zablokowaną możliwość uruchamiania jakichkolwiek programów z poziomu systemu operacyjnego. Musimy mu na to jawnie pozwolić, przekazując flagę -shell-escape. Trzeba dodać tę flagę do ustawień edytora:

1. Wciśnij skrót Ctrl + Shift + P, aby otworzyć paletę komend.

2. Wpisz: Preferences: Open User Settings (JSON)

3. Dodać:
```JSON
"latex-workshop.latex.tools": [
    {
        "name": "latexmk",
        "command": "latexmk",
        "args": [
            "-synctex=1",
            "-interaction=nonstopmode",
            "-file-line-error",
            "-pdf",
            "-outdir=%OUTDIR%",
            "-shell-escape",
            "%DOC%"
        ]
    },
    {
        "name": "pdflatex",
        "command": "pdflatex",
        "args": [
            "-synctex=1",
            "-interaction=nonstopmode",
            "-file-line-error",
            "-shell-escape",
            "%DOC%"
        ]
    }
],
```

---

## 3. Jak pracować z projektem?

* **Kompilacja:** Wtyczka kompiluje dokument automatycznie do formatu PDF przy każdym zapisaniu pliku (`Ctrl + S`).
* **Podgląd PDF:** Aby otworzyć podgląd na żywo obok kodu, użyj skrótu `Ctrl + Alt + V` lub kliknij ikonę z zakładką/lupą w prawym górnym rogu ekranu.
* **Nawigacja:** Kliknięcie z wciśniętym klawiszem `Ctrl` na tekst w podglądzie PDF przeniesie Cię do odpowiedniej linijki w kodzie `.tex` (i odwrotnie).


## Authors

- Alicja Borek
- Dobrawa Rumszewicz
- Patryk Kowalczyk
