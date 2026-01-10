# British Airways Data Science Project

## ✈️ Project Overview
This repository contains the analysis and machine learning models developed for the British Airways Data Science Virtual Internship. The project tackles two critical business problems: optimizing lounge staffing through data modeling and predicting customer booking behavior using machine learning.

## 📊 Task 1: Lounge Utilization Analysis
**Goal:** Estimate lounge demand per flight to optimize staffing and stock allocation.

* **Approach:** Built a probabilistic "Lookup Table" using Python to estimate passenger eligibility based on flight metadata (Route, Time, Aircraft).
* **Key Findings:**
    * **Europe** routes have the highest density of eligible passengers (~21.6%), driven by frequent business commuters.
    * **Long-haul PM** flights drive the highest demand for premium dining services.
    * **Strategic Recommendation:** Shift staffing peaks to align with "Short-haul AM" departure waves rather than total passenger volume.
* **Key Files:** `01_lounge_utilization_analysis.ipynb`, `lounge_lookup_table.csv`

## 🤖 Task 2: Customer Booking Prediction
**Goal:** Build a predictive model to identify which customers are most likely to complete a flight booking.

* **Approach:**
    * Trained a **Random Forest Classifier** on 50,000 customer records.
    * Engineered features from booking data (Lead time, Route, Ancillaries).
* **Results:**
    * **Accuracy:** **85.2%**
    * **Top Predictor:** `purchase_lead` (Time between search and travel) is the strongest indicator of buying behavior.
    * **Insight:** Customers selecting **ancillaries** (Extra Bags, Preferred Seats) show significantly higher booking intent.
* **Key Files:** `02_customer_booking_prediction.ipynb`, `customer_booking.csv`

## 📂 Repository Structure
```text
├── 01_lounge_utilization_analysis.ipynb   # Task 1: Data Cleaning & Logic
├── 02_customer_booking_prediction.ipynb   # Task 2: Machine Learning Model
├── lounge_lookup_table.csv                # Task 1 Output: The Strategy Table
├── customer_booking.csv                   # Task 2 Data: Source file
├── requirements.txt                       # Dependencies
└── README.md                              # Project Documentation