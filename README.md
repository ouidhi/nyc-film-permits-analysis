# NYC Film Permits Analysis

## Overview

New York City is a global hub for film and television production, but how exactly is its space and time used by the industry? This project analyzes publicly available film permit data to explore filming activity across NYC boroughs. Using Power BI, the dashboard uncovers patterns in filming locations, categories, durations, and daily timing. The goal is to visualize the scale and distribution of productions and provide insights valuable for city planners, production teams, and local businesses.

## Problem Statement

This project explores filming trends across New York City to understand where and what type of content is most commonly shot. It looks at popular boroughs, common film categories, typical event durations, and time-of-day patterns. The goal is to uncover location preferences and production behaviors that can inform planning and logistics.

-------- CHANGE AFTER FINAL RESULTS !!!!!!--------

I initially expected Manhattan to dominate the data, given how often it’s featured in shows and movies — but the analysis helped validate **or** challenge those assumptions with real numbers. 

### AIMS grid


## Tech Stack

- Python
- Jupyter Notebook (VS code)
- PowerBI
- GitHub 

## Data Sources & Description

The data is collected from [data.gov - City of New York | Film Permits](https://catalog.data.gov/dataset/film-permits) and maintained by [NYC Open Data](https://data.cityofnewyork.us/City-Government/Film-Permits/tg4x-b46p/about_data).



## Data Cleaning & Preparation

cleaned using python pandas, numpy libraries

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
