# Real Estate Price Prediction in Bangalore

[![GitHub Repo](https://img.shields.io/badge/GitHub-Repository-blue)](https://github.com/imakhxl/Real-Estate-Price-Prediction-in-Banglore)

## Overview
This project predicts real estate prices in Bangalore using machine learning and provides a web-based interface for **real-time price estimation**. It demonstrates an **end-to-end ML workflow**: from data cleaning and model training to API creation and deployment on AWS.

## Features
- Predict housing prices in Bangalore based on **total square feet, BHK, bathrooms, and location**.
- Real-time prediction through a **Flask API** integrated with a **responsive frontend**.
- Deployed on **AWS EC2** for scalability and accessibility.
- End-to-end pipeline: data processing → model training → API → deployment.

## Model Details
- **Algorithm:** Linear Regression  
- **Accuracy:** ~90%  
- **Dataset:** Bangalore housing prices  
- **Techniques Used:** Feature engineering, hyperparameter tuning, and data cleaning  

## Tech Stack
- **Backend:** Python, Flask  
- **Frontend:** HTML, CSS, JavaScript  
- **Machine Learning:** Pandas, NumPy, scikit-learn, Matplotlib  
- **Deployment:** AWS EC2, Gunicorn, Nginx  
- **Version Control:** Git, GitHub  

## Installation

1. Clone the repository
git clone https://github.com/imakhxl/Real-Estate-Price-Prediction-in-Banglore.git
cd Real-Estate-Price-Prediction-in-Banglore/server

2. Create a virtual environment
python3 -m venv venv
source venv/bin/activate   # Linux/Mac
venv\Scripts\activate      # Windows

3. Install dependencies
pip install -r requirements.txt

Usage
Run locally with Flask
python server.py


API Endpoints:

GET /get_location_names → returns all available locations

POST /predict_home_price → predict home price with total_sqft, bhk, bath, location

Run with Gunicorn (Production-ready)
nohup gunicorn --bind 0.0.0.0:5000 server:app &


Access locally at http://127.0.0.1:5000

Deployment

Deployed on AWS EC2 t3.micro instance

Gunicorn serves the Flask app, optionally behind Nginx

API accessible over the internet via EC2 public IP or domain

Live demo: Available on request

File Structure
.
├── server/
│   ├── server.py
│   ├── util.py
│   └── artifacts/
│       ├── columns.json
│       └── banglore_home_prices_model.pickle
├── client/
│   ├── app.html
│   ├── app.css
│   └── app.js
├── model/
│   ├── banglore_home_prices_model.pickle
│   ├── columns.json
│   └── Real Estate Price Prediction in Banglore.ipynb
├── requirements.txt
└── README.md

How to Contribute

Fork the repository

Create your branch: git checkout -b feature-name

Commit your changes: git commit -m "Description of changes"

Push to the branch: git push origin feature-name

Create a Pull Request

License

MIT License

Contact

GitHub: imakhxl

Email: akhilj2003@gmail.com.com

