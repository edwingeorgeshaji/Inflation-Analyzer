# Cost of Living Analytics – AI-Powered Forecast Platform

### Infosys Springboard Virtual Internship 6.0 – Milestone 1

---

## Overview

The **Cost of Living Analytics** project is an AI-powered forecasting web application designed to predict India’s **Cost of Living Index (CPI)** for both rural and urban sectors. Built using **TensorFlow**, **Keras**, and **Streamlit**, the platform transforms historical CPI data into meaningful insights, enabling users to analyze past trends and forecast future cost of living values.

The web application emphasizes interactivity, responsiveness, and professional design while offering data visualization, forecasting, and statistical insights through a unified interface.

---

## Key Features

### Dual Index Forecasting

* Predicts both **Rural** and **Urban** CPI values independently.
* Enables a deeper understanding of sector-specific economic variations.

### Real-Time Forecasting

* Allows users to select any year and month to generate instant CPI forecasts.
* Displays results using **Plotly** gauge charts for clarity and ease of interpretation.

### Historical vs. Predicted Trends

* Visualizes real historical CPI data alongside model-generated forecasts.
* Uses solid lines for actual data and dotted lines for predictions to ensure clear differentiation.

### Statistical Summary

* Provides minimum and maximum CPI values for selected indices.
* Users can filter and compare statistics through an interactive selection panel.

### Modern User Interface

* Built using **Streamlit** with a clean glassmorphism aesthetic.
* Offers light and dark mode themes for improved accessibility and user comfort.

### Optimized Performance

* Uses Streamlit’s caching mechanisms to reduce load times and enhance performance.

### Contextual Definitions

* Includes expandable information sections that explain CPI, index meanings, and forecasting methodology for better user understanding.

---

## System Architecture

### 1. Offline Training Pipeline

* Implemented using **Python** and **Jupyter Notebook**.
* Preprocessing includes:

  * Handling missing values.
  * One-hot encoding for sector data (Rural/Urban).
  * Feature scaling using **StandardScaler**.
* Model trained using a deep neural network with the following structure:

  ```python
  Dense(64, activation='relu')
  Dense(32, activation='relu')
  Dense(1)
  ```
* Evaluation Metrics:

  * Mean Squared Error (MSE)
  * Mean Absolute Error (MAE)
* The trained model is exported as `cost_of_living_model.keras` for deployment.

### 2. Online Inference Application

* Developed in **Streamlit** using the trained deep learning model.
* Loads both the model and dataset once using caching for efficiency.
* Users select a target year and month, and the application predicts CPI for rural and urban sectors.
* Forecasts and historical data are combined and visualized interactively through:

  * Gauge charts for real-time predictions.
  * Line plots for historical and forecasted trends.
  * Metric cards for summary statistics.

---

## Tools and Technologies

| Category             | Tool/Library | Version | Purpose                        |
| -------------------- | ------------ | ------- | ------------------------------ |
| Programming Language | Python       | 3.11+   | Core development               |
| Machine Learning     | TensorFlow   | 2.20.0  | Deep learning framework        |
|                      | Keras        | 3.11.3  | High-level neural network API  |
| Data Science         | Pandas       | 2.3.3   | Data manipulation and analysis |
|                      | NumPy        | 2.3.4   | Numerical computations         |
|                      | Scikit-learn | 1.7.2   | Preprocessing and scaling      |
| Visualization        | Plotly       | 6.3.1   | Interactive charts and gauges  |
| Web Application      | Streamlit    | 1.50.0  | Frontend framework             |

---

## Results

* The trained neural network achieved:

  * **Mean Squared Error (MSE): 2.90**
  * **Mean Absolute Error (MAE): 1.26**
* Demonstrates high accuracy and generalization capability.
* The Streamlit dashboard successfully integrates predictive analytics with interactive visualizations for accessible interpretation.

---

## Future Enhancements

* **Live Data Integration:** Replace static CSV data with live CPI feeds.
* **Macroeconomic Variables:** Include additional indicators such as inflation, GDP growth, and exchange rates.
* **Advanced Models:** Experiment with LSTM or GRU architectures for better temporal prediction.
* **Database Support:** Store user interactions and prediction logs for long-term analytics.
* **User Personalization:** Add authentication, saved forecasts, and alert notifications.

---

## Conclusion

The **Cost of Living Analytics** platform demonstrates an end-to-end data science implementation - from data preprocessing and neural network training to web deployment. The project bridges AI and economics, showcasing how predictive modeling can provide practical insights for decision-making.

As part of **Infosys Springboard Virtual Internship 6.0 (Milestone 1)**, this project lays a strong foundation for future enhancements, focusing on real-world scalability, automation, and advanced forecasting models.
