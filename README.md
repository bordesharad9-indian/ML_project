# Student Exam Performance Indicator

This is a small end-to-end machine learning project I built while learning how
ML models actually get deployed as a working app, not just a Jupyter notebook.

## What it does

You enter a student's details — gender, ethnicity, parental education, lunch
type, whether they did a test prep course, and their reading/writing scores —
and the app predicts what their maths score is likely to be. It's a regression
problem, and I used the classic "Students Performance in Exams" dataset for it.

## Why I built it

I wanted to understand the full pipeline of a real ML project, not just
`model.fit()` in a notebook — things like:
- structuring code into ingestion, transformation, and training components
- saving a preprocessor and model as `.pkl` files so they can be reused
- wrapping everything in a Flask app so a normal person could use it
  through a browser instead of running Python scripts

This is still a learning project, so the model and the code structure are
kept fairly simple on purpose. I'm sure there are better ways to do parts
of this — I'm figuring it out as I go.

## Tech stack

- **Python** — core language
- **scikit-learn** — preprocessing (encoding, scaling) and model training
  (tried a few regressors with GridSearchCV)
- **Pandas / NumPy** — data handling
- **Flask** — backend + serving the web page
- **HTML/CSS** — frontend form and result display

## Project structure
ML_project/
├── artifacts/              # saved model + preprocessor + train/test data
├── src/
│   ├── components/         # data ingestion, transformation, model training
│   ├── pipeline/            # predict_pipeline.py (loads model, runs prediction)
│   ├── exception.py         # custom exception handling
│   └── utils.py             # helper functions (save/load objects, etc.)
├── templates/
│   └── home.html            # the form + result page
├── app.py                   # Flask routes
└── requirements.txt


<img width="1873" height="993" alt="Screenshot 2026-07-17 170959" src="https://github.com/user-attachments/assets/7cc272bd-d68e-4a44-97da-737dd4ace242" />


