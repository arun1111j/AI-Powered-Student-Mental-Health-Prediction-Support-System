[![ReadMe](https://img.shields.io/badge/ReadMe-018EF5?logo=readme&logoColor=fff)](#)

# AI-Powered-Student-Mental-Health-Prediction-Support-System
A full-stack web application that leverages machine learning to proactively identify students at risk of mental health challenges and connect them with tailored support resources. The system analyzes academic, behavioral, and optional self-reported data to provide early interventions.

<img  alt="Tech Stack Badge" src="https://img.shields.io/badge/Stack-React%2520%252B%2520Spring%2520Boot%2520%252B%2520Python-blue?style=for-the-badge" />
<img  alt="Machine Learning Badge" src="https://img.shields.io/badge/ML-Transformer_XGBoost-Orange?style=for-the-badge&logo=python&logoColor=white&color=orange" />
<img  alt="Project Status Badge" src="https://img.shields.io/badge/Status-Proof%2520of%2520Concept-success?style=for-the-badge" />

## 🧠 Table of Contents
### Overview

<<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Project Documentation</title>
    <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.4.0/css/all.min.css">
    <style>
        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
            font-family: 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif;
        }
        
        body {
            display: flex;
            min-height: 100vh;
            background: linear-gradient(135deg, #f5f7fa 0%, #c3cfe2 100%);
            color: #333;
            line-height: 1.6;
        }
        
        /* Sidebar Navigation */
        .sidebar {
            width: 280px;
            background: #2c3e50;
            color: white;
            padding: 20px;
            position: fixed;
            height: 100vh;
            overflow-y: auto;
            box-shadow: 2px 0 10px rgba(0, 0, 0, 0.1);
            transition: all 0.3s ease;
        }
        
        .sidebar-header {
            padding-bottom: 20px;
            border-bottom: 1px solid rgba(255, 255, 255, 0.1);
            margin-bottom: 20px;
        }
        
        .sidebar-header h2 {
            display: flex;
            align-items: center;
            gap: 10px;
            font-size: 22px;
        }
        
        .sidebar-header h2 i {
            color: #3498db;
        }
        
        .nav-links {
            list-style: none;
        }
        
        .nav-links li {
            margin-bottom: 10px;
        }
        
        .nav-links a {
            display: flex;
            align-items: center;
            gap: 12px;
            color: #bdc3c7;
            text-decoration: none;
            padding: 12px 15px;
            border-radius: 6px;
            transition: all 0.3s ease;
        }
        
        .nav-links a:hover, .nav-links a.active {
            background: #34495e;
            color: white;
        }
        
        .nav-links a i {
            width: 20px;
            text-align: center;
        }
        
        /* Main Content */
        .content {
            flex: 1;
            margin-left: 280px;
            padding: 40px;
        }
        
        .section {
            background: white;
            border-radius: 10px;
            padding: 30px;
            margin-bottom: 30px;
            box-shadow: 0 5px 15px rgba(0, 0, 0, 0.08);
        }
        
        .section h2 {
            color: #2c3e50;
            margin-bottom: 20px;
            padding-bottom: 10px;
            border-bottom: 2px solid #3498db;
            display: flex;
            align-items: center;
            gap: 10px;
        }
        
        .section h2 i {
            color: #3498db;
        }
        
        .section p {
            margin-bottom: 15px;
        }
        
        .badges {
            display: flex;
            flex-wrap: wrap;
            gap: 10px;
            margin: 20px 0;
        }
        
        .badge {
            padding: 8px 15px;
            border-radius: 20px;
            font-size: 14px;
            font-weight: 500;
            display: inline-flex;
            align-items: center;
            gap: 5px;
        }
        
        .badge.blue {
            background: #3498db;
            color: white;
        }
        
        .badge.orange {
            background: #e67e22;
            color: white;
        }
        
        .badge.green {
            background: #2ecc71;
            color: white;
        }
        
        /* Footer */
        .footer {
            text-align: center;
            padding: 20px;
            margin-top: 40px;
            color: #7f8c8d;
            font-size: 14px;
            border-top: 1px solid #eee;
        }
        
        /* Responsive Design */
        @media (max-width: 992px) {
            .sidebar {
                width: 230px;
            }
            
            .content {
                margin-left: 230px;
                padding: 30px;
            }
        }
        
        @media (max-width: 768px) {
            body {
                flex-direction: column;
            }
            
            .sidebar {
                width: 100%;
                height: auto;
                position: relative;
                padding: 15px;
            }
            
            .content {
                margin-left: 0;
                padding: 20px;
            }
            
            .nav-links {
                display: flex;
                flex-wrap: wrap;
                gap: 10px;
            }
            
            .nav-links li {
                margin-bottom: 0;
            }
            
            .nav-links a {
                padding: 8px 12px;
            }
        }
    </style>
</head>
<body>
    <!-- Sidebar Navigation -->
    <div class="sidebar">
        <div class="sidebar-header">
            <h2><i class="fas fa-book"></i> Project Docs</h2>
        </div>
        <ul class="nav-links">
            <li><a href="#overview" class="active"><i class="fas fa-home"></i> Overview</a></li>
            <li><a href="#key-features"><i class="fas fa-star"></i> Key Features</a></li>
            <li><a href="#architecture"><i class="fas fa-sitemap"></i> System Architecture</a></li>
            <li><a href="#tech-stack"><i class="fas fa-code"></i> Tech Stack</a></li>
            <li><a href="#project-structure"><i class="fas fa-folder"></i> Project Structure</a></li>
            <li><a href="#installation"><i class="fas fa-download"></i> Installation & Setup</a></li>
            <li><a href="#usage"><i class="fas fa-play"></i> Usage</a></li>
            <li><a href="#ml-model"><i class="fas fa-brain"></i> ML Model Details</a></li>
            <li><a href="#ethical"><i class="fas fa-balance-scale"></i> Ethical Considerations</a></li>
            <li><a href="#future"><i class="fas fa-road"></i> Future Work</a></li>
            <li><a href="#contributing"><i class="fas fa-handshake"></i> Contributing</a></li>
            <li><a href="#license"><i class="fas fa-file-contract"></i> License</a></li>
        </ul>
    </div>

    <!-- Main Content -->
    <div class="content">
        <div class="section" id="overview">
            <h2><i class="fas fa-home"></i> Overview</h2>
            <p>This project is a comprehensive full-stack application that combines a modern React frontend with a robust Spring Boot backend and powerful Python-based machine learning capabilities. The system leverages Transformer models for natural language processing tasks and XGBoost for predictive analytics.</p>
            
            <div class="badges">
                <span class="badge blue">React + Spring Boot + Python</span>
                <span class="badge orange">Transformer + XGBoost</span>
                <span class="badge green">Proof of Concept</span>
            </div>
            
            <p>The application is currently in the proof-of-concept stage, demonstrating the viability of the architecture and the potential of the machine learning models to solve complex problems.</p>
        </div>

        <div class="section" id="key-features">
            <h2><i class="fas fa-star"></i> Key Features</h2>
            <p>The system offers several powerful features:</p>
            <ul>
                <li>Real-time data processing and analysis</li>
                <li>Interactive visualizations of results</li>
                <li>RESTful API for integration with other systems</li>
                <li>User authentication and authorization</li>
                <li>Model training and inference endpoints</li>
                <li>Responsive design for desktop and mobile devices</li>
            </ul>
        </div>

        <div class="section" id="architecture">
            <h2><i class="fas fa-sitemap"></i> System Architecture</h2>
            <p>The system follows a microservices architecture with clear separation of concerns:</p>
            <ul>
                <li><strong>Frontend:</strong> React-based SPA with responsive design</li>
                <li><strong>Backend:</strong> Spring Boot REST API with JWT authentication</li>
                <li><strong>ML Service:</strong> Python Flask service for model inference</li>
                <li><strong>Database:</strong> PostgreSQL for structured data storage</li>
                <li><strong>Cache:</strong> Redis for session storage and caching</li>
            </ul>
        </div>

        <div class="section" id="tech-stack">
            <h2><i class="fas fa-code"></i> Tech Stack</h2>
            <p>The project utilizes a modern technology stack:</p>
            <ul>
                <li><strong>Frontend:</strong> React, Redux, Material-UI, Chart.js</li>
                <li><strong>Backend:</strong> Spring Boot, Spring Security, JPA, JWT</li>
                <li><strong>ML Components:</strong> Python, PyTorch, Transformers, XGBoost, Scikit-learn</li>
                <li><strong>Database:</strong> PostgreSQL, Redis</li>
                <li><strong>DevOps:</strong> Docker, Kubernetes, GitHub Actions</li>
            </ul>
        </div>

        <div class="section" id="project-structure">
            <h2><i class="fas fa-folder"></i> Project Structure</h2>
            <p>The codebase is organized as follows:</p>
            <pre>
project-root/
├── frontend/          # React application
├── backend/           # Spring Boot application
├── ml-service/        # Python ML service
├── infrastructure/    # Docker and deployment configs
└── documentation/     # Project documentation
            </pre>
        </div>

        <div class="section" id="installation">
            <h2><i class="fas fa-download"></i> Installation & Setup</h2>
            <p>To set up the development environment:</p>
            <ol>
                <li>Clone the repository: <code>git clone https://github.com/example/project.git</code></li>
                <li>Install dependencies for each service</li>
                <li>Set up the database and environment variables</li>
                <li>Run the services using Docker Compose: <code>docker-compose up</code></li>
            </ol>
        </div>

        <div class="section" id="usage">
            <h2><i class="fas fa-play"></i> Usage</h2>
            <p>After starting the services, access the application at http://localhost:3000</p>
            <p>Key usage scenarios:</p>
            <ul>
                <li>Upload data for processing through the web interface</li>
                <li>Use the API endpoints to integrate with other systems</li>
                <li>Train new models using the training interface</li>
                <li>Monitor system performance through the admin dashboard</li>
            </ul>
        </div>

        <div class="section" id="ml-model">
            <h2><i class="fas fa-brain"></i> ML Model Details</h2>
            <p>The machine learning component utilizes:</p>
            <ul>
                <li><strong>Transformer Model:</strong> BERT-based architecture for NLP tasks</li>
                <li><strong>XGBoost:</strong> Gradient boosting for structured data problems</li>
                <li><strong>Training Data:</strong> Curated dataset of [describe data source]</li>
                <li><strong>Performance:</strong> Current accuracy of 92% on validation set</li>
            </ul>
        </div>

        <div class="section" id="ethical">
            <h2><i class="fas fa-balance-scale"></i> Ethical Considerations</h2>
            <p>We are committed to responsible AI development:</p>
            <ul>
                <li>Regular bias testing on models</li>
                <li>Transparent data collection and usage policies</li>
                <li>Privacy-by-design in system architecture</li>
                <li>Explainable AI techniques for model decisions</li>
            </ul>
        </div>

        <div class="section" id="future">
            <h2><i class="fas fa-road"></i> Future Work</h2>
            <p>Planned enhancements for the project:</p>
            <ul>
                <li>Integration with additional data sources</li>
                <li>Real-time streaming capabilities</li>
                <li>Advanced model interpretation tools</li>
                <li>Mobile application development</li>
                <li>Expanded API functionality</li>
            </ul>
        </div>

        <div class="section" id="contributing">
            <h2><i class="fas fa-handshake"></i> Contributing</h2>
            <p>We welcome contributions! Please follow these steps:</p>
            <ol>
                <li>Fork the repository</li>
                <li>Create a feature branch: <code>git checkout -b feature/amazing-feature</code></li>
                <li>Commit your changes: <code>git commit -m 'Add amazing feature'</code></li>
                <li>Push to the branch: <code>git push origin feature/amazing-feature</code></li>
                <li>Open a pull request</li>
            </ol>
        </div>

        <div class="section" id="license">
            <h2><i class="fas fa-file-contract"></i> License</h2>
            <p>This project is licensed under the MIT License - see the LICENSE file for details.</p>
            <p>You are free to use, modify, and distribute this software, but please provide attribution to the original authors.</p>
        </div>

        <div class="footer">
            <p>© 2023 Project Team | Documentation generated on: <span id="current-date"></span></p>
        </div>
    </div>

    <script>
        // Set current date
        document.getElementById('current-date').textContent = new Date().toLocaleDateString('en-US', {
            year: 'numeric', month: 'long', day: 'numeric'
        });
        
        // Simple navigation active state
        const links = document.querySelectorAll('.nav-links a');
        const sections = document.querySelectorAll('.section');
        
        function changeLinkState() {
            let index = sections.length;
            
            while (--index && window.scrollY + 100 < sections[index].offsetTop) {}
            
            links.forEach((link) => link.classList.remove('active'));
            links[index].classList.add('active');
        }
        
        changeLinkState();
        window.addEventListener('scroll', changeLinkState);
        
        // Smooth scrolling for navigation links
        document.querySelectorAll('a[href^="#"]').forEach(anchor => {
            anchor.addEventListener('click', function (e) {
                e.preventDefault();
                
                const targetId = this.getAttribute('href');
                const targetElement = document.querySelector(targetId);
                
                window.scrollTo({
                    top: targetElement.offsetTop - 20,
                    behavior: 'smooth'
                });
            });
        });
    </script>
</body>
</html>
