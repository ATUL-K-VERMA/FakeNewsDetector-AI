# 📰 Fake News Detection

![Python](https://img.shields.io/badge/Python-3.9+-blue.svg)
![scikit-learn](https://img.shields.io/badge/scikit--learn-1.3+-orange.svg)
![Flask](https://img.shields.io/badge/Flask-2.3+-green.svg)
![License](https://img.shields.io/badge/License-MIT-brightgreen.svg)

> **AI-powered fake news detection** using Natural Language Processing (NLP) and Machine Learning.  
> Paste any news article to verify its authenticity with confidence scoring.

---

## 🎯 Features

- **5 ML Classifiers**: Naive Bayes, Logistic Regression, Linear SVM, SGD, Random Forest
- **TF-IDF Features**: N-gram analysis (unigram to 4-gram) with sublinear TF scaling
- **Beautiful Web UI**: Modern glassmorphism design with real-time confidence meters
- **REST API**: JSON endpoints for programmatic access
- **CLI Tool**: Interactive command-line prediction interface
- **Automated Training**: One-command pipeline with model comparison and selection
- **Comprehensive Tests**: Unit tests for preprocessor, predictor, and API

---

## 🏗️ Architecture

```
fake-news-detection/
├── config/              # Configuration (hyperparameters, paths)
├── src/                 # Source code
│   ├── data/            # Data loading & preprocessing
│   ├── features/        # TF-IDF feature extraction
│   ├── models/          # Training & prediction
│   └── utils/           # Logging, plotting, helpers
├── app/                 # Flask web application
│   ├── templates/       # HTML templates
│   └── static/          # CSS, JS, images
├── scripts/             # CLI tools (train, predict)
├── tests/               # Unit & integration tests
├── models/              # Saved model artifacts
└── notebooks/           # Jupyter notebooks
```

---

## ⚡ Quick Start

### 1. Clone & Install

```bash
git clone https://github.com/yourusername/fake-news-detection.git
cd fake-news-detection
pip install -r requirements.txt
```

### 2. Train the Model

```bash
python scripts/train.py
```

This will:
- Load the LIAR dataset (train.csv, test.csv, valid.csv)
- Train 5 classifiers with TF-IDF features
- Compare models and select the best one
- Save the pipeline to `models/fake_news_pipeline.pkl`

**Train specific models:**
```bash
python scripts/train.py --models logistic_regression naive_bayes
```

**With cross-validation:**
```bash
python scripts/train.py --cv
```

### 3. Run the Web App

```bash
python app/main.py
```

Open **http://localhost:5000** in your browser.

### 4. CLI Prediction

```bash
python scripts/predict_cli.py
python scripts/predict_cli.py --text "Obama announces new healthcare policy"
```

---

## 🔌 API Usage

### Predict Endpoint

```bash
curl -X POST http://localhost:5000/api/predict \
  -H "Content-Type: application/json" \
  -d '{"text": "Scientists discover a new planet that could support human life"}'
```

**Response:**
```json
{
  "label": "REAL",
  "raw_label": "True",
  "confidence": 0.8234,
  "probabilities": [0.1766, 0.8234],
  "processing_time_ms": 12.5
}
```

### Health Check

```bash
curl http://localhost:5000/api/health
```

---

## 📊 Model Performance

| Model               | Accuracy | F1 Score | Precision | Recall |
|---------------------|----------|----------|-----------|--------|
| Logistic Regression | 0.62     | 0.62     | 0.61      | 0.62   |
| Naive Bayes         | 0.60     | 0.60     | 0.60      | 0.60   |
| Random Forest       | 0.58     | 0.57     | 0.58      | 0.58   |
| Linear SVM          | 0.61     | 0.60     | 0.61      | 0.61   |
| SGD Classifier      | 0.60     | 0.60     | 0.60      | 0.60   |

> **Note:** Performance metrics will update based on your training run. These are baseline results on the LIAR dataset.

---

## 📦 Dataset

**LIAR: A Benchmark Dataset for Fake News Detection**

- **Source**: William Yang Wang, ACL 2017
- **Size**: ~12,800 labeled political statements
- **Labels**: True / False (mapped from 6-class original)
- **Files**: `train.csv`, `test.csv`, `valid.csv`

---

## 🧪 Running Tests

```bash
# Run all tests
pytest tests/ -v

# Run with coverage report
pytest tests/ -v --cov=src --cov-report=html

# Run specific test file
pytest tests/test_preprocessor.py -v
```

---

## ⚙️ Configuration

All hyperparameters are in `config/config.yaml`:

```yaml
features:
  ngram_range: [1, 4]
  max_features: 50000
  use_idf: true

models:
  default: "logistic_regression"
  logistic_regression:
    C: 1.0
    max_iter: 1000
```

---

## 🛠️ Tech Stack

| Component        | Technology                           |
|------------------|--------------------------------------|
| **Language**     | Python 3.9+                          |
| **ML Framework** | scikit-learn                         |
| **NLP**          | NLTK, TF-IDF, N-grams               |
| **Web Server**   | Flask                                |
| **Frontend**     | HTML5, CSS3 (Glassmorphism), JS      |
| **Testing**      | pytest, pytest-cov                   |
| **Fonts**        | Inter (Google Fonts)                 |

---

## 📝 License

This project is licensed under the MIT License — see the [LICENSE](LICENSE) file.

---

## 👤 Author

**Atul K**  
Fake News Detection Project v2.0

---

*Built with ❤️ using Python, scikit-learn & Flask*
