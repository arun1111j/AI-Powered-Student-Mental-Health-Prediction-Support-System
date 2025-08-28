# AI-Powered Student Mental Health Prediction Support System

[![ReadMe](https://img.shields.io/badge/ReadMe-018EF5?logo=readme&logoColor=fff)](#)

A full-stack web application that leverages machine learning to proactively identify students at risk of mental health challenges and connect them with tailored support resources.

<img src="https://img.shields.io/badge/React-20232A?style=for-the-badge&logo=react&logoColor=61DAFB"><img src="https://img.shields.io/badge/Spring_Boot-6DB33F?style=for-the-badge&logo=spring-boot&logoColor=white"> 
<img src="https://img.shields.io/badge/Python-3776AB?style=for-the-badge&logo=python&logoColor=white"> 
<img src="https://img.shields.io/badge/Transformer-XGBoost-orange">
<img src="https://img.shields.io/badge/Status-Proof%20of%20Concept-green">

## Overview

This project is an AI-powered system designed to identify students who may be at risk of mental health challenges using machine learning. By analyzing academic performance, behavioral patterns, and optional self-reported data, the system provides early intervention recommendations and connects students with appropriate support resources.

simple README.md with a link to the documentation: [Live Documentation Page](https://ai-powered-student-mental-health-pr.vercel.app)

### Our Mission

To create a supportive educational environment where students' mental well-being is proactively addressed through ethical AI applications, reducing stigma and providing timely access to resources.

The application is currently in the proof-of-concept stage, demonstrating the viability of the architecture and the potential of the machine learning models to identify at-risk students while maintaining strict privacy and ethical standards.

## Key Features

- **Early Risk Detection:** Machine learning models identify patterns indicative of mental health challenges
- **Personalized Recommendations:** Tailored support resources based on individual needs
- **Anonymous Reporting:** Optional self-reporting tools for students to express concerns
- **Counselor Dashboard:** Specialized interface for mental health professionals to monitor and intervene
- **Privacy-First Design:** Data anonymization and strict access controls to protect student privacy
- **Responsive Design:** Accessible on desktop and mobile devices

## System Architecture

The system follows a microservices architecture with clear separation of concerns to ensure scalability and maintainability:

- **Frontend:** React-based SPA with responsive design and interactive visualizations
- **Backend API:** Spring Boot REST API with JWT authentication and role-based access
- **ML Service:** Python Flask service for model training and inference
- **Database:** PostgreSQL for structured data storage with encryption at rest
- **Cache:** Redis for session storage and caching of frequently accessed data
- **Message Queue:** RabbitMQ for asynchronous processing of prediction tasks

### System Architecture Diagram

<img width="2208" height="925" alt="diagram-export-8-27-2025-9_56_38-PM" src="https://github.com/user-attachments/assets/906fb7f3-3913-413f-9981-4ee46663387d" />

### Student Risk Prediction Pipeline Diagram

<img width="3504" height="1795" alt="diagram-export-8-27-2025-10_01_44-PM" src="https://github.com/user-attachments/assets/68fd082a-f742-41b1-a929-b1eef4b750ec" />


### Privacy & Security

All student data is anonymized before processing, and personally identifiable information is stored separately from behavioral data. The system complies with FERPA and other educational privacy regulations.

## Tech Stack

The project utilizes a modern, robust technology stack chosen for performance, scalability, and developer ecosystem:

- **Frontend:** React, Redux, Material-UI, Chart.js, D3.js
- **Backend:** Spring Boot, Spring Security, JPA, JWT, OAuth 2.0
- **ML Components:** Python, PyTorch, Transformers, XGBoost, Scikit-learn, NLTK
- **Database:** PostgreSQL, Redis, Elasticsearch
- **DevOps:** Docker, Kubernetes, GitHub Actions, Prometheus, Grafana

## Project Structure

### Website Structure
```text
mental-health-ai/
├── frontend/ # React application
│ ├── public/ # Static assets
│ ├── src/
│ │ ├── components/ # Reusable UI components
│ │ ├── pages/ # Page components
│ │ ├── services/ # API communication
│ │ └── utils/ # Helper functions
├── backend/ # Spring Boot application
│ ├── src/main/java/
│ │ ├── controller/ # REST controllers
│ │ ├── service/ # Business logic
│ │ ├── repository/ # Data access layer
│ │ ├── model/ # Data models
│ │ └── config/ # Application configuration
├── ml-service/ # Python ML service
│ ├── app/ # Flask application
│ ├── models/ # Trained model files
│ ├── training/ # Model training scripts
│ └── inference/ # Prediction scripts
├── infrastructure/ # Docker and deployment configs
└── documentation/ # Project documentation
```
### Model Structure
```text
ml-service/
├── app/                    # Flask application
│   ├── __init__.py
│   ├── routes.py          # API endpoints
│   └── error_handlers.py
├── data/
│   ├── raw/               # Original data sources
│   │   ├── textual/
│   │   ├── academic/
│   │   ├── behavioral/
│   │   └── surveys/
│   └── processed/         # Cleaned and preprocessed data
├── models/                # Serialized trained models (.pkl, .h5)
├── utils/                 # Helper functions
│   ├── preprocessors.py
│   ├── plotters.py
│   └── constants.py
├── pipelines/             # Core ML Pipelines
│   ├── nlp_pipeline.py    # NLP and Sentiment Analysis Transformer Model
│   ├── anomaly_pipeline.py # Academic Performance Anomaly Detection
│   ├── trend_pipeline.py  # Psychological Trend Analysis
│   ├── behavioral_pipeline.py # Behavioral Pattern Analysis
│   └── fusion_pipeline.py # SINGOLIAR - Feature Vector Fusion & Meta Classifier
├── inference/             # Prediction scripts
│   ├── predictor.py
│   └── model_loader.py
├── training/              # Model training scripts
│   ├── train.py           # Script to train all models
│   └── data_preprocessor.py
├── requirements.txt
├── Dockerfile
└── app.py                 # Main Flask application entry point
```

## Installation & Setup

To set up the development environment for this project:

1. Clone the repository: `git clone https://github.com/arun1111j/AI-Powered-Student-Mental-Health-Prediction-Support-System.git`
2. Install Docker and Docker Compose on your system
3. Navigate to the project directory: `cd mental-health-ai`
4. Copy the environment template: `cp .env.example .env`
5. Update the environment variables with your configuration
6. Build and start the containers: `docker-compose up --build`
7. Access the application at`http://localhost:3000`

### Important Note

This application processes sensitive student data. Ensure you have appropriate security measures and compliance protocols in place before deploying to production.

## Usage

After starting the services, access the application at `http://localhost:3000`

Key usage scenarios:

- **Students:** Access resources, optionally report concerns, view personalized recommendations
- **Educators:** Monitor class well-being metrics, receive alerts about at-risk students
- **Counselors:** Access detailed dashboards, intervention tools, and student progress tracking
- **Administrators:** Manage system settings, user permissions, and view analytics

## ML Model Details

The machine learning component utilizes state-of-the-art techniques while maintaining explainability:

- **Transformer Model:** BERT-based architecture for analyzing text data from optional student journals
- **XGBoost:** Gradient boosting for structured data problems (attendance, grades, activity participation)
- **Feature Engineering:** Carefully selected features that avoid biases and protect privacy
- **Training Data:** Synthetic data based on research patterns (no real student data used in proof-of-concept)
- **Performance:** Current accuracy of 85% on validation set with precision-recall optimized for early detection

### Model Interpretation

All predictions include explainable AI components that help counselors understand why a student was flagged, ensuring human oversight and appropriate context for interventions.

## Ethical Considerations

We are committed to responsible AI development with these core principles:

- **Transparency:** Clear documentation of how data is used and how predictions are made
- **Bias Mitigation:** Regular auditing of models for demographic biases
- **Privacy Protection:** Data minimization and anonymization practices
- **Human Oversight:** All recommendations are reviewed by trained professionals
- **Voluntary Participation:** Students can opt-out of data collection at any time
- **Beneficence:** The system is designed solely to support student well-being

## Future Work

Planned enhancements for the project:

- Integration with popular Learning Management Systems (LMS)
- Mobile application for increased accessibility
- Advanced natural language processing for more nuanced text analysis
- Longitudinal tracking of intervention effectiveness
- Multi-institution collaboration tools for research
- Enhanced counselor tools with workflow management

## Contributing

We welcome contributions from developers, researchers, and mental health professionals! Please follow these steps:

1. Fork the repository
2. Create a feature branch: `git checkout -b feature/amazing-feature`
3. Commit your changes: `git commit -m 'Add amazing feature'`
4. Push to the branch: `git push origin feature/amazing-feature`
5. Open a pull request

### Contribution Guidelines

Please read our contribution guidelines and code of conduct before submitting. All contributors must complete ethics training related to student data privacy.

## License

This project is licensed under the Apache License 2.0 - see the LICENSE file for details.

You are free to use, modify, and distribute this software, with the condition that any use involving real student data must implement appropriate privacy and security measures and comply with all applicable regulations.

### Important Notice

This software is provided as-is without warranty. Organizations using this system are solely responsible for compliance with local privacy laws and regulations regarding student data.

---

© 2023 Mental Health AI Project | Documentation generated on: [Current Date]

**If you're experiencing a mental health crisis, please contact a professional. This tool is designed for early intervention, not emergency response.**
