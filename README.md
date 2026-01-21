Airline Revenue Management Analytics Platform

A Revenue Management (RM) Analytics & Governance Platform built with Flask, PostgreSQL, and Python, designed to simulate airline pricing, demand, and revenue optimization. This project showcases advanced query capabilities, login authentication, and explainable analytics, going beyond traditional RM systems like Altéa, Sabre Mosaic, and PROS.

🔹 Features

Login Authentication: Secure user login system using Flask-Login.

Dashboard: Overview of revenue metrics and performance indicators.

Advanced Query Engine: Analyst-driven queries including:

Explainable price changes (why prices moved)

Revenue risk analysis (simulate downside revenue scenarios)

WTP (Willingness-to-Pay) and buy-down risk evaluation

CSV Integration: Load historical flight booking data for analysis.

PostgreSQL Backend: Stores flight and booking data for scalable analytics.

Progressive Queries: Analyst can run strategy sandbox queries and validate RM outputs.

🔹 Technologies Used

Backend: Python, Flask, SQLAlchemy

Database: PostgreSQL

Data Analysis: Pandas, NumPy

Authentication: Flask-Login

Frontend: HTML, Bootstrap (optional for styling)

🔹 Project Structure
airline-rm-analytics/
│
├── app.py                  # Main Flask application
├── config.py               # Configuration (DB connection, secret key)
├── load_csv.py             # Script to load bookings CSV into DB
│
├── models/                 # Database models
│   ├── __init__.py
│   ├── user.py
│   └── booking.py
│
├── routes/                 # Application routes
│   ├── __init__.py
│   ├── auth_routes.py
│   ├── dashboard_routes.py
│   └── query_routes.py
│
├── templates/              # HTML templates
│   ├── login.html
│   ├── dashboard.html
│   └── query.html
│
└── static/                 # CSS/JS files (optional)

🔹 Setup Instructions

Clone the repository

git clone <repo-url>
cd airline-rm-analytics


Create and activate a virtual environment

python -m venv venv
venv\Scripts\activate


Install dependencies

pip install -r requirements.txt


Set up PostgreSQL database

Create a database named airline_rm

Update config.py with your PostgreSQL credentials

Load booking data from CSV

python load_csv.py


Run the Flask app

python app.py


Access in browser

http://127.0.0.1:5000

🔹 Usage

Login Page: Enter credentials to access the dashboard.

Dashboard: View revenue summaries and key metrics.

Query UI: Select query type and run advanced RM analyses:

Price explanations

Revenue risk simulations

Buy-down and WTP segmentation

CSV Updates: Load new booking data anytime for real-time analytics.

🔹 Screenshots

(Optional: add screenshots of login, dashboard, and query results here)

🔹 Why This Project Stands Out

Explainable Analytics: Provides human-readable reasoning for pricing decisions.

Risk-Aware Queries: Simulate revenue scenarios and downside risk.

Analyst Control: Sandbox queries allow strategy testing beyond typical RM systems.

Interview-Ready: Demonstrates technical skills in Python, Flask, SQL, and data analytics, aligned with Solutions & Analytics Analyst responsibilities.

🔹 Future Enhancements

Natural language query input for analysts

Interactive visualizations using Plotly or Dash

Machine learning–based WTP prediction

Docker deployment for cloud-ready setup

Role-based permissions for multi-level analyst access

🔹 Author

John Kipkemboi Kimaiyo
Email: kimaiyojohn6@gmail.com

Portfolio: https://johnkimaiyo-rosy.vercel.app/
