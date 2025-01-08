# COVID-19 pandemic for the US Analysis
[![LinkedIn](https://img.shields.io/badge/-LinkedIn-black.svg?style=for-the-badge&logo=linkedin&colorB=555)](https://www.linkedin.com/in/yufang-w-1295881b5/) [![GitHub](https://img.shields.io/badge/GitHub-100000?style=for-the-badge&logo=github&logoColor=white&colorB=555)](https://github.com/Yufanggg) <img alt="GitHub" src="https://img.shields.io/github/license/bopith/UnicornCompanies?style=for-the-badge"> 

## Overview
This repository contains the ETL (Extract, Transform and load) data into a SQL database SQL queries and the slide presentation for the analytical project on COVID-19 pandemic for the US Analysis

This project aims at exploring the answers to the following questions:
1. How have the positive and negative COVID-19 cases trended over time? Are there any noticeable spikes or drops in the number of positive or negative cases?
2. How have the numbers of currently hospitalized and ICU patients changed over time? What are the trends in cumulative hospitalizations and ICU admissions?
3. How has the number of patients currently on ventilators changed over time? What are the trends in cumulative ventilator usage?
4. How have the number of deaths and death increases trended over time? Are there any significant periods with higher death rates?
5. How have the total test results and test result increases trended over time? Are there any correlations between testing increases and positive case increases?
6. How do different states compare in terms of positive cases, hospitalizations, ICU admissions, and deaths?
Are there any states that consistently show higher or lower numbers across these metrics?
7. How have the number of pending cases changed over time? Are there any correlations between pending cases and other metrics like positive cases or hospitalizations?
8. How complete is the data for each metric? Are there any metrics with significant amounts of missing data?
How might missing data impact the analysis and conclusions?

## Table of Contents

- [Requirements](#requirements)
- [Installation](#installation)
- [Usage](#usage)
- [Project Structure](#project-structure)

## Requirments
To run this Project, you will need the following:
- Python (> 3.6)
- Pandas (pip install pandas)
- Requests (pip install requests)
- SQLAlchemy (pip install sqlalchemy)

## Installation

1. Clone the repository to local machine:
   ```
   git clone https://github.com/Yufanggg/USCovid_tracking_analysis.git    
   ```

2. Navigate to the project directory:
   ```
   cd 
   ```

3. Intsall the required Python packages:
   ```
   pip install -r requires.txt
   ```



## Data

The dataset used in this analysis contains records of daily data on the COVID-19 pandemic for the US and individual states obtained from [The COVID Tracking Project](https://covidtracking.com/). <br />

Information on the dataset include:
- `date` : *integer*, Date on which data was collected by The COVID Tracking Project.
- `death` : *integer* (*null* if no data is available), Deaths (confirmed and probable). 
- `deathIncrease` : *integer* (*null* if no data is available), Daily increase in death, calculated from the previous day’s value.
- `hospitalized` : *integer* (*null* if no data is available), Old label for `hospitalizedCumulative`.
- `hospitalizedCumulative` : *integer* (*null* if no data is available), Cumulative hospitalized/Ever hospitalized.
 - `hospitalizedCurrently` : *integer* (*null* if no data is available), Currently hospitalized/Now hospitalized. 
- `inIcuCumulative`:  *integer* (*null* if no data is available), Cumulative in ICU/Ever in ICU. 
- `inIcuCurrently` :  *integer* (*null* if no data is available), Currently in ICU/Now in ICU. 
- `lastModified` : *string*, Deprecated. Old label for lastUpdateET.
- `negative` : *integer* (*null* if no data is available), Negative PCR tests (people). 
- `negativeIncrease` : *integer* (*null* if no data is available), Increase in negative computed by subtracting the value of negative for the previous day from the value for negative from the current day.
- `onVentilatorCumulative` : *integer* (*null* if no data is available), Cumulative on ventilator/Ever on ventilator. 
- `onVentilatorCurrently` : *integer* (*null* if no data is available), Currently on ventilator/Now on ventilator. 
- `pending` : *integer* (*null* if no data is available), Pending. Total number of viral tests that have not been completed as reported by the state or territory.
- `posNeg` : *integer* (*null* if no data is available), Deprecated. Computed by adding positive and negative values.
- `positive` : *integer* (*null* if no data is available), Cases (confirmed plus probable). 
- `positiveIncrease` : *integer* (*null* if no data is available), New cases. 
- `recovered` :  *integer* (*null* if no data is available), Recovered. 
- `states` : *integer*, States. Only available in national records. The number of states and territories included in the US dataset for this day.
- `total` :  *integer* (*null* if no data is available), Deprecated. Computed by adding positive, negative, and pending values.
- `totalTestResults` :  *integer* (*null* if no data is available), Total test results. 
- `totalTestResultsIncrease` : *integer* (*null* if no data is available), New tests. Daily increase in totalTestResults, calculated from the previous day’s value. 


## SQL Queries

- `data_cleaning.sql`: a query for data cleaning
- `data_exploration.sql`: a query for data exploration
- `query_data_visualization.sql`: a query for data visualization in PowerBI


## Analytical Results

Brief findings of this project are:
1. Zapier has the biggest return on investment.
2. It usually takes about 6 years to become a unicorn.
3. Fintech industry has the most unicorns.
4. The United States has the most unicorns.
5. Accel has funded the most unicorns.

Please check `uc_covid_results.pdf` for more details and meaningful discussion on query outputs and analytical results.

Tableau Dashboard:
![Dashboard](/img/dashboard.png?raw=true)


## Acknowledgments
