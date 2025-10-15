# ![CI logo](https://codeinstitute.s3.amazonaws.com/fullstack/ci_logo_small.png)

## Air Pollution Forecasting & Analysis Project

The Air Pollution Forecasting & Analysis Project applies data-driven methods to understand and predict air quality across the United States. Using publicly available environmental and meteorological datasets, the project explores how pollutants such as nitrogen dioxide (NO₂), ozone (O₃), and sulphur dioxide (SO2) vary over time and between regions.

By integrating geographic coordinates, weather conditions, populations and pollutant measurements, the project identifies key relationships influencing daily air quality. Statistical analysis, data visualization, and predictive modeling are used to uncover temporal patterns, assess spatial trends, and estimate future pollutant levels.

The overall goal is to build an interpretable framework that supports informed environmental decision-making and highlights pollution hotspots. Through statistical analysis, machine learning, and clear data visualization, the project delivers interpretable forecasts and insights that can support citizens, health professionals, and policymakers with data-driven forecasts, that aims to reduce exposure risks, guide preventive measures, and contribute to healthier, more resilient communities.

## Dataset Content

- Source: https://www.kaggle.com/datasets/sogun3/uspollution/data?select=pollution_us_2000_2016.csv
- Timeframe: 2000–2016 (filtered to 2011–2016)
- Geography: United States (by city/county/state)
- Features:
   •	Pollutants: NO₂, O₃, SO₂, CO (daily values + AQI)
   •	Location: State, county, city, site number
   •	Population (added from external dataset)
   •  Weather (Installed Meteostat and libraries in VS Code)
- Note: Raw dataset exceeds 300MB and is excluded from the repo (see .gitignore).
________________________________________
 
## Business Requirements

- This project aims to support public health and environmental decision-making by answering:
   •	Which locations consistently exceed safe pollution levels?
   •	How do weather conditions and population affect air quality?
   •	Can we forecast AQI to enable preventative measures (e.g., air quality alerts)?
________________________________________
 
## Hypotheses & Validation

- Hypothesis & Validation Method:
  - H1: Higher population areas have worse air quality	
  - Validation: Correlation analysis, scatter plots (population vs AQI)
  
  - H2: Weather conditions (e.g., wind speed) affect pollutant levels	
  - Validation: Multivariate regression
  
  - H3: Pollution levels follow seasonal patterns	
  - Validation: Time series decomposition
  
  - H4: Forecasting models can predict pollutant levels accurately 1 week in advance	
  - Validation: RMSE/MAE from model validation

## Project Plan

1.	Data Cleaning
   • Handle missing values (e.g., AQI NaNs)
   • Optimize data types (e.g., downcasting floats and removing whitespaces)

2.	Feature Engineering
   • Add population from US Census, mapped from city level data first, then county levl if city is not application or available 
   • Weather data: maximum temperature (tmax), wind speed (wspd) and precipitation (prcp) 

3.	EDA
   • Trends, heatmaps, correlations

4.	Modeling
   • Baseline (ARIMA) and advanced (XGBoost/LSTM) models

5.	Dashboard
   • Interactive dashboard with filters by pollutant, location, and date

6.	Documentation & Ethical Review
   • ?????????

________________________________________
5. Mapping Business Requirements to Visuals

| Requirement	                        |                         Visual                     |
---------------------------------------------------------------------------------------------
| Identify high-risk areas	            |             Choropleth map of AQI by region        |
| Compare pollutants over time	      |             Line charts with rolling averages      |
| Understand weather impact	         |             Scatter plots & regression overlays    | 
| Detect seasonal trends	            |             Time series decomposition              | 
| Forecast accuracy	                  |             Prediction vs actual plots             |


6. Analysis Techniques Used
  • EDA: Heatmaps, boxplots, trend lines
  • Statistical Tests: Pearson correlation, ADF test
  • Time Series Modeling: ARIMA, SARIMA
  • Machine Learning: Random Forest, XGBoost
  • Feature Engineering: Weather and Population Data
  • Dashboarding: Streamlit (planned)
________________________________________
 

7. Ethical Considerations
  • Bias: Ensure fair analysis across rural and urban areas
  • Transparency: Clearly communicate data limitations and assumptions
  • Privacy: No personal data used — only aggregate, public data
  • Policy Sensitivity: Avoid drawing misleading conclusions about causation without strong evidence


8. Dashboard Design

- Tool: Power BI
- Features:
  • Select pollutant, city, and date range
  • View pollution trends and forecasts
  • Toggle weather overlays
  • Map of pollution hotspots
  • Downloadable charts for reports

- Tool: Streamlit
- Features:
  • Select pollutant, city, and date range
  • View pollution trends and forecasts
  • Toggle weather overlays
  • Map of pollution hotspots
  • Downloadable charts for reports
- Status: In development 


