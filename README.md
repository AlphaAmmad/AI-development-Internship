# 🤖 AI Analytics Dashboard
<img width="1846" height="960" alt="image" src="https://github.com/user-attachments/assets/31500809-e681-4bca-93f4-0d6fc105fdc5" />

A comprehensive machine learning dashboard providing advanced analytics solutions for business intelligence. This project includes three main AI-powered features: customer churn prediction, sales forecasting, and product recommendations.

## 📋 Project Summary

The AI Analytics Dashboard is a full-stack web application that combines multiple machine learning models to provide business insights:

### Features
- **🔮 Customer Churn Prediction**: Predict customer churn probability using logistic regression
<img width="1846" height="960" alt="image" src="https://github.com/user-attachments/assets/559ada81-6be5-4786-b3ac-77588ec72a57" />

- **📈 Sales Forecasting**: Forecast future sales trends and demand patterns with time series analysis

<img width="1846" height="960" alt="image" src="https://github.com/user-attachments/assets/1491ad9f-aed2-44b3-b3ee-22d60ea9da62" />
<img width="1846" height="960" alt="image" src="https://github.com/user-attachments/assets/fd10c3d2-9bc0-4729-ae95-00cb1259ad09" />
<img width="1846" height="960" alt="image" src="https://github.com/user-attachments/assets/1babba7b-e033-4478-bcf5-881c2d62dad5" />
<img width="1846" height="960" alt="image" src="https://github.com/user-attachments/assets/1e557dfc-751a-4966-89d0-7439dadac491" />

- **🛍️ Product Recommendations**: Get personalized product recommendations using XGBoost classifier
<img width="1846" height="960" alt="image" src="https://github.com/user-attachments/assets/45b96f17-7235-45fe-9b18-92a70a579307" />
<img width="1846" height="960" alt="image" src="https://github.com/user-attachments/assets/802b58f0-e682-401c-a7aa-b9a51c6ca667" />


## 📊 Data Requirements & Input Guidelines

### 🔮 Customer Churn Prediction

**Required Input Fields:**
- `customer_tenure`: Customer tenure in months (1-120)
- `number_of_services_or_products`: Number of services (1-8)
- `average_monthly_usage`: Monthly usage amount (50.0-500.0)
- `days_since_last_interaction`: Days since last interaction (0-365)
- `complaints_resolved_ratio`: Complaint resolution ratio (0.0-1.0)
- `total_spent`: Total amount spent (100-10000)
- `average_transaction_value`: Average transaction value (100-2000)
- `discount_or_offer_received`: Discount received (0=No, 1=Yes)
- `account_status`: Account status (Active, Inactive, Suspended, Closed)

**Example Input:**
```json
{
  "customer_tenure": 46,
  "number_of_services_or_products": 1,
  "average_monthly_usage": 156.21,
  "days_since_last_interaction": 192,
  "complaints_resolved_ratio": 0.84,
  "total_spent": 8691.93,
  "average_transaction_value": 869.19,
  "discount_or_offer_received": 1,
  "account_status": "Closed"
}
```

**If using your own CSV for churn prediction, it must contain these columns:**
```csv
name,customer_id,customer_tenure,number_of_services_or_products,average_monthly_usage,last_interaction_date,days_since_last_interaction,number_of_complaints,complaints_resolved_ratio,total_spent,average_transaction_value,outstanding_balance,payment_frequency,discount_or_offer_received,customer_support_calls,account_status,churn_flag
```

### 🛍️ Product Recommendations

**Required Input Fields:**
- `region`: Customer region (India, Pakistan, UAE)
- `gender`: Customer gender (Male, Female)
- `user_age_group`: Age group (18-25, 25-30, 30-40, 40+)
- `user_preferences`: Style preference (office wear, sports wear, daily wear, party wear)
- `season`: Current season (Spring, Summer, Autumn, Winter)
- `product_keywords`: Product interests (comma-separated: shoes, shirts, jeans, etc.)
- `previous_buy`: Last purchased item

**If using your own CSV for recommendations, it must contain these columns:**
```csv
user_id,region,gender,user_age_group,user_preferences,season,product_keywords,previous_buy,suggested_brand,suggested_product
```

### 📈 Sales Forecasting

**CSV Requirements:**
- Must contain date column and sales/value column
- Date format: YYYY-MM-DD or MM/DD/YYYY
- Minimum 30 data points recommended
- No missing values in key columns

**Example CSV structure:**
```csv
date,sales
2024-01-01,1500.50
2024-01-02,1750.25
2024-01-03,1200.75
```


### Tech Stack
- **Backend**: Flask (Python) with CORS support
- **Frontend**: HTML5, CSS3, JavaScript (Vanilla)
- **ML Libraries**: scikit-learn, XGBoost, pandas, numpy
- **Visualization**: Chart.js for interactive charts
- **Styling**: Custom CSS with Poppins font

## 🚀 Setup Instructions

### Prerequisites
- Python 3.10 or higher
- pip package manager
- Modern web browser

### Backend Setup

1. **Clone the repository**
```bash
git clone <repository-url>
cd AI-Analytics-Dashboard
```

2. **Navigate to backend directory**
```bash
cd backend
```

3. **Create and activate virtual environment**
```bash
python -m venv venv
source venv/bin/activate  # On Windows: venv\Scripts\activate
```

4. **Install dependencies**
```bash
pip install -r req.txt
```

5. **Train the models** (if not already trained)
```bash
python churn-model.py
python recommendatrion-model.py
```

6. **Start the Flask server**
```bash
python app.py
```
The backend will run on `http://127.0.0.1:5000`

### Frontend Setup

1. **Navigate to frontend directory**
```bash
cd frontend
```

2. **Open with serve locally by opening your index.html file**
  

## 📁 Project Structure

```
AI-Analytics-Dashboard/
├── backend/
│   ├── app.py                 # Main Flask application
│   ├── churn-model.py         # Churn prediction model training
│   ├── recommendatrion-model.py # Product recommendation model training
│   ├── forcast_model.py       # Sales forecasting model
│   ├── req.txt               # Python dependencies
│   ├── uploads/              # File upload directory
│   └── venv/                 # Virtual environment
├── frontend/
│   ├── index.html            # Main dashboard
│   ├── css/main.css          # Global styles
│   ├── churn/
│   │   └── result.html       # Churn prediction interface
│   ├── forcast/frontend/
│   │   ├── index.html        # Sales forecast interface
│   │   └── scripts.js        # Forecast functionality
│   └── product-recommend/frontend/
│       ├── index.html        # Product recommendation interface
│       └── script.js         # Recommendation functionality
└── README.md
```

## 🔧 API Endpoints

- `GET /` - Health check
- `POST /predict-churn` - Customer churn prediction
- `GET /metrics` - Churn metrics from dataset
- `POST /predict-file` - Sales forecasting with file upload
- `POST /predict-product` - Product recommendation

## 📊 Usage

1. **Dashboard**: Navigate through different AI tools from the main dashboard
2. **Churn Prediction**: Input customer data to get churn probability
3. **Sales Forecast**: Upload CSV file to get sales predictions and visualizations
4. **Product Recommendations**: Fill customer preferences to get product suggestions


## 📄 License

This project is powered by Advanced ML Models.

---
*© 2024 AI Analytics Dashboard. Developed by Ammad*
