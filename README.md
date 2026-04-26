# London Public Transport (TfL) Journeys Analysis

## Project Overview
This project analyzes the volume of public transport journeys in London across different transport methods. Using a dataset provided by the Mayor of London's office and hosted on Google BigQuery, the analysis explores passenger trends to understand transport popularity, historical peaks, and the impact of external events on ridership.

This project was developed as a SQL-focused Data Analytics assessment.

## Business Objective
The goal of this analysis is to extract insights from historical transport data to answer key operational questions:
* Which transport types handle the highest volume of passengers?
* What were the historical peaks in ridership for niche transport methods (e.g., Emirates Airline cable car)?
* How did external factors (like the COVID-19 pandemic) impact the usage of the London Underground?

## Data Source
* **Provider:** Transport for London (TfL) / Greater London Authority.
* **Database:** Google BigQuery.
* **Table:** `TFL.JOURNEYS`
* **Features:** Reporting dates, months, years, days in the month, journey types, and total journeys measured in millions.

## Tech Stack
* **Language:** SQL (Google BigQuery dialect)
* **Environment:** Jupyter Notebook 
* **Key SQL Concepts Demonstrated:** Data Aggregation (`SUM`), Grouping (`GROUP BY`), Sorting (`ORDER BY`), Data Filtering (`WHERE`), Math Functions (`ROUND`), Limit constraints (`LIMIT`).

## Queries and Methodology
The analysis was broken down into three targeted SQL queries:
1. **Overall Transport Popularity:** Aggregated total journeys across all available years to rank transport methods by overall usage.
2. **Niche Transport Peak Usage:** Filtered the data specifically for the "Emirates Airline" cable car, grouping by month and year to find the top 5 periods of highest usage.
3. **Pandemic Impact on Major Networks:** Filtered for "Underground & DLR" and sorted the aggregated yearly volume in ascending order to identify the years with the lowest ridership.

## Key Findings
* **Buses Drive London:** Despite the global fame of the "Tube", buses are the most utilized transport method in London (24.9 billion journeys in the dataset), significantly outperforming the Underground & DLR (15.0 billion journeys).
* **Event-Driven Spikes:** The Emirates Airline cable car saw its absolute peak usage in May, June, and April of 2012. This strongly correlates with the build-up and execution of the 2012 London Olympics.
* **COVID-19 Impact:** The data clearly illustrates the severe impact of the pandemic lockdowns. The years 2020 and 2021 recorded the lowest ridership for the Underground & DLR in the entire dataset, with 2020 seeing only 310 million journeys compared to pre-pandemic averages of over 1 billion.

## How to Run This Project
1. Clone this repository.
2. Open the `notebook.ipynb` file in Jupyter Notebook, JupyterLab, or Google Colab.
3. Ensure you have the appropriate BigQuery integration configured if you wish to re-run the queries directly against the live database.
