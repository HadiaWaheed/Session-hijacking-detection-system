# Session-hijacking

# Session Hijacking Detection System

## Overview
This project aims to detect session hijacking vulnerabilities in websites by analyzing HTTP headers, cookie flags, and session-related features using machine learning (Random Forest classifier).

## Dataset
- The dataset includes categorical and numerical features extracted from HTTP headers and cookies.
- It contains columns such as `Strict-Transport-Security`, `Set-Cookie`, `HttpOnly`, `Secure`, `SameSite`, and several missing security flags.
- The target variable is `Security_Class` with classes: Secure, Insecure, Highly Insecure.

## Features
Categorical columns:
- Strict-Transport-Security
- Set-Cookie
- X-Content-Type-Options
- X-Frame-Options
- Cookie Name
- HttpOnly
- Secure
- SameSite
- Session in URL
- Session in Cookies
- Session in Referer
- Authentication Mechanism

Numerical columns:
- Missing_Cookie_Flag
- Missing_HttpOnly
- Missing_Secure
- Missing_HSTS
- Missing_X-Content-Type-Options
- Missing_X-Frame-Options
- Missing_SameSite
- Missing_Auth_Method
- Total_Security_Impact

## Model
- The project uses a Random Forest model saved as `session_rf_model.pkl`.
- The model predicts the security classification based on extracted features.

## Usage
1. Clone the repository.
2. Install dependencies: `pip install -r requirements.txt`
3. Run the Flask app: `python app.py`
4. Open `http://localhost:5000` in your browser.
5. Enter a URL to analyze its session security.

