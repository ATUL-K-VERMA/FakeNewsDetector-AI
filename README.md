# 📰 FakeNewsDetector-AI

# 📖 Overview

**FakeNewsDetector-AI** is an AI-powered Fake News Detection System that classifies news articles as **Real** or **Fake** using Natural Language Processing (NLP) and Machine Learning techniques.

The application processes textual news content through preprocessing, TF-IDF feature extraction, and multiple machine learning classifiers to accurately predict the authenticity of news articles. A user-friendly Flask web interface enables users to input news content and receive instant predictions.

---

# ✨ Features

* 📰 Detects Fake and Real News
* 🤖 Machine Learning-Based Classification
* 🧠 Natural Language Processing (NLP)
* 📄 TF-IDF Feature Extraction
* 🌐 Interactive Flask Web Interface
* ⚡ Real-Time Predictions
* 📊 Model Performance Evaluation
* 🔍 Multiple Machine Learning Algorithms
* 💾 Trained Model Serialization using Pickle

---

# 📸 Application Preview

### Home Page

* News Article Input
* Detect Fake News Button

### Prediction Page

* Prediction Result
* Real/Fake Classification
* Model Confidence (if available)

> Add screenshots inside the `screenshots/` folder for a professional GitHub repository.

---

# 🏗️ Project Architecture

```text
User Input
      │
      ▼
Flask Web Interface
      │
      ▼
Text Preprocessing
      │
      ▼
TF-IDF Vectorization
      │
      ▼
Machine Learning Model
      │
      ▼
Prediction
      │
      ▼
Real News / Fake News
```

---

# 🧠 Machine Learning Workflow

```text
News Dataset
      │
      ▼
Data Cleaning
      │
      ▼
Text Preprocessing
      │
      ▼
Tokenization
      │
      ▼
TF-IDF Vectorization
      │
      ▼
Model Training
      │
      ▼
Prediction
```

---

# 🛠️ Technologies Used

| Category             | Technology          |
| -------------------- | ------------------- |
| Programming Language | Python              |
| Web Framework        | Flask               |
| Machine Learning     | Scikit-learn        |
| NLP                  | NLTK                |
| Data Processing      | Pandas              |
| Numerical Computing  | NumPy               |
| Visualization        | Matplotlib, Seaborn |
| Model Storage        | Pickle              |

---

# 🤖 Machine Learning Models

The project evaluates several machine learning algorithms before selecting the best-performing model.

* Logistic Regression
* Naive Bayes
* Support Vector Machine (SVM)
* Stochastic Gradient Descent (SGD)
* Random Forest

The final trained model is serialized using **Pickle** for deployment.

---

# 📂 Project Structure

```text
FakeNewsDetector-AI/
│
├── app.py
├── classifier.py
├── prediction.py
├── DataPrep.py
├── FeatureSelection.py
├── final-fnd.ipynb
├── model.pkl
├── final_model.sav
├── train.csv
├── test.csv
├── valid.csv
├── templates/
├── static/
├── screenshots/
├── requirements.txt
├── README.md
└── .gitignore
```

---

# 📊 Dataset

The model is trained on a labeled news dataset containing:

* News Statement
* Label (Real/Fake)

The dataset is divided into:

* Training Dataset
* Validation Dataset
* Testing Dataset

---

# ⚙️ Installation

## Clone Repository

```bash
git clone https://github.com/your-username/FakeNewsDetector-AI.git
```

---

## Navigate to Project

```bash
cd FakeNewsDetector-AI
```

---

## Install Dependencies

```bash
pip install -r requirements.txt
```

---

## Download Required NLTK Resources

```python
import nltk

nltk.download('punkt')
nltk.download('stopwords')
nltk.download('wordnet')
```

---

## Run Application

```bash
python app.py
```

Open your browser:

```
http://127.0.0.1:5000
```

---

# 🚀 How It Works

1. User enters a news article.
2. Text is cleaned and preprocessed.
3. TF-IDF converts text into numerical features.
4. The trained machine learning model predicts the result.
5. Flask displays whether the news is **Real** or **Fake**.

---

# 📈 Model Evaluation

The project evaluates different models using:

* Accuracy
* Precision
* Recall
* F1-Score
* Confusion Matrix
* K-Fold Cross Validation
* Grid Search Hyperparameter Tuning

---

# 📦 Dependencies

* Python
* Flask
* Scikit-learn
* Pandas
* NumPy
* NLTK
* Matplotlib
* Seaborn
* Pickle

Install all dependencies:

```bash
pip install -r requirements.txt
```

---

# 🌟 Future Enhancements

* Deep Learning Models (LSTM/BERT)
* Transformer-Based Fake News Detection
* News Source Verification
* Explainable AI Predictions
* REST API Support
* Docker Deployment
* Cloud Deployment (AWS/Azure/GCP)
* Multilingual Fake News Detection
* User Authentication
* Real-Time News Verification

---

# 🤝 Contributing

Contributions are welcome!

1. Fork this repository.
2. Create a feature branch.
3. Commit your changes.
4. Push your branch.
5. Open a Pull Request.

---

# 📄 License

This project is licensed under the MIT License.

---

# 👨‍💻 Author

**Atul Kumar**

Bachelor of Technology (Computer Science & Engineering)

* GitHub: github.com/ATUL-K-VERMA
* LinkedIn: linkedin.com/in/atul-kumar

---

# 🙏 Acknowledgements

* Flask
* Scikit-learn
* NLTK
* Pandas
* NumPy
* Matplotlib
* Seaborn
* Python Community

---

# ⭐ Support

If you found this project helpful, please consider giving it a **⭐ Star** on GitHub.

It helps others discover the project and motivates further development.

**Happy Coding! 🚀**
