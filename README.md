# **Weather and Air Quality Analysis: Predicting Air Pollution from Weather Patterns**

## **Project Overview**

This project analyzes the relationship between meteorological conditions and air quality in major U.S. cities (New York, Los Angeles, Houston, Phoenix, and Denver). The goal is to develop a model that can predict air pollution levels (specifically PM2.5 concentrations) based on weather patterns.

The project began with a classification approach to predict air quality categories but pivoted to a more robust time series forecasting model to predict the next day's PM2.5 levels.

## **Data Sources**

* **Weather Data:** Sourced from the [OpenMeteo API](https://open-meteo.com/), providing daily metrics such as temperature, humidity, wind speed, precipitation, and surface pressure.  
* **Air Quality Data:** Sourced from the [U.S. Environmental Protection Agency (EPA) Air Quality System (AQS) API](https://aqs.epa.gov/aqsweb/documents/data_api.html), providing daily PM2.5 concentration data.

## **Methodology**

1. **Data Collection & Cleaning:** Fetched and merged data from the two APIs for the five selected cities.  
2. **Exploratory Data Analysis (EDA):** Analyzed the relationships between weather variables and PM2.5 levels using correlation heatmaps.  
3. **Initial Classification:** Developed Random Forest and Logistic Regression models to classify air quality. This approach was limited by significant class imbalance in the dataset.  
4. **Time Series Forecasting:** Engineered new features (e.g., lag features, rolling means) and developed a Random Forest Regressor to forecast the next day's PM2.5 value for Denver.  
5. **Visualization:** Created a geographic map using Folium to visualize the average PM2.5 levels across the cities.

## **Getting Started**

### **Prerequisites**

* Python 3.8+  
* pip

### **Installation**

1. **Clone the repository:**  
   git clone \[https://github.com/your-username/weather-air-quality-analysis.git\](https://github.com/your-username/weather-air-quality-analysis.git)  
   cd weather-air-quality-analysis

2. **Create and activate a virtual environment (recommended):**  
   python \-m venv venv  
   source venv/bin/activate  \# On Windows, use \`venv\\Scripts\\activate\`

3. **Install the required packages:**  
   pip install \-r requirements.txt

### **Usage**

To run the analysis, execute the main Python script:

python analysis.py

You can also explore the project's development and detailed outputs in the Data\_Science\_Practicum.ipynb notebook.