✈️ Airline Revenue Management Analytics & Machine Learning Platform

A serverless, ML-powered airline Revenue Management (RM) platform that combines booking analytics, advanced querying, and predictive machine learning models.
Built with Flask, Scikit-Learn, and AWS Lambda, this project simulates how modern airlines support pricing, demand forecasting, and revenue optimization decisions.

📌 Key Features
🔐 Authentication

Secure login using Flask-Login

Role-ready architecture (analyst, admin, RM manager)

📊 Revenue Management Analytics

Revenue by route, POS, fare class

Passenger and yield trends

Seasonality and pricing impact analysis

Advanced query logic inspired by real RM systems (Altéa, PROS, Sabre)

🧠 Machine Learning (Core Differentiator)

Demand Forecasting Model

Predicts expected passengers for future flights

Willingness-to-Pay (WTP) Model

Classifies customers as price-sensitive vs high-value

Buy-Down / Waiting Risk Model

Predicts likelihood of customers delaying purchase for lower fares

All models trained using historical booking data

☁️ Serverless Cloud Hosting

Hosted for free using:

AWS Lambda

API Gateway

Deployed using Zappa

HTTPS endpoint generated automatically

🏗️ Technology Stack
Layer	Technology
Backend	Flask (Python)
Authentication	Flask-Login
Database	SQLite (Lambda-compatible)
Analytics	Pandas, SQLAlchemy
Machine Learning	Scikit-Learn
Model Persistence	Joblib
Cloud	AWS Lambda + API Gateway
Deployment	Zappa
📁 Project Structure
airline-rm-ml-platform/
│
├── application.py          # Flask app entry point
├── config.py               # App configuration
├── load_csv.py             # Load booking CSV into DB
├── train_models.py         # Train ML models
│
├── models/
│   ├── user.py             # User authentication model
│   ├── booking.py          # Booking data model
│   └── ml_models.py        # ML model helpers
│
├── routes/
│   ├── auth_routes.py      # Login / logout
│   ├── dashboard_routes.py # Main dashboard
│   └── analytics_routes.py # RM analytics & ML queries
│
├── ml/
│   ├── demand_model.pkl
│   ├── wtp_model.pkl
│   └── risk_model.pkl
│
├── templates/
│   ├── login.html
│   ├── dashboard.html
│   └── analytics.html
│
└── static/

🚀 Setup Instructions (Local)
1️⃣ Clone Repository
git clone <your-repo-url>
cd airline-rm-ml-platform

2️⃣ Create Virtual Environment
python -m venv venv
venv\Scripts\activate

3️⃣ Install Dependencies
pip install flask flask-login flask-sqlalchemy pandas numpy scikit-learn joblib zappa awscli

📥 Load Booking Data

You already have the booking CSV file.

python load_csv.py


This will:

Create bookings.db

Load all booking records

🧠 Train Machine Learning Models
python train_models.py


Outputs:

ml/
├── demand_model.pkl
├── wtp_model.pkl
└── risk_model.pkl

▶️ Run Application Locally
python application.py


Access:

http://127.0.0.1:5000

☁️ Deploy to AWS Lambda (Free Tier)
1️⃣ Configure AWS CLI
aws configure

2️⃣ Initialize Zappa
zappa init


Use:

App function: application.app

Runtime: python3.10

Region: us-east-1

3️⃣ Deploy
zappa deploy dev


Zappa returns a public HTTPS URL 🎉

4️⃣ Update Deployment
zappa update dev

🧪 Machine Learning Overview
Model	Algorithm	Purpose
Demand Forecast	Linear Regression	Predict passengers
WTP Model	Logistic Regression	High vs low value customers
Buy-Down Risk	Random Forest	Fare waiting behavior

All models are trained on:

Route

Seasonality

Day of week

Fare price

Passenger history

🧠 What Makes This Project Unique

✅ Combines analytics + ML (not just dashboards)
✅ Includes pricing risk & WTP modeling (rare in demos)
✅ Serverless & production-style deployment
✅ Inspired by real airline RM systems (PROS, Altéa, Sabre)
✅ Interview-ready and portfolio-grade

📌 Future Enhancements

SHAP model explainability

PostgreSQL (RDS)

Real-time pricing simulation

Role-based access control

CI/CD pipeline
