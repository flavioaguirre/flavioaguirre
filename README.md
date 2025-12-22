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
  <a href="https://drive.google.com/file/d/1kDF-ZMmboAALJVwvI8CN9-DqiTpg5Nro/view?usp=sharing" target="_blank">
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

<br>

---

## Highlights
- Professional certifications with verifiable badges on [Credly](https://www.credly.com/users/flavio-aguirre.84c58337).
- Portfolio aligned with real-world DS/ML tasks (churn, weather classification, SQL EDA).
- Comfortable across DS stack: Python, SQL, scikit-learn, Django, MLOps, PyTorch/TensorFlow (foundations)
<br>

---

## Skills

- **Languages:** Python, SQL, JavaScript  
- **Web Backend & APIs:** Django, FastAPI, RESTful APIs  
- **Web Frontend (Foundations):** HTML, CSS, SASS  
- **Data Science & Machine Learning:** Pandas, NumPy, scikit-learn, statsmodels  
- **Deep Learning:** PyTorch, TensorFlow / Keras, Transfer Learning  
- **Natural Language Processing:** Hugging Face Transformers, spaCy  
- **MLOps & Deployment:** Docker, DVC, GitHub Actions (CI/CD)  
- **Data Visualization:** Matplotlib, Seaborn, Plotly  
- **Databases:** PostgreSQL, MySQL, SQLite, MongoDB  
- **Cloud & Developer Tools:** Azure, Google Cloud Platform (GCP), Hugging Face Spaces, Git, VS Code, Jupyter Notebooks, Anaconda / Miniconda, Excel  
- **Apps & Demos:** Streamlit, Dash  
- **Soft Skills:** Clear communication, fast learner, documentation-first mindset

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

### 1) Hielo Rosario — Enterprise-grade Django e-commerce platform (MVP)

**Goal:** Deliver a production-ready Minimum Viable Product (MVP) for Hielo Rosario — an industrial ice producer in Rosario, Argentina — to manage catalog, orders, and fulfillment with minimal operational overhead.

**Result:** End-to-end, deployable Django application providing a professional commerce flow: product catalog with volume pricing, a user-friendly checkout (delivery method selection, validation, and order reference tracking), and a tailored admin interface to manage orders and customers. The project is containerized with Docker, prepared for cloud deployment (Azure-ready IaC stubs and CI guidance), and published as a portfolio piece with documentation and a demo video.

**What I did:**

- Designed the overall architecture and domain model for products, price tiers, carts, and orders to support B2B and B2C workflows.
- Implemented a polished, accessible UI with server-rendered Django templates for:
  - Product browsing and detail pages,
  - Cart management and quantity-based pricing,
  - Checkout flow with delivery method selection, terms acceptance, and a blocking message when preconditions fail.
- Built the checkout success flow with unique order reference generation and clear customer messaging for follow-up.
- Hardened operational UX with an enhanced **Django admin**:
  - Custom admin views and actions to let non-technical staff manage products, update order status, and reduce human error in order processing.
- Containerized the app with Docker and Docker Compose for reproducible local development and simplified deployment.
- Added infrastructure placeholders and documentation (infra/ with Terraform/Bicep stubs) to ease future provisioning on Azure.
- Improved developer experience: `.env.example` with CI/Azure placeholders, test suite, pre-commit, and CI-friendly commands.
- Produced professional documentation (README), a demo video, and a clear licensing notice for public portfolio use.

**Next steps:**

- Harden production deployment (Azure App Service / Container Apps) including secret management, autoscaling, and monitoring.
- Add optional integrations: payment gateway, delivery scheduling, and reporting dashboards for operations.
- Expand admin analytics and automated notifications to further reduce manual workload.

<!-- Pinned card -->
<p align="center">
  <a href="https://github.com/flavioaguirre/hielo-rosario">
    <img src="https://github-readme-stats.anuraghazra1.vercel.app/api/pin/?username=flavioaguirre&repo=hielo-rosario&theme=tokyonight" alt="hielo-rosario"/>
  </a>
</p>

### 2) ByeBye Predictor — Hybrid Telco Churn Prediction (Top Project)

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


<p align="center">
  <a href="https://github.com/flavioaguirre/byebye-predictor">
    <img src="https://github-readme-stats.anuraghazra1.vercel.app/api/pin/?username=flavioaguirre&repo=byebye-predictor&theme=tokyonight" alt="byebye-predictor"/>
  </a>
</p>

<br>

### 3) Precipi-Check — Will It Rain Tomorrow? (Top Project)

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
- Email: flavio.aguirre.dev@gmail.com
- <a href="https://www.linkedin.com/in/flavio-aguirre-12784a252/" target="_blank">LinkedIn</a> 
- <a href="https://drive.google.com/file/d/1kDF-ZMmboAALJVwvI8CN9-DqiTpg5Nro/view?usp=sharing" target="_blank">My CV</a>

<br>
