# AI-Powered-Student-Mental-Health-Prediction-Support-System
A full-stack web application that leverages machine learning to proactively identify students at risk of mental health challenges and connect them with tailored support resources. The system analyzes academic, behavioral, and optional self-reported data to provide early interventions.

https://img.shields.io/badge/Stack-React%2520%252B%2520Spring%2520Boot%2520%252B%2520Python-blue?style=for-the-badge
[https://img.shields.io/badge/ML-Transformer%2520%252B%2520XGBoost-orange?style=for-the-badge
](https://img.shields.io/badge/ML-Transformer_XGBoost-Orange?style=for-the-badge&logo=python&logoColor=white&color=orange)
https://img.shields.io/badge/Status-Proof%2520of%2520Concept-success?style=for-the-badge

## 🧠 Table of Contents
### Overview

Key Features

System Architecture

Tech Stack

Project Structure

Installation & Setup

Usage

ML Model Details

Ethical Considerations

Future Work

Contributing

License

### 📖 Overview
Student mental health is a critical issue in educational institutions. This project aims to create a proactive, data-driven support system that moves beyond traditional reactive methods. By using a multi-modal machine learning approach, the system identifies subtle signs of distress from various data points (academic, behavioral, textual) and facilitates early intervention through personalized resource recommendations and counselor alerts.

Disclaimer: This is a proof-of-concept. In a real-world deployment, the highest standards of ethics, privacy, and data security must be enforced. This system is designed as a support tool, not a replacement for professional human judgment and care.

### ✨ Key Features
#### 🔍 Multi-Modal Risk Analysis: Combines academic performance, engagement patterns, and sentiment analysis from optional surveys.

#### 🤖 High-Precision ML Ensemble: Utilizes a hybrid model (Transformer NLP + Anomaly Detection + XGBoost) for accurate, explainable predictions.

#### 📊 Interactive Dashboard: Provides students with insights into their own well-being trends and personalized self-help resources.

#### ⚠️ Counselor Alert System: Flags at-risk students for proactive, confidential check-ins by mental health professionals.

#### 🔐 Privacy by Design: All data is anonymized for model training. The system operates on an opt-in basis with transparent data policies.

### 🏗️ System Architecture
The system is built on a microservices-inspired architecture for clarity and separation of concerns.

### Diagram


<img width="600" height="600" alt="deepseek_mermaid_20250827_4dc514" src="https://github.com/user-attachments/assets/2a86b508-1303-49b2-b066-cb0a51529a94" />



🛠️ Tech Stack
Frontend
React (with Hooks, Context API)

Axios for API calls

Chart.js / D3.js for data visualizations

Material-UI / Chakra UI for component library

Backend
Spring Boot (REST API)

Spring Security with JWT Authentication

Spring Data JPA (ORM)

MySQL / PostgreSQL (Database)

Hibernate

Machine Learning & Data Pipeline
Python 3.8+

PyTorch / Transformers (for NLP model - BERT/DistilBERT)

Scikit-learn (for classic ML models & preprocessing)

XGBoost (for the meta-classifier)

TensorFlow/Keras (for potential LSTM networks)

Pandas / NumPy (for data manipulation)

FastAPI (to serve ML models as a REST API)

Joblib / Pickle (for model serialization)

DevOps & Tools
Docker (for containerization)

Git (version control)

Jupyter Notebook (for ML experimentation)

📁 Project Structure
text
├── frontend/                 # React application
│   ├── public/
│   ├── src/
│   │   ├── components/       # Reusable UI components
│   │   ├── contexts/         # Auth & Global state
│   │   ├── pages/            # Main views Dashboard, Resources
│   │   ├── services/         # API service calls
│   │   └── utils/            # Helper functions
│   └── package.json
│
├── backend/                  # Spring Boot application
│   ├── src/main/java/
│   │   └── com/mentalhealth/
│   │       ├── controller/   # REST APIs
│   │       ├── service/      # Business logic
│   │       ├── repository/   # Data access layer JPA
│   │       ├── model/        # Entity classes
│   │       ├── config/       # Security & Web config
│   │       └── exception/    # Global exception handling
│   ├── src/main/resources/
│   │   └── application.properties
│   └── pom.xml
│
├── ml-model/                 # Python ML Service
│   ├── app/                  
│   │   └── main.py          # FastAPI application
│   ├── notebooks/           # Jupyter notebooks for EDA & training
│   ├── scripts/             # Data preprocessing & training scripts
│   ├── models/              # Saved serialized models .pkl, .joblib
│   ├── requirements.txt
│   └── Dockerfile
│
└── README.md
⚙️ Installation & Setup
Prerequisites
Node.js & npm

Java JDK 11+

Python 3.8+

MySQL or PostgreSQL

1. Clone the Repository
bash
git clone https://github.com/your-username/AI-Powered-Student-Mental-Health-Prediction-Support-System.git
cd AI-Powered-Student-Mental-Health-Prediction-Support-System
2. Backend Setup (Spring Boot)
bash
cd backend
# Configure your database in src/main/resources/application.properties
./mvnw spring-boot:run
The API will be served at http://localhost:8080.

3. Frontend Setup (React)
bash
cd frontend
npm install
npm start
The client will be served at http://localhost:3000.

4. ML Service Setup (Python/FastAPI)
bash
cd ml-model
# Create a virtual environment
python -m venv venv
source venv/bin/activate  # On Windows: venv\Scripts\activate
pip install -r requirements.txt

# Run the FastAPI server
uvicorn app.main:app --reload --host 0.0.0.0 --port 8000
The ML API docs will be available at http://localhost:8000/docs.

🧪 Usage
Student Sign-Up: Students create an account and opt-in to data analysis.

Dashboard: View their own engagement metrics and well-being score.

Surveys: Complete optional weekly well-being check-ins.

Counselor View: Authorized staff see a list of students flagged by the system, ranked by risk level, with explainable factors (e.g., "75% risk due to detected hopelessness and attendance drop").

Intervention: Counselors can initiate confidential support based on the system's alerts.

🧠 ML Model Details
The system uses a hybrid ensemble model for high precision and explainability.

Data: Trained on proxy datasets (e.g., Reddit mental health forums, synthetic academic data).

NLP Model (Transformer): A pre-trained model (e.g., DistilBERT) fine-tuned to detect specific psychological states (hopelessness, anxiety, loneliness) from text.

Anomaly Detection Model (Isolation Forest): Identifies significant deviations in academic performance (e.g., GPA drop) and engagement (e.g., library access).

Meta-Classifier (XGBoost): Takes the outputs from all other models as features and makes the final risk prediction. Its built-in feature importance provides explainability.

⚖️ Ethical Considerations
Consent is Paramount: This must be an opt-in only system for students.

Transparency: Students must be able to see what data is collected and how it is used.

Anonymization: Personal identifiers must be removed before data is used for model inference.

Bias Mitigation: Models must be audited regularly for demographic bias.

Human-in-the-Loop: The system flags at-risk students; it does not diagnose. A trained human professional must always make the final decision.

Data Security: All data must be encrypted in transit and at rest.

🔮 Future Work
Implement Federated Learning to train models on decentralized data without compromising privacy.

Develop a mobile app for push notifications and easier survey access.

Integrate with more data sources (e.g., anonymized fitness tracker data with explicit consent).

Incorporate advanced time-series models (e.g., Temporal Fusion Transformers) for better behavioral analysis.

🤝 Contributing
Contributions, issues, and feature requests are welcome. Feel free to check issues page.

Fork the Project

Create your Feature Branch (git checkout -b feature/AmazingFeature)

Commit your Changes (git commit -m 'Add some AmazingFeature')

Push to the Branch (git push origin feature/AmazingFeature)

Open a Pull Request

📜 License
This project is licensed under the MIT License - see the LICENSE.md file for details.
