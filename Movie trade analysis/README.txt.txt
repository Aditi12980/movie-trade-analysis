Movie Ratings & Revenue Analysis
Overview
This project focuses on analyzing movie data to understand trends in ratings, genres, revenue, and overall performance. It helps identify factors that contribute to a movie being a Hit or Flop using SQL, Python, and visualization tools.
---
Objectives
- Analyze movie ratings and audience engagement
- Compare revenue, budget, and profit
- Identify top-performing genres and platforms
- Classify movies as Hit or Flop
- Visualize trends using graphs and dashboards
---
Tech Stack
- SQL (SQLite / DBeaver) – Data storage & querying
- Python (Matplotlib / Pandas) – Data analysis & visualization
- Power BI – Interactive dashboard
- Excel – Data preprocessing

---
Dataset Description
The dataset contains the following columns:
- "Name" – Movie name
- "Release_Date" – Release date
- "Year", "Month" – Time-based analysis
- "Colour" – Black & White / Color
- "Platform" – Netflix, Theatre, Amazon Prime, etc.
- "Genre" – Action, Drama, Comedy, Sci-Fi, etc.
- "Language", "Country", "State"
- "Rating" – Movie rating
- "Votes" – Audience votes
- "Revenue" – Earnings (Crore ₹)
- "Budget" – Production cost
- "Profit" – Revenue - Budget
- "Hit_Flop" – Movie performance
---
Database Schema
CREATE TABLE Movies (
    Name TEXT,
    Release_Date TEXT,
    Year INTEGER,
    Month TEXT,
    Colour TEXT,
    Platform TEXT,
    Genre TEXT,
    Language TEXT,
    Country TEXT,
    State TEXT,
    Rating REAL,
    Votes INTEGER,
    Revenue REAL,
    Budget REAL,
    Profit REAL,
    Hit_Flop TEXT
);
---
Key SQL Queries
-- Top 5 highest revenue movies
SELECT Name, Revenue
FROM Movies
ORDER BY Revenue DESC
LIMIT 5;

-- Genre-wise movie count
SELECT Genre, COUNT(*) AS Total
FROM Movies
GROUP BY Genre;

-- Platform-wise average rating
SELECT Platform, AVG(Rating) AS Avg_Rating
FROM Movies
GROUP BY Platform;

-- Hit vs Flop analysis
SELECT Hit_Flop, COUNT(*) AS Count
FROM Movies
GROUP BY Hit_Flop;

---
Analysis & Visualizations
- Bar charts for genre distribution
- Pie chart for Hit vs Flop
- Line chart for yearly revenue trends
- Comparison of Budget vs Profit
---
Key Insights
- High-budget movies often generate higher revenue
- Action and Sci-Fi genres tend to perform better
- OTT platforms are gaining popularity
- Profit does not always depend on rating
---
How to Run the Project
1. Open DBeaver / SQLite
2. Create the "Movies" table
3. Insert dataset records
4. Run SQL queries
5. Use Python or Power BI for visualization
---
Future Improvements
- Add real-world dataset
- Apply machine learning for prediction
- Enhance dashboard interactivity
---
Author
Aditi Borkar
Computer Science Student
---