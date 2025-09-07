# 🛂 US Visa Approval Prediction using Machine Learning  

![Python](https://img.shields.io/badge/Python-3.8-blue?style=for-the-badge&logo=python)
![Scikit-learn](https://img.shields.io/badge/Scikit--learn-ML%20Models-F7931E?style=for-the-badge&logo=scikit-learn)
![MongoDB](https://img.shields.io/badge/MongoDB-Database-47A248?style=for-the-badge&logo=mongodb)
![Flask](https://img.shields.io/badge/Flask-Web%20App-black?style=for-the-badge&logo=flask)
![DVC](https://img.shields.io/badge/DVC-MLOps-purple?style=for-the-badge&logo=dvc)
![Docker](https://img.shields.io/badge/Docker-Containerization-2496ED?style=for-the-badge&logo=docker)
![AWS](https://img.shields.io/badge/AWS-Deployment-232F3E?style=for-the-badge&logo=amazon-aws)

---

## 📌 Project Overview  
This project builds a **machine learning pipeline** to predict whether a **US visa application will be approved or denied**.  

It includes:  
- 🔍 **Data validation** with schema checks & drift detection  
- ⚙️ **Automated model training & evaluation**  
- 🌐 **Web application (Flask)** for real-time predictions  
- ⚡ **MLOps practices** with DVC, Docker, and AWS CI/CD  

The system is designed to be **scalable, reproducible, and deployment-ready**.  

---

## 📊 Workflow  

1. **Data Ingestion** → Load raw visa data  
2. **Data Validation** → Schema validation, missing columns check, drift detection (Evidently AI)  
3. **Data Transformation** → Preprocessing & feature engineering  
4. **Model Training** → Automated ML with NeuroMF to select best-performing model  
5. **Model Evaluation** → Accuracy, Precision, Recall, F1-score  
6. **Pipeline Orchestration** → Config-driven, modular design  
7. **Deployment** → Flask web app + Docker + AWS (ECR, EC2, GitHub Actions)  

---

## 🛠 Tech Stack  

- **Language:** Python 🐍  
- **Libraries:** Pandas, NumPy, Scikit-learn  
- **Data Validation:** Evidently AI  
- **Database:** MongoDB  
- **Web Framework:** Flask  
- **MLOps Tools:** DVC, GitHub Actions  
- **Deployment:** Docker, AWS EC2, AWS ECR  

---

## 📂 Project Structure  

US-Visa-Approval-Prediction/

│── constant/ # Constant values

│── config_entity/ # Configurations

│── artifact_entity/ # Entities for pipeline artifacts

│── component/ # Data ingestion, validation, transformation, training

│── pipeline/ # Training & prediction pipelines

│── app.py / demo.py # Flask app for deployment

│── requirements.txt # Dependencies

│── config.yaml # Pipeline configuration

│── params.yaml # Hyperparameters

│── dvc.yaml # DVC pipeline

│── setup.py # Installation


---

## 💻 How to Run  

### 🔹 Setup Project  

```bash
# Clone the repository

git clone https://github.com/<your-username>/US-Visa-Approval-Prediction.git

cd US-Visa-Approval-Prediction

# Create virtual environment

conda create -n visa python=3.8 -y

conda activate visa

# Install dependencies

pip install -r requirements.txt

# Run Flask app

python app.py

🔑 Environment Variables

Before running, set up required environment variables:

export MONGODB_URL="mongodb+srv://<username>:<password>@cluster.mongodb.net/..."

export AWS_ACCESS_KEY_ID=<AWS_ACCESS_KEY_ID>

export AWS_SECRET_ACCESS_KEY=<AWS_SECRET_ACCESS_KEY>

☁️ AWS CICD Deployment with GitHub Actions

1️⃣ Login to AWS Console

2️⃣ Create IAM User for Deployment

Access Required:

AmazonEC2FullAccess

AmazonEC2ContainerRegistryFullAccess

3️⃣ Create ECR Repository

4️⃣ Create EC2 Machine (Ubuntu)

5️⃣ Install Docker on EC2

# Optional

sudo apt-get update -y

sudo apt-get upgrade

# Required

curl -fsSL https://get.docker.com -o get-docker.sh

sudo sh get-docker.sh

sudo usermod -aG docker ubuntu

newgrp docker

6️⃣ Configure EC2 as Self-Hosted Runner

Navigate:
GitHub > Repo > Settings > Actions > Runners > New self-hosted runner

Choose Ubuntu, run the commands provided.

7️⃣ Setup GitHub Secrets

AWS_ACCESS_KEY_ID

AWS_SECRET_ACCESS_KEY

AWS_DEFAULT_REGION

ECR_REPO

📈 Results

✅ Achieved high accuracy in visa approval prediction

🚀 Automated model selection ensures best performance

🛡️ Data validation + drift detection improve reliability

☁️ Deployment-ready with AWS + Docker + CI/CD
