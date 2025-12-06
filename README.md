<!-- Banner simple y limpio -->

<h1 align="center">Hi, I'm Flavio Aguirre</h1>

<p align="center">
  Data Scientist · Python Full‑Stack · Aspiring AI Engineer
</p>

<p align="center">
  Rosario, Santa Fe (AR) · 
  <a href="https://www.linkedin.com/in/flavio-aguirre-12784a252/" target="_blank">LinkedIn</a> · <a href="https://www.credly.com/users/flavio-aguirre.84c58337" target="_blank">Credly – Verified Certifications</a> 
</p>
<br>

<!-- Botón de CV -->
<p align="center">
  <a href="https://drive.google.com/file/d/15FmGoY0KxbXkpdf9oIgdcMbP8oVzyXyH/view?usp=sharing" target="_blank">
    <img src="https://img.shields.io/badge/View%20My%20CV-2F80ED?style=for-the-badge&logo=googledrive&logoColor=white" alt="View My CV">
  </a>
</p>

<br>

---

## Value Proposition
I build data solutions that are clear, reproducible and ready for lightweight production:
- From dataset to decision: EDA → features → model → evaluation → demo.
- Communication-first: concise READMEs, metrics that matter, and business framing.
- Engineering mindset: versioned artifacts, tests, simple CI, and deployment basics.

I am currently working as a freelancer, delivering a full e-commerce website with a shopping cart system for an ice factory based in Rosario, Santa Fe (Argentina).
<br>

---

## Highlights
- Professional certifications with verifiable badges on [Credly](https://www.credly.com/users/flavio-aguirre.84c58337).
- Portfolio aligned with real-world DS/ML tasks (churn, weather classification, SQL EDA).
- Comfortable across DS stack: Python, SQL, scikit-learn, PyTorch/TensorFlow (foundations), basic MLOps.
<br>

---

## Skills
- Languages: Python, SQL, JavaScript
- DS/ML: Pandas, NumPy, Scikit-learn, Statsmodels
- DL: PyTorch, TensorFlow/Keras, Transfer Learning
- NLP: Hugging Face Transformers, spaCy
- MLOps: Docker, FastAPI, DVC, GitHub Actions (CI/CD)
- Visualization: Matplotlib, Seaborn, Plotly
- Databases: PostgreSQL, SQLite, MySQL, MongoDB
- Cloud & Tools: Azzure, Hugging Face Spaces, VSCode, Git, Excel, Jupyter Notebooks, Anaconda, Miniconda
- App/Demos: Streamlit, Dash
- Soft: Clear communication, fast learning, documentation-first

You can also check out my verified skill stack [by clicking here](https://www.credly.com/users/flavio-aguirre.84c58337/skills).


<!-- Badges visuales sutiles -->
<p>
  <img alt="Python" src="https://img.shields.io/badge/Python-3776AB?style=flat&logo=python&logoColor=white"/>
  <img alt="SQL" src="https://img.shields.io/badge/SQL-025E8C?style=flat&logo=postgresql&logoColor=white"/>
  <img alt="scikit-learn" src="https://img.shields.io/badge/scikit--learn-F7931E?style=flat&logo=scikitlearn&logoColor=white"/>
  <img alt="PyTorch" src="https://img.shields.io/badge/PyTorch-EE4C2C?style=flat&logo=pytorch&logoColor=white"/>
  <img alt="TensorFlow" src="https://img.shields.io/badge/TensorFlow-FF6F00?style=flat&logo=tensorflow&logoColor=white"/>
  <img alt="Docker" src="https://img.shields.io/badge/Docker-2496ED?style=flat&logo=docker&logoColor=white"/>
  <img alt="FastAPI" src="https://img.shields.io/badge/FastAPI-009688?style=flat&logo=fastapi&logoColor=white"/>
  <img alt="GitHub Actions" src="https://img.shields.io/badge/GitHub%20Actions-2088FF?style=flat&logo=githubactions&logoColor=white"/>
</p>
<br>

---

## Featured Projects

### 1) ByeBye Predictor — Hybrid Telco Churn Prediction (Top Project)

**Goal:** Predict Telco customer churn by combining structured data (contracts, billing, services) with Spanish text-based churn-intent signals (Reddit comments).  
**Result:** End-to-end, production-style pipeline with a hybrid Logistic Regression model achieving approximately **F1 ≈ 0.83** and **Accuracy ≈ 0.82** on a held-out test set.

**What I did:**

- Designed a **clean, modular project structure** (`data/`, `notebooks/`, `src/`, `tests/`) with reusable utilities for:
  - Data loading and cleaning,
  - EDA and feature engineering,
  - Model training, cross-validation, and evaluation.
- Built a baseline **Telco churn model** using curated structured features:
  - Encoders, imputers, and scalers via `ColumnTransformer`,
  - Logistic Regression and tree-based models orchestrated through a custom `ModelBuilder`.
- Developed a **Spanish NLP pipeline** to detect churn intent in Reddit comments:
  - Custom `TextCleaner` (lowercasing, URLs/punctuation/digits removal, Spanish stopwords),
  - TF‑IDF with 1–2 grams + `TruncatedSVD` for dimensionality reduction,
  - Logistic Regression (`class_weight="balanced"`) to produce `nlp_churn_score` for each comment.
- Integrated text into a **hybrid churn model** by simulating realistic customer-level aggregates:
  - `nlp_churn_score_max_30d`,
  - `nlp_churn_score_mean_90d`,
  - `nlp_churn_high_risk_count_30d`.
- Evaluated baseline vs hybrid using a dedicated `ModelEvaluator`:
  - Metrics: Accuracy, Precision, Recall, F1,
  - Confusion matrices, ROC curves, Precision–Recall curves,
  - Visual F1 comparison between structured-only and hybrid feature spaces.
- Persisted final models with `joblib` and documented an **end-to-end scoring demo**:
  - Modify only text-based aggregates to simulate high-risk customers,
  - Show how churn probability reacts to new text-derived risk signals.

**Next steps:**

- Replace synthetic aggregates with **real** `nlp_churn_score` features joined via `customerID`.
- Explore additional models (XGBoost, LightGBM, calibrated classifiers) in `ModelBuilder`.
- Exposing the hybrid model and the text model behind an **API (FastAPI)** with monitoring and retraining strategy.

  <!-- Tarjetas fijadas -->
<p align="center">
  <a href="https://github.com/flavioaguirre/byebye-predictor">
    <img src="https://github-readme-stats.anuraghazra1.vercel.app/api/pin/?username=flavioaguirre&repo=byebye-predictor&theme=tokyonight" alt="byebye-predictor"/>
  </a>
</p>

<br>

### 2) Precipi-Check — Will It Rain Tomorrow? (Top Project)

**Goal:** Predict next-day precipitation using historical meteorological signals (temperature, humidity, wind, etc.).  
**Result:** Structured, reproducible pipeline comparing simple baselines against ML models, with a focus on interpretability and seasonal behavior.

**What I did:**

- Defined a **feature pipeline** from raw weather data to model-ready features:
  - Temporal features (lags, rolling windows, seasonal indicators),
  - Normalization/standardization and handling of missing values.
- Implemented and compared **baselines vs ML models**:
  - Naive benchmarks (e.g., “same as yesterday”),
  - Tree-based models / Logistic Regression for precipitation probability.
- Designed an **evaluation framework**:
  - Global metrics (Accuracy, F1, ROC–AUC),
  - Seasonal evaluation (performance by month/season),
  - Error analysis to understand failure modes.
- Explored **interpretability techniques**:
  - Feature importance,
  - Partial dependence plots, SHAP values.
- Planned from the outset for **deployment**:
  - Prediction API (FastAPI),
  - Automation-ready daily scoring.

**Next steps:**

- Strengthen seasonality analysis and long-term stability checks.
- Add formal explainability (SHAP / PDP) to the standard workflow.
- Publish an interactive demo (Gradio/Streamlit) supported by the API already built in this repo.


<!-- Tarjetas fijadas -->
  <p align="center">
  <a href="https://github.com/flavioaguirre/precipi-check">
    <img src="https://github-readme-stats.anuraghazra1.vercel.app/api/pin/?username=flavioaguirre&repo=precipi-check&theme=tokyonight" alt="precipi-check"/>
  </a>
</p>

<br>

---

## Engineering Signals
- Reproducibility: requirements.txt / pyproject, fixed seeds, data/model versioning (basic).
- Structure: notebooks/ vs src/ modules, scripts/, reports/figures.
- Quality: lint (ruff/black), minimal unit tests (pytest) for core functions.
- CI/CD: GitHub Actions for lint + tests on push/PR.
- Deploy: demo UIs (Streamlit/Gradio) and simple API (FastAPI) + Dockerfile.

If a project is interesting to you, I can quickly add a demo or API endpoint.

<br>

---

## Certifications
- <a href="https://www.coursera.org/account/accomplishments/professional-cert/GOFAVW3AD1AT" target="_blank">IBM Data Science Professional Certificate</a> — Verified on [Credly](https://www.credly.com/users/flavio-aguirre.84c58337).
- In progress: IBM AI Engineering Professional Certificate.

<br>

---

## Contact
- Location: Rosario, Santa Fe (AR)
- Email: flavioaguirre0@gmail.com
- <a href="https://www.linkedin.com/in/flavio-aguirre-12784a252/" target="_blank">LinkedIn</a> 
- <a href="https://drive.google.com/file/d/15FmGoY0KxbXkpdf9oIgdcMbP8oVzyXyH/view?usp=sharing" target="_blank">My CV</a>

<br>
