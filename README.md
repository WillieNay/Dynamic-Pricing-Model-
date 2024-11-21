# Dynamic Pricing and Predictive Modeling for Ride-Sharing

This project focuses on analyzing ride-sharing data, implementing a dynamic pricing strategy, and training a machine learning model to predict ride costs based on various factors such as demand, supply, vehicle type, and time of booking.

---

## Features

### 1. Data Analysis and Visualization
- **Scatter Plot**: Analyzes the relationship between expected ride duration and historical ride cost.
- **Box Plot**: Shows the distribution of historical ride costs by vehicle type and time of booking.
- **Donut Chart**: Visualizes the proportion of profitable and loss-making rides under the dynamic pricing strategy.

### 2. Dynamic Pricing Strategy
- Calculates adjusted ride costs based on:
  - **Demand Multiplier**: Based on the number of riders.
  - **Supply Multiplier**: Based on the number of drivers.
- Identifies profitable and loss-making rides based on the adjusted pricing.

### 3. Predictive Modeling
- Implements a **Random Forest Regressor** to predict ride costs using features such as:
  - Number of riders.
  - Number of drivers.
  - Vehicle type.
  - Time of booking.
  - Expected ride duration.
- Provides real-time ride cost prediction based on user inputs.

### 4. Model Evaluation
- Compares actual and predicted ride costs.
- Visualizes the comparison with a scatter plot showing actual vs. predicted values and an ideal line.

---

## Directory Structure
**dynamic_pricing.csv**: Input dataset for analysis and model training.
**main.py**: Core script for data analysis, dynamic pricing, and predictive modeling.
**Visualizations**: Generated dynamically during runtime.

---

## Outputs

**Visualizations**
Scatter Plot: Expected ride duration vs. ride cost.
Box Plots: Ride cost distribution by vehicle type.
Ride cost distribution by time of booking.
Donut Chart: Profitability of rides under dynamic pricing.
Scatter Plot: Actual vs. predicted ride costs.

## Model Evaluation
R² score to evaluate the model's predictive performance.

## Predictions
Predicted ride cost for custom user input.

## Key Functions

**Dynamic Pricing Calculation**:
Calculates demand and supply multipliers based on percentiles.
Adjusts ride costs dynamically.

**Data Preprocessing**: Handles missing values.
Detects and handles outliers using the Interquartile Range (IQR).
Encodes categorical features numerically.

**Predictive Modeling**: Trains a Random Forest Regression model to predict adjusted ride costs.

**Custom Predictions**: Predicts ride costs based on user inputs like vehicle type, time of booking, and demand/supply conditions.

---

# Example input
user_number_of_riders = 65
user_number_of_drivers = 30
user_vehicle_type = "Economy"
user_time_of_booking = "Afternoon"
expected_ride_duration = 50

# Predict ride cost
predicted_price = predict_price(user_number_of_riders, user_number_of_drivers, user_vehicle_type, user_time_of_booking, expected_ride_duration)
print("Predicted Ride Cost:", predicted_price)

---

## Dataset Details

**The dataset dynamic_pricing.csv contains the following features**:
Expected_Ride_Duration: Duration of the ride (in minutes).
Historical_Cost_of_Ride: Cost of the ride (historical).
Number_of_Riders: Number of riders requesting rides.
Number_of_Drivers: Number of drivers available.
Vehicle_Type: Type of vehicle (Economy or Premium).
Time_of_Booking: Time when the booking was made (Morning, Afternoon, Evening, Night).

