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
