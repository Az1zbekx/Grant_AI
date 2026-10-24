# 🎓 Grant AI: Academic Scholarship Eligibility & Allocation Predictor

[![CI](https://github.com/Az1zbekx/Grant_AI/actions/workflows/ci.yml/badge.svg)](https://github.com/Az1zbekx/Grant_AI/actions/workflows/ci.yml) [![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)](https://opensource.org/licenses/MIT)

[![Python](https://img.shields.io/badge/Python-3.10+-blue.svg?logo=python&logoColor=white)](https://python.org)
[![Streamlit](https://img.shields.io/badge/Streamlit-UI-FF4B4B.svg?logo=streamlit&logoColor=white)](https://streamlit.io)
[![Scikit-Learn](https://img.shields.io/badge/Scikit--Learn-Random%20Forest-F7931E.svg?logo=scikitlearn&logoColor=white)](https://scikit-learn.org)
[![License: MIT](https://img.shields.io/badge/License-MIT-green.svg)](LICENSE)

> An end-to-end Machine Learning web application designed to evaluate student profiles, predict scholarship grant eligibility, and estimate grant percentage allocation based on academic performance and socioeconomic indicators.

---

## 🌟 Key Features & Pipeline Architecture

```
                       +-------------------------------+
                       | Student Profile Input (UI)    |
                       +---------------+---------------+
                                       |
                                       v
                       +-------------------------------+
                       | Feature Engineering & Scaling |
                       +---------------+---------------+
                                       |
                   +-------------------+-------------------+
                   |                                       |
                   v                                       v
  +--------------------------------+      +--------------------------------+
  | Stage 1: Classifier            |      | Stage 2: Regressor             |
  | (RandomForestClassifier)       |      | (RandomForestRegressor)        |
  | Target: Grant Eligibility      |      | Target: Allocation Percentage  |
  +--------------------------------+      +--------------------------------+
                   |                                       |
                   +-------------------+-------------------+
                                       |
                                       v
                       +-------------------------------+
                       | Interactive Dashboard Output  |
                       +-------------------------------+
```

- **Dual-Model Architecture:**
  1. **Eligibility Classifier:** Evaluates academic criteria to classify whether an applicant qualifies for scholarship funding.
  2. **Grant Allocation Regressor:** Quantifies the exact funding tier and percentage allocation (e.g., 25%, 50%, 75%, 100%).
- **Interactive Web Interface:** Built with **Streamlit** for real-time inference, intuitive slider inputs, and dynamic results visualization.
- **Robust Preprocessing Pipeline:** Validates and normalizes feature distributions across study habits, attendance, and exam scores.

---

## 📊 Input Feature Schema

| Category | Features | Description |
| :--- | :--- | :--- |
| **Academic Metrics** | `Hours Studied`, `Attendance`, `Previous Scores`, `Exam Score` | Core indicators of scholastic dedication and consistency. |
| **Extracurricular & Well-being** | `Tutoring Sessions`, `Physical Activity`, `Sleep Hours` | Behavioral and physical wellness attributes affecting cognition. |
| **Socioeconomic Indicators** | `Family Income`, `Parental Education`, `Extracurriculars` | Contextual socioeconomic factors for equitable scholarship distribution. |

---

## 📂 Project Structure

```
Grant_AI/
├── Data/
│   ├── StudentPerformanceFactors.csv   # Raw training dataset
│   └── dataset.csv                     # Processed feature store
├── Models/
│   ├── classifier.pkl                  # Serialized Random Forest Classifier
│   └── regressor.pkl                   # Serialized Random Forest Regressor
├── Notebooks/
│   ├── preprocessing.ipynb             # Exploratory Data Analysis & feature scaling
│   └── grant-ai-model.ipynb            # Model training, hyperparameter tuning & evaluation
├── Utils/
│   ├── __init__.py
│   └── preprocess.py                   # Reusable inference preprocessing module
├── app.py                              # Streamlit interactive application
├── requirements.txt                    # Project dependencies
└── README.md                           # Documentation
```

---

## 🚀 Quickstart & Installation

### 1. Clone the Repository
```bash
git clone https://github.com/Az1zbekx/Grant_AI.git
cd Grant_AI
```

### 2. Set Up Virtual Environment
```bash
python3 -m venv venv
source venv/bin/activate
pip install -r requirements.txt
```

### 3. Launch the Application
```bash
streamlit run app.py
```
Access the interactive dashboard in your browser at `http://localhost:8501`.

---

## 🛠️ Tech Stack

- **Core Runtime:** Python 3.10+
- **Machine Learning:** Scikit-Learn (Random Forest, Preprocessing, Metrics)
- **Data Manipulation:** Pandas, NumPy
- **Serving & UI:** Streamlit, Joblib

---

## 👤 Author

- **Developer:** [Azizbek (Az1zbekx)](https://github.com/Az1zbekx)
- **Focus:** Practical Machine Learning & Applied AI Systems
