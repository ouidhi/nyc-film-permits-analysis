# NYC Film Permits Analysis

## Overview


## Business Question(s)
which boroughs are most popular for filming?

which categories of film are most shot in new york/

which categores of film are shot in the most popular borough vice-versa for least popular

how long are the events typically? any outliers (boroughs, film categories, sub categories) using 
startdatetime adn enddatetime 

density of each borough on a map in regards to max events filmed.

how early are the events booked (request is submitted) before the start date?

### AIMS grid


## Tech Stack
- Excel
- Python
- PowerBI
- GitHub 


## Data Sources & Description

## Data Cleaning & Preparation

cleaned using ms excel and python pandas, numpy libraries

removes the parkingheld field, as it is not relevant to my analysis. 

removed eventagency column, no unique values. every event has the same value- Mayor's Office of Media & Entertainment.

converted multiple values in one row to multiple rows

created new col, where project origin (domestic (USA) or international)


## Dashboard Features

## Insights & Analysis

## Live Dashboard

## Challenges & Learnings

During the data cleaning process, some columns had multiple values seperated by commas which violates the 1NF (first normal form) which requires that each cell has single value. I had to seperate them appropriately in individual rows to perform accurate analysis. 

business objective
aims grid- purpose, stakeholders,
data preprocessing using excel 
data loading in SQL
tableau connected to SQL database for visualization
