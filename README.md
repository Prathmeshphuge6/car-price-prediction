# AutoValuate — Vehicle Price Prediction Dashboard

A Flask web dashboard that predicts used vehicle prices using a Random Forest
model trained on 8,000+ Indian vehicle transactions.

---

## About

AutoValuate is a machine learning web application that estimates the resale
price of used cars in the Indian market. It provides instant price predictions,
a confidence range, and a feature importance breakdown based on real transaction data.

---

## Model Details

- **Algorithm:** Random Forest Regressor (100 trees, max_depth=12)
- **R² Score:** 0.9828
- **Dataset:** 8,000+ Indian vehicle transactions
- **Top Features:** Engine Power (69%), Year (17%), KM Driven (6%)

---

## Project Structure

vehicle_dashboard/
├── app.py               # Flask backend — routes and prediction logic
├── model.pkl            # Trained Random Forest model
├── encoders.pkl         # Label encoders for categorical features
├── requirements.txt     # Python dependencies
├── Vehicle.csv          # Dataset
├── templates/
│   └── index.html       # Dashboard HTML
└── static/
├── css/
│   └── style.css    # Stylesheet
└── js/
└── app.js       # Form handling and API calls



---

## Setup

**1. Install dependencies**
```bash
pip install -r requirements.txt
```

**2. Add the dataset**

Place `Vehicle.csv` in the root project folder alongside `app.py`.

**3. Run the app**
```bash
python app.py
```

**4. Open in browser**




> To retrain the model from scratch, run `python train_model.py` before starting the app.

---

## Input Features

| Feature          | Type   | Values                                              |
|------------------|--------|-----------------------------------------------------|
| Year             | Number | 1994 – 2020                                         |
| KM Driven        | Number | 1 – 475,000 km                                      |
| Engine Power     | Number | 32 – 280 bhp                                        |
| Engine CC        | Number | 624 – 3,604 cc                                      |
| Fuel Efficiency  | Number | 0 – 33.44 kmpl                                      |
| Seats            | Select | 2, 4, 5, 6, 7, 8, 9                                 |
| Fuel Type        | Select | Petrol, Diesel, CNG, LPG                            |
| Transmission     | Select | Manual, Automatic                                   |
| Owner History    | Select | First / Second / Third / Fourth+ / Test Drive       |
| Seller Type      | Select | Individual, Dealer, Trustmark Dealer                |

---

## Tech Stack

- **Backend:** Python, Flask
- **Machine Learning:** scikit-learn
- **Frontend:** HTML, CSS, JavaScript

---

## Author

Prathmesh Phuge



