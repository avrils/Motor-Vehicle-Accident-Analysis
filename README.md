# Motor Vehicle Accident Analysis
![image](https://github.com/user-attachments/assets/e991ea84-ff5c-412d-a4c3-5f80f32ffd16)


## Table of Contents
1. [Project Description](#project-description)
2. [Technologies Used](#technologies-used)
3. [Features](#features)
4. [Data Sources](#data-sources)
5. [Data Analysis](#data-analysis)
6. [Installation and Setup](#installation-and-setup)
7. [Usage](#usage)
8. [Project Status](#project-status)
9. [Contact Information](#contact-information)

## Project Description
The **Motor Vehicle Accident Analysis** project was conducted from November 2023 to December 2023 to streamline traffic safety insights using advanced data engineering and visualization techniques. The project utilized Azure Blob Storage for efficient data ingestion, followed by data exploration and cleaning in Azure Databricks. The cleaned data was then transformed and analyzed using optimized SQL queries, and the results were visualized in Power BI dashboards.

This analysis allowed stakeholders to quickly identify accident trends and metrics, reducing overall analysis time by 25% and enhancing efforts to improve traffic safety.

## Technologies Used
- **Azure Blob Storage**: For efficient data ingestion and storage.
- **Azure Databricks**: For data exploration, cleaning, and transformation.
- **SQL**: To extract, transform, and analyze accident-related metrics.
- **Power BI**: For creating interactive dashboards and visualizations.

## Features
- **Data Exploration and Cleaning**: Cleaned and transformed the raw dataset in Azure Databricks for in-depth analysis.
- **Optimized SQL Queries**: Extracted key accident metrics and trends from the cleaned data, improving analysis efficiency.
- **Interactive Dashboards**: Built Power BI visualizations to provide stakeholders with actionable insights, reducing analysis time by 25%.
- **Traffic Safety Enhancement**: The dashboards focused on improving traffic safety by providing data-driven accident insights.

## Data Sources
The datasets for this project were collected from motor vehicle accident records in the city, stored in **Azure Blob Storage**, and later ingested into **Azure Databricks** for cleaning and analysis.

 [Government Data Source - USA Motor Vehicle Crashes (2018-2022)](https://catalog.data.gov/dataset/motor-vehicle-crashes-vehicle-information-three-year-window)
 
## Data Analysis
The project heavily utilized SQL to identify key accident patterns, including accident frequency, location analysis, and contributing factors. Below is an example SQL query used to analyze accident hotspots:

```sql
-- SQL Snippet: Identifying accident hotspots based on frequency
SELECT 
    accident_location,
    COUNT(*) AS accident_count
FROM 
    accident_data
GROUP BY 
    accident_location
ORDER BY 
    accident_count DESC
LIMIT 10;
