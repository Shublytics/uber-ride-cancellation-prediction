# Uber Ride Cancellation Prediction

## 🎯 Objective
Build a machine learning model to predict whether a customer will cancel a ride before it begins, using only booking metadata available at the time of booking. The goal is to help optimize driver dispatch efficiency by proactively identifying high-risk cancellations.

## 📊 Dataset
The dataset contains ride booking information including:
- Booking details (ID, status, datetime)
- Customer information
- Vehicle type
- Location details (pickup/drop)
- Timing metrics (VTAT - Vehicle Time of Arrival, CTAT - Customer Time of Arrival)
- Rating and payment information

## 🛠️ Tech Stack
- Python 3.x
- Key Libraries:
  - pandas & numpy: Data manipulation
  - scikit-learn: Machine learning models
  - xgboost: Gradient boosting
  - matplotlib & seaborn: Visualization

## 📝 Project Structure

### 1. Data Preprocessing
- Standardized column names
- Handled missing values
- Combined date-time features
- Created derived features (is_weekend, hour, etc.)

### 2. Feature Engineering
- Time-based features (peak hours, weekday/weekend)
- Location-based encoding
- Customer booking patterns
- Categorical variable encoding

### 3. Model Development
Three models were evaluated:
- Logistic Regression
- Random Forest
- XGBoost (Best performing)

### 4. Model Performance

| Model                | Accuracy | ROC-AUC | Precision (Class 1) | Recall (Class 1) | F1-Score (Class 1) |
|---------------------|----------|---------|-------------------|----------------|------------------|
| Logistic Regression | 0.9648   | 0.9477  | 0.989             | 0.503          | 0.667            |
| Random Forest       | 0.9663   | 0.9483  | 0.980             | 0.528          | 0.690            |
| XGBoost (Best)      | 0.8640   | 0.9556  | 0.325             | 0.870          | 0.473            |

## 🔍 Key Findings
1. High VTAT (Vehicle Arrival Time) strongly correlates with cancellations
2. Peak cancellation hours: 23:00 and 15:00
3. Certain locations show higher cancellation rates
4. Payment method influences cancellation likelihood

## 💡 Recommendations
1. **Driver Rebalancing**: Focus on high VTAT areas
2. **Dynamic Dispatching**: Proactive driver allocation
3. **Customer Communication**: Early notifications for high-risk bookings
4. **Continuous Monitoring**: Track VTAT and cancellation trends

## 🚀 Future Improvements
- Incorporate distance calculations between locations
- Add real-time traffic data
- Include weather conditions
- Consider special events impact

## 📄 License
[MIT License](LICENSE)

## 👥 Author
Shubham Malhotra