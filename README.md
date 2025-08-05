# NYC Film Permits Analysis

## Overview

New York City is a global hub for film and television production, but how exactly is its space and time used by the industry? This project analyzes publicly available film permit data to explore filming activity across NYC boroughs. Using Power BI, the dashboard uncovers patterns in filming locations, categories, durations, and daily timing. The goal is to visualize the scale and distribution of productions and provide insights valuable for city planners, production teams, and local businesses.

## Problem Statement

This project explores filming trends across New York City to understand where and what type of content is most commonly shot. It looks at popular boroughs, common film categories, typical event durations, and time-of-day patterns. The goal is to uncover location preferences and production behaviors that can inform planning and logistics.

I initially expected Manhattan to dominate the data, given how often it’s featured in shows and movies and the analysis helped validate those assumptions with real numbers. 

## Tech Stack

- Python
- Jupyter Notebook (VS code)
- PowerBI
- GitHub 

## Data Sources & Description

This project uses publicly available data from the data.gov, specifically the City of New York Open Data Portal. 

**Links:**
- [Data Dictionary]()
- [data.gov - City of New York | Film Permits](https://catalog.data.gov/dataset/film-permits)
- [NYC Open Data](https://data.cityofnewyork.us/City-Government/Film-Permits/tg4x-b46p/about_data)


## Data Cleaning & Preparation

The original dataset contained inconsistencies in formatting and data types. To ensure the data was analysis-ready, I performed the following preprocessing steps using Python libraries such as pandas and numpy:

- Cleaned and standardized the dataset using pandas and numpy for efficient data handling.
- Removed the parkingheld field as it was not relevant to the analysis.
- Dropped the eventagency column since it contained only a single repeated value: "Mayor's Office of Media & Entertainment".
- Split rows with multiple ZIP codes into separate rows to normalize the data structure.

## Dashboard Features


## Power Query DAX

- Removed rows with invalid ZIP code 00083.
- Removed one row with ZIP code 10048, which was retired following 9/11. The area formerly associated with this ZIP code (World Trade Center, Lower Manhattan) has since been redistributed under neighboring ZIP codes.
- Created multiple calculated columns and measures using DAX in Power BI to support more accurate visualizations and analysis.
- Used COUNT(DISTINCT) for event counting, as each eventID appears multiple times due to prior row-splitting (e.g., splitting multiple ZIP codes in one row into separate rows).
  
## Insights & Analysis

This analysis uncovers the temporal, spatial, and logistical patterns behind thousands of permitted events across New York City. 

### Temporal Behavior: When Does NYC Film?

- Filming starts early and fast: Event activity peaks sharply between 5–7 AM, then declines throughout the day. This suggests strict morning shoot schedules and potential city regulations influencing early-day setups.
- March is Hollywood's NYC month: The highest number of events occurs in March, aligning with pre-summer production ramps and permitting cycles. If you’re planning media operations or services, March is your high-traffic season.
- Permits are processed fast, but erratically: While the median permit lead time is 6 days, there are noticeable drops in months like March, July, and October, pointing to either streamlined approvals or backlog pressures. This irregularity could impact production teams relying on tight schedules.
- 2024 spikes in activity: The dataset reveals a surge in permits in 2024, potentially post-COVID rebound, new productions, or incentives. Planners can look to 2024 as a benchmark year for demand forecasting.
  
### Borough Dynamics: Manhattan Isn’t Just the Star, it’s the Set

- Manhattan dominates, not just in volume (6.2K+ events), but in event duration, averaging 25.56 hours, nearly double the borough average. This implies more complex, high-budget productions needing extended time for shoots and load-ins.
- Brooklyn’s rising presence: With 4K+ events and second-highest durations, Brooklyn is clearly a media hotspot — possibly due to its growing creative industry scene and availability of diverse urban settings.
- Queens, Bronx, and Staten Island = Low-volume, short-term: These boroughs host significantly fewer events, often lasting less than 17 hours. These may be niche shoots or administrative permitting rather than full-scale productions.

### Category & Event Type Trends: Who’s Shooting What?

- Television shoots lead by a mile: Nearly 45% of all permits are for television, indicating NYC’s continued dominance as a hub for serial content — think Netflix, HBO, and NBC shows. This insight can help vendors or service providers tailor offerings to TV crews.
- Theater and Film follow — but with a steeper drop-off: These categories, while still prominent, don’t come close to television in volume. That highlights the shift in production investments towards episodic content.
- Shooting permits overwhelm all other event types: 9.7K+ events were classified under this, dwarfing the next category (Theater Load-Ins at  2.4K). This confirms the logistics-heavy nature of NYC productions, requiring constant street coordination, security, and infrastructure support.
- Music videos, student films, and documentaries are rare: These are either underrepresented in the data or face challenges in accessing permits. This insight could be relevant for policy-making or funding support in the indie space.
  
### Parking Demand 

- The maximum number of streets held for parking during a single event was 24 — a signal of large-scale, resource-intensive shoots. Parking availability and neighborhood coordination remain critical bottlenecks in NYC's media logistics chain.


## Live Dashboard


## Challenges & Learnings

During the data cleaning process, some columns had multiple values seperated by commas which violates the 1NF (first normal form) which requires that each cell has single value. I had to seperate them appropriately in individual rows to perform accurate analysis. 

