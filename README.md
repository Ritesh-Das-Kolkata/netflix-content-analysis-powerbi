# Netflix Content Analysis Dashboard

## Project Overview
An interactive 4-page Power BI dashboard analyzing 5,282 Netflix 
titles including Movies and TV Shows, with IMDB ratings and 
audience votes data. MySQL was used for data storage and cleaning, 
Power Query for transformation, and DAX for calculated measures.

## Tools Used
- MySQL — data storage and cleaning
- Power BI Desktop — dashboard building
- DAX — calculated measures
- Power Query — data transformation and custom columns

## Dataset
- 5,282 Netflix titles total
- Includes Movies and TV Shows
- Columns: title, type, release_year, age_certification, 
  runtime, imdb_id, imdb_score, imdb_votes

## Data Cleaning Steps (MySQL)
- Checked for NULL values — dataset was clean
- Verified row count after import
- Exported clean CSV for Power BI connection

## Power Query Transformations
Added 2 custom calculated columns:
- Score_Category — Excellent / Good / Average / Poor / No Rating
- Decade — groups content by decade (1950s, 1960s... 2020s)

## DAX Measures Created
- Total Titles
- Total Movies
- Total Shows
- Avg IMDB Score
- High Rated Titles (score >= 8.0)
- Avg Runtime

## Dashboard Pages

### Page 1 — Overview
- KPI cards: Total Titles, Movies, Shows, Avg Score
- Donut chart: Movies vs Shows split
- Bar chart: Titles by Score Category
- Bar chart: Titles by Age Certification
- Line chart: Content growth by Release Year
- Slicers: Type, Age Certification

### Page 2 — Ratings Analysis
- KPI cards: Avg Score, High Rated Titles, Total Titles
- Table: All titles rated 8.0 and above
- Bar chart: Avg IMDB Score by Age Certification
- Scatter plot: IMDB Score vs Release Year (size = votes)
- Slicers: Type, Score Category

### Page 3 — Content Trends
- KPI cards: Total Titles, Avg Runtime, High Rated Titles
- Bar chart: Total Titles by Decade and Type
- Line chart: Content growth by Release Year and Type
- Bar chart: Avg Runtime by Type
- Slicers: Type, Decade

### Page 4 — Top Content
- KPI cards: High Rated, Avg Score, Total Titles
- Bar chart: Top 10 Highest Rated titles
- Bar chart: Avg IMDB Score by Decade
- Bar chart: Top 10 Most Voted titles
- Slicers: Type, Decade

## Key Insights
- 64.24% Movies vs 35.76% Shows on Netflix
- Average IMDB Score of 6.54 across all titles
- 477 titles rated 8.0 or above — 9% excellent content
- Breaking Bad is the highest rated title with score 9.50
- Avatar: The Last Airbender scores 9.30
- Forrest Gump is the most voted title with 1.9M votes
- Content grew massively from 2010 peaking around 2019-2020
- 1960s and 1970s content has the highest average quality ratings
- Movies have avg runtime of ~100 mins vs Shows ~30 mins
- TV-14 rated content has the highest average IMDB score

## Screenshots
### Page 1 — Overview
![Overview](page1_overview.png)

### Page 2 — Ratings Analysis
![Ratings](page2_ratings.png)

### Page 3 — Content Trends
![Trends](page3_trends.png)

### Page 4 — Top Content
![Top Content](page4_topcontent.png)

## How to Use
1. Download `Netflix_Dashboard.pbix`
2. Open in Power BI Desktop
3. Use slicers to filter by Type or Decade
4. Click any visual to cross-filter other visuals
