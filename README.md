# Smart-City-Risk-Analysis-System

## Overview
This project implements a smart city monitoring system that collects and analyzes real-time environmental and traffic data.  
The system combines weather conditions, air pollution levels and traffic information in order to estimate potential risk levels within a city environment.

The solution performs automated data processing and classification using a clustering algorithm and distributes alerts through messaging systems.

---

## Features

- Real-time data collection from multiple APIs
- Integration of weather, air pollution and traffic datasets
- Dynamic risk classification using K-Means clustering
- Event-driven architecture
- Alert distribution through messaging brokers
- Data storage for historical analysis
- Dashboard visualization for monitoring system metrics

---

## Data Sources

The system collects data from the following external APIs:

- **OpenWeather API**
  - Temperature
  - Humidity
  - Pressure

- **OpenWeather Air Pollution API**
  - PM2.5
  - PM10
  - CO
  - NO2
  - O3

- **TomTom Traffic API**
  - Current traffic speed
  - Free flow speed
  - Travel time
  - Road closure information

---

## System Architecture

The system pipeline includes the following stages:

1. **Data Collection**
   - API requests retrieve weather, pollution and traffic data.

2. **Data Processing**
   - JSON responses are parsed and formatted.

3. **Data Integration**
   - Weather, air quality and traffic data are merged into a unified dataset.

4. **Data Storage**
   - Data is stored in CSV files for historical analysis.

5. **Risk Analysis**
   - A K-Means clustering algorithm classifies data points into:
     - Normal
     - Moderate
     - High Risk

6. **Alert Routing**
   - Alerts are distributed through messaging services based on risk level.

7. **Visualization**
   - Dashboard components display key metrics such as temperature, pollution and risk level.

---

## Technologies Used

- Node-RED
- JavaScript
- OpenWeather API
- TomTom Traffic API
- MQTT
- RabbitMQ
- CSV data storage
- K-Means clustering algorithm

---

## Messaging System

The system distributes alerts using routing topics:

| Risk Level | Routing Topic |
|-------------|--------------|
| High Risk | risk.high.broadcast |
| Moderate | risk.moderate.* |
| Normal | risk.normal.* |

Alerts can be consumed by different systems such as:

- municipal services
- traffic management systems
- public health systems
- mobile applications

---

## Example Output

Example risk classification:
Temperature: 34°C
PM2.5: 85
Traffic Speed: 10 km/h

Risk Level: High Risk


---

## Dashboard

The system provides a monitoring dashboard displaying:

- Temperature trends
- Air pollution levels
- Real-time risk classification

---

## Future Improvements

- Integration with additional smart city sensors
- Machine learning model optimization
- Database storage instead of CSV
- Web application for public visualization
- Predictive analytics for risk forecasting

---

## Author

Vasilis Nousis  
BSc Informatics & Telematics

