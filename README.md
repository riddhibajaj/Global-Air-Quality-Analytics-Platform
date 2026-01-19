# Global Air Quality Analytics Platform

This project delivers an end-to-end **data analytics and data modeling solution** for analyzing global air quality patterns, pollution drivers, and population exposure risk. It integrates heterogeneous datasets into a relational data model and applies exploratory, diagnostic, and comparative analytics to generate actionable insights through interactive visualizations.

The work emphasizes **data integration, schema design, analytical reasoning, and visualization**, rather than prediction or machine learning.

## Problem Statement

Global air quality data is widely available, but it often lacks context around why pollution occurs, who is most affected, and how local experiences align with official measurements.

Key challenges addressed:
* Disconnected pollution, socioeconomic, and field report data
* Limited ability to validate citizen complaints with scientific metrics
* Difficulty prioritizing high-risk regions and pollutants
* Slow, manual reporting processes

This project addresses these gaps through data integration, analytics, and visualization.

## Data Sources

### Air Pollution Measurements
* City-level AQI and pollutant readings
* Pollutants include PM2.5, NO₂, CO, and Ozone
* Supports spatial and comparative analysis

### Socioeconomic and Demographic Indicators
* Population, GDP per capita, literacy rate
* Birth and death rates
* Economic sector composition

### Field Observation Data
* Structured reports capturing visibility, odor, severity, suspected source, and health impact
* Provides qualitative validation for quantitative metrics

## Data Modeling

A **relational data model** was designed to support scalable analytics and ensure data consistency.

Key characteristics:
* Country-level data serves as the master reference entity
* One-to-many relationships between countries and cities
* One-to-many relationships between countries and field observations
* Enforced primary and foreign keys to maintain referential integrity
* Supports temporal and geographic expansion

Core tables:
* `CountriesOfWorld` (master reference)
* `GlobalAirPollution` (city-level measurements)
* `FieldReport` (human observations)

The model enables efficient joins, cross-dataset validation, and population-level aggregation.

## Analytical Approach

* Exploratory Data Analysis (EDA)
* Descriptive and diagnostic analytics
* Cross-variable comparison and correlation analysis
* Population exposure risk assessment
* Integration of qualitative and quantitative signals

### AQI Severity Metric

The analysis uses the **90th percentile AQI (P90)** to represent sustained high-exposure pollution levels. This avoids underestimating risk through averages while preventing distortion from extreme outliers.

## Tools & Technologies

* **Excel**: Data cleaning, standardization, and preprocessing
* **Azure SQL Database**: Physical data model implementation and querying
* **Microsoft Forms + Power Automate**: Structured ingestion of field observations
* **Tableau**: Dashboards and analytical storytelling

## Visual Analytics

### Dashboard
A diagnostic view optimized for rapid analysis:
* Global AQI severity distribution
* Regional pollution hotspots
* Dominant pollutants by country
* Population exposure risk
* Alignment between AQI data and field observations

Dashboard
[https://public.tableau.com/app/profile/riddhi.bajaj5141/viz/bajaj_riddhi_5/Dashboard?publish=yes](https://public.tableau.com/app/profile/riddhi.bajaj5141/viz/bajaj_riddhi_5/Dashboard?publish=yes)

### Storyboard
A multi-step analytical narrative:
* Global and regional AQI patterns
* Socioeconomic and demographic drivers
* Population density and exposure analysis
* Outlier and benchmark identification
* Validation of qualitative reports against measured data

Storyboard
[https://public.tableau.com/app/profile/riddhi.bajaj5141/viz/bajaj_riddhi_5/Storyboard?publish=yes](https://public.tableau.com/app/profile/riddhi.bajaj5141/viz/bajaj_riddhi_5/Storyboard?publish=yes)

## Key Insights
* Roughly **40% of countries** experience unhealthy air quality
* Severe pollution is concentrated in **Asia, the Near East, and parts of Africa**
* **PM2.5** is the dominant driver of extreme AQI values
* Economic and literacy indicators alone do not guarantee cleaner air
* High population density significantly amplifies exposure risk
* Qualitative field reports align closely with measured AQI in high-risk regions

## Limitations

* Uneven geographic coverage of monitoring stations
* Limited temporal depth and seasonal representation
* Subjectivity in human-reported observations
* Aggregated country-level indicators mask local variation
* Findings reflect correlation rather than causation

## License
MIT License © 2025 Riddhi Bajaj
