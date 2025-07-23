# Road-Accident-Dashboard
In this Dashboard, I've created a comprehensive view of road accidents for the years 2019 to 2022. The objective was to provide valuable insights to clients and shed light on accident trends.

# About the project:
* I used Excel for data cleaning to help strengthen my command of the fundamental spreadsheet tool.
* This dashboard displays the yearly cumulative number of accidents that occurred in the UK region. The dashboard can be filtered by year and accident severity, and it can make value comparisons between the previous and current years.
* It also displays the number of casualties by vehicle or road category. Weather conditions and road surfaces are also used to locate fatalities of varying severity.
* The orginal dataset consisted of 27 fields out of which only 14 of them are utilized for this use case
* The visual representation of the Fatal severity for the year 2022 is displayed below. The comparison could be drawn for any year between 2019 to 2022.

🔍Data Gathering & Cleaning: I imported the CSV file and performed various activities such as applying filters, removing duplicates, fixing errors, and transforming the data into an easily analyzable format. The data includes information about accidents, such as the number of vehicles involved, severity of the accident, and the location and time of the accident.

🔄 Data Processing: Creating some new columns that involved organizing, sorting, and filtering the data to extract meaningful insights.

📊 Data Analysis: Used various statistical methods to get valuable insights from the data.

📈 Data Visualization: Used Excel as a visualization tool. With the help of this, I have created attractive charts, graphs, and interactive visuals to present the data in an easy way.

🔄 Dashboard Making: Finally, I built a dashboard in Excel by inserting slicers and timelines that allow users to interact with the data.

# Introduction:
* This project is aimed at developing a tableau Dashboard for generating insights about road accident data in the United Kingdom.

# Dashboard Requirements:
* Primary KPI's - Total Casualties and Total Accident values for Current Year and YoY Growth
* Primary KPI's - Total Casualties by Accident Severity for Current Year and YoY Growth
* Secondary KPI's - Total Casualties with respect to Vehicle Type for Current Year
* Monthly Trend showing comparison of Casualties for Current Year and Previous Year
* Casualties by Road Type for Current Year
* Current Year Casualties by Area/Location & Day/Night
* Total Casualties and Total Accident by Location

# About the Dataset:
* This dataset is specifically of UK region obatined from Kaggle
* It has over half a million records collected over the time period 2019-2022.

# Installation / Usage:
* Install Tableau Desktop from Official Webiste.
* Download data files from link given in Introduction.
* Clone/download this repository to your local machine.
* Open Dashboard report file (Road Accidents Dashboard.twbx) in tableau Desktop, to access the dashboard's interactivity.

# DAX Formulas Used in Measures:
### 1. Total Casualties For Current Year and Year on Year Growth
(a) Current Year To Date Casualties -- CY Casualties Measure
* CY Casualties = TOTALYTD(SUM(Data[Number_of_Casualties]), 'Calendar'[Date])

(b) Previous Year Casualties -- PY Casualties Measure
* PY Casualties = CALCULATE(SUM(Data[Number_of_Casualties]), SAMEPERIODLASTYEAR('Calendar'[Date]))

(c) Year on Year Growth of Casualties - YoY Casualties Measure
* YoY Casualties = ([CY Casualties] - [PY Casualties])/[PY Casualties]

### 2. Total Accidents for Current Year and Year on Year Growth
(a) Current Year Accidents Count -- CY Accidents Count Measure
* CY Accidents Count = TOTALYTD(COUNT(Data[Accident_Index]), 'Calendar'[Date])

(b) Previous Year Accidents Count -- PY Accidents Count Measure
* PY Accidents Count = CALCULATE(COUNT(Data[Accident_Index]), SAMEPERIODLASTYEAR('Calendar'[Date]))

(c) Year on Year Growth of Accidents - YoY Accidents Measure
* YoY Accidents = ([CY Accidents Count]-[PY Accidents Count])/[PY Accidents Count]
