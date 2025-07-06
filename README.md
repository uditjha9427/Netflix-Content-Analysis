Netflix Content Strategy: A Deep Dive Analysis
A Data Analytics Portfolio Project


Project Overview

This project performs a comprehensive analysis of the Netflix content library to reverse-engineer its content strategy. By exploring trends in content types, genres, geographical distribution, and the rise of "Netflix Originals," this analysis aims to answer the question: How does Netflix decide what to invest in?
The entire process, from data cleaning and exploratory analysis in Python to the creation of a final interactive dashboard in Power BI, is documented here.


1) 🛠️ Tech Stack
Python: Used for data cleaning, processing, and exploratory data analysis.
Libraries: Pandas, NumPy, Matplotlib, Seaborn, Plotly
Power BI: Used for creating the final interactive and shareable business intelligence dashboard.
Jupyter Notebook: Used as the environment for Python scripting and analysis.

2) 📊 Data Source
The dataset used for this analysis is the "Netflix Movies and TV Shows" dataset, publicly available on Kaggle.
Source: Kaggle
Description: This dataset contains information on all movies and TV shows available on Netflix as of 2022, including details like type, title, director, cast, country, release year, rating, duration, and genre.

3) ⚙️ Project Workflow
1. Data Cleaning and Preparation (Python)
The initial dataset required significant cleaning and feature engineering to prepare it for analysis. The key steps performed in the Jupyter Notebook (notebooks/netflix_analysis.ipynb) were:
Handling Missing Values: Filled nulls in director, cast, and country with "Unknown" to preserve data. Dropped the few rows with missing date_added or rating as they were essential for analysis.
Data Type Correction: Converted date_added to a proper datetime format.
Feature Engineering:
Extracted year_added and month_added from the date_added column for time-series analysis.
Created a crucial proxy column, content_source, to classify titles as "Original" or "Licensed". A title was flagged as an Original if its release_year was the same as its year_added to Netflix.
Split and exploded the country and listed_in columns to enable accurate counting for multi-country and multi-genre titles.
Final Output: A cleaned CSV file (data/netflix_dashboard_data.csv) was generated as the single source of truth for all subsequent analysis and visualization.
2. Exploratory Data Analysis (EDA) (Python)
Using the cleaned dataset, an in-depth EDA was conducted to uncover initial trends and form hypotheses. Key visualizations and findings from this phase include:
The clear pivot from Movies to TV Shows starting around 2018.
The dominance of content for mature audiences (TV-MA and TV-14).
The identification of key international markets like India, the UK, Japan, South Korea, and Spain.
3. Dashboard Creation (Power BI)
The insights from the EDA were used as a blueprint to build a three-page interactive dashboard in Power BI:
Overview: A high-level summary with KPIs for total titles, a breakdown of content types, top genres, and a timeline of content additions.
Originals vs. Licensed: A deep dive comparing the characteristics of Netflix Originals against licensed content, focusing on genre choice, rating, and production country.
Global Footprint: A geospatial analysis showcasing Netflix's production hotspots around the world and highlighting the growth of international content.
📈 Key Insights & Business Recommendations
This analysis revealed several core pillars of Netflix's content strategy:


🚀 Insight 1: The Strategic Pivot to TV Shows and Originals
Netflix has fundamentally shifted its focus from being a library of licensed movies to a production house for binge-worthy original TV series. The data shows a clear crossover point around 2018 where the volume of new TV shows added began to surpass movies. This strategy is aimed at subscriber retention, as exclusive, multi-episode series are more effective at keeping audiences engaged on the platform.
Business Implication: Investment in long-form, episodic content is paramount. The "fail-fast" model, evidenced by the high number of shows with only one season, allows Netflix to test a wide variety of concepts and double down only on proven hits.

🌎 Insight 2: Aggressive Globalization with Localized Production
While the US remains the largest content producer, there has been an exponential increase in content from international markets, particularly South Korea, India, and Spain. These aren't just licensed acquisitions; Netflix is heavily investing in creating Originals in these regions.
Business Recommendation: Continue to empower and invest in regional production hubs. The success of shows like Money Heist (Spain) and Squid Game (South Korea) proves that locally-produced content can achieve massive global success. Netflix should leverage its data to identify which genres resonate best in which markets and tailor production accordingly (e.g., thrillers in Spain, dramas in South Korea).

🎯 Insight 3: A Laser Focus on the Adult Binge-Watcher
The vast majority of Netflix Originals are rated TV-MA or TV-14. When compared to licensed content, Originals are significantly less likely to be aimed at children or families. The dominant genres for originals are dramas and thrillers—categories known for their "binge-ability."
Business Recommendation: While the adult market is well-covered, there is a strategic opportunity to expand the library of original family-friendly and children's content. This could be a key growth area to attract and retain family subscriptions, a demographic potentially underserved by the current Originals strategy.


![final dashboard](https://github.com/user-attachments/assets/aa1da985-1b80-4923-8e48-949e7461ceab)
