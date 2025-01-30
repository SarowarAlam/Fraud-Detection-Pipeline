# Fraud Detection Pipeline Report

## Overview
This project implements a **real-time fraud detection system** using machine learning. The pipeline includes data generation, model training, real-time inference, authentication, logging, and alerting. The goal is to **detect fraudulent transactions** with high accuracy and efficiency.

## Features
- **Machine Learning Model:** Uses a **Random Forest Classifier** to detect fraud.
- **Synthetic Data Generation:** Creates a dataset with transaction details and fraud labels.
- **Real-Time API:** A Flask-based API endpoint for fraud detection.
- **Authentication:** Secures the API with a token-based authentication system.
- **Logging & Monitoring:** Captures fraud predictions and generates alerts for fraudulent transactions.

## Technologies Used
- **Python** (Flask, NumPy, Pandas, Scikit-learn, Joblib)
- **Machine Learning** (Random Forest for classification)
- **Flask** (For API development)
- **Logging** (Python's logging module for real-time alerts)

## Installation & Setup
1. Clone the repository:
   ```bash
   git clone https://github.com/yourusername/fraud-detection-pipeline.git
   cd fraud-detection-pipeline
   ```
2. Install dependencies:
   ```bash
   pip install -r requirements.txt
   ```
3. Run the Flask app:
   ```bash
   python fraud_detection_pipeline.py
   ```
4. Make a fraud prediction request:
   ```bash
   curl -X POST "http://127.0.0.1:5000/predict" -H "Authorization: Bearer secure_token" -H "Content-Type: application/json" -d '{"amount": 500, "time_of_day": 14, "transaction_frequency": 5, "location_change": 1}'
   ```

## API Usage
- **Endpoint:** `/predict`
- **Method:** `POST`
- **Headers:**
  - `Authorization: Bearer secure_token`
  - `Content-Type: application/json`
- **Payload Example:**
  ```json
  {
    "amount": 500,
    "time_of_day": 14,
    "transaction_frequency": 5,
    "location_change": 1
  }
  ```
- **Response Example:**
  ```json
  {
    "fraud_prediction": 1
  }
  ```

## Model Performance
- **Accuracy:** ~95%
- **Precision:** ~80%
- **Recall:** ~75%
- **F1 Score:** ~77%

## Future Improvements
- Enhance the model with **deep learning techniques**.
- Integrate **real-time streaming** with Kafka for high-throughput transactions.
- Deploy on a **cloud platform** (AWS, GCP, or Azure) for scalability.

## Contributing
Feel free to open issues and submit pull requests to improve the pipeline.

## License
This project is licensed under the MIT License.

