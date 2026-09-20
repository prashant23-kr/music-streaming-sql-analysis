# 🎵 Music Streaming SQL Analysis

> A complete SQL-based data analytics project analyzing music streaming behavior using MySQL, covering 28 real-world analytical questions with Joins, CTEs, Subqueries, and Window Functions.

---

## 📌 Project Overview

The **Music Streaming SQL Analysis** project focuses on analyzing user listening behavior, song popularity, artist performance, subscription activity, and listening patterns using SQL.

The project contains **28 SQL analytical problems**, progressing from basic aggregation and joins to advanced SQL concepts such as:

- CTEs
- Subqueries
- Window Functions
- RANK()
- DENSE_RANK()
- ROW_NUMBER()
- LAG()
- Aggregations
- GROUP BY
- HAVING
- CASE statements
- Date and time analysis

The goal of this project is to demonstrate practical SQL and data-analysis skills by answering business-oriented questions from a music streaming dataset.

---

## 🎯 Project Objectives

The main objectives of this project are:

- Analyze music streaming activity.
- Identify the most-played songs and artists.
- Compare paid and free subscription users.
- Analyze user listening behavior.
- Calculate total listening time.
- Identify popular songs across subscription levels.
- Rank artists and songs using window functions.
- Analyze user activity over time.
- Identify heavy, regular, and light listeners.
- Apply advanced SQL techniques to solve analytical problems.

---

## 🗂️ Dataset

The project uses two main tables:

### 1. `events_cleaned`

This table contains user activity and song-play events.

Important columns include:

| Column | Description |
|---|---|
| `userId` | Unique user identifier |
| `artist` | Artist associated with the event |
| `song` | Song associated with the event |
| `level` | Subscription level such as paid/free |
| `ts` | Timestamp of the event |
| `length` | Song length in seconds |
| `page` | Type of user activity |

The `page = 'NextSong'` event is used to identify actual song-play activity.

---

### 2. `songs`

This table contains information about songs.

Important columns include:

| Column | Description |
|---|---|
| `artist_name` | Artist name |
| `title` | Song title |
| `year` | Song release year |

---

## 🛠️ Tools & Technologies

- **MySQL**
- **MySQL Workbench**
- **SQL**
- **GitHub**
- **Data Analysis**

---

# 📊 SQL Analysis – 28 Questions

## 🔹 Section 1 — Joins & Aggregations

### Q1. Join events with songs and calculate total song plays for every artist.

**Concepts Used:**
- JOIN
- COUNT()
- GROUP BY
- ORDER BY

---

### Q2. Join events with songs and find the top 10 songs by number of plays.

**Concepts Used:**
- JOIN
- COUNT()
- GROUP BY
- ORDER BY
- LIMIT

---

### Q3. Find total listening time in minutes for every artist.

**Concepts Used:**
- SUM()
- GROUP BY
- Mathematical calculation
- ROUND()

---

### Q4. Find users who listened to at least one song released after 2010.

**Concepts Used:**
- JOIN
- DISTINCT
- WHERE

---

### Q5. Compare paid and free users by number of song plays.

**Concepts Used:**
- GROUP BY
- COUNT()
- ORDER BY

---

### Q6. Find the most popular song for every subscription level.

**Concepts Used:**
- CTE
- GROUP BY
- ROW_NUMBER()

---

# 🔹 Section 2 — Window Functions

### Q7. Rank artists by total song plays using `RANK()`.

**Concepts Used:**
- CTE
- RANK()
- ORDER BY

---

### Q8. Rank songs within each subscription level using `DENSE_RANK()`.

**Concepts Used:**
- CTE
- DENSE_RANK()
- PARTITION BY

---

### Q9. Find the top 3 artists by plays in each subscription level using `ROW_NUMBER()`.

**Concepts Used:**
- CTE
- ROW_NUMBER()
- PARTITION BY

---

### Q10. For every user, number their song-play events chronologically using `ROW_NUMBER()`.

**Concepts Used:**
- ROW_NUMBER()
- PARTITION BY
- ORDER BY

---

### Q11. Use `LAG()` to calculate the time in minutes between consecutive song plays for each user.

**Concepts Used:**
- LAG()
- PARTITION BY
- ORDER BY
- Timestamp calculation

---

### Q12. Calculate cumulative listening time for every user over time.

**Concepts Used:**
- Window functions
- SUM() OVER()
- PARTITION BY
- ORDER BY

---

### Q13. Calculate each user's percentage contribution to total song plays.

**Concepts Used:**
- Aggregation
- Window functions
- Percentage calculation

---

### Q14. Find each user's most-played song using `ROW_NUMBER()`.

**Concepts Used:**
- CTE
- ROW_NUMBER()
- PARTITION BY

---

### Q15. Find the most popular song for each song-release year using `RANK()`.

**Concepts Used:**
- JOIN
- RANK()
- PARTITION BY
- GROUP BY

---

### Q16. For each user, compare current song length with previous song length using `LAG()`.

**Concepts Used:**
- LAG()
- PARTITION BY
- ORDER BY

---

# 🔹 Section 3 — CTE-Based Analysis

### Q17. Using CTEs, classify users as Heavy, Regular, or Light listeners based on total song plays.

**Concepts Used:**
- CTE
- CASE
- COUNT()
- GROUP BY

---

### Q18. Using CTEs, calculate total listening minutes for each user and return the top 10 users.

**Concepts Used:**
- CTE
- SUM()
- GROUP BY
- ORDER BY
- LIMIT

---

### Q19. Using CTEs, calculate daily song plays and return days with above-average activity.

**Concepts Used:**
- CTE
- Date extraction
- AVG()
- GROUP BY
- HAVING

---

### Q20. Using CTEs, calculate unique users, total plays and plays per user for each subscription level.

**Concepts Used:**
- CTE
- COUNT(DISTINCT)
- COUNT()
- GROUP BY
- Calculated metrics

---

### Q21. Using CTEs, calculate monthly song plays and find the month with the highest activity.

**Concepts Used:**
- CTE
- Date formatting
- GROUP BY
- ORDER BY

---

### Q22. Using CTEs, calculate plays by song-release year and identify release years with above-average plays.

**Concepts Used:**
- CTE
- JOIN
- AVG()
- GROUP BY
- HAVING

---

# 🔹 Section 4 — Subqueries

### Q23. Find users whose total song plays are greater than the average number of plays per user using a subquery.

**Concepts Used:**
- Subquery
- AVG()
- GROUP BY
- HAVING

---

### Q24. Find songs whose number of plays is greater than the average number of plays across all songs using a subquery.

**Concepts Used:**
- Subquery
- AVG()
- COUNT()
- GROUP BY
- HAVING

---

### Q25. Find the user with the highest total listening time using a subquery.

**Concepts Used:**
- Subquery
- SUM()
- MAX()
- GROUP BY

---

### Q26. Find artists whose total number of plays is greater than the average artist play count using a subquery.

**Concepts Used:**
- Subquery
- AVG()
- COUNT()
- GROUP BY
- HAVING

---

### Q27. Find users who have listened to more distinct songs than the average user.

**Concepts Used:**
- Subquery
- COUNT(DISTINCT)
- AVG()
- GROUP BY
- HAVING

---

### Q28. Find songs with a release year greater than the average release year that were actually played.

**Concepts Used:**
- Subquery
- JOIN
- AVG()
- DISTINCT
- Filtering

---

# 🧠 SQL Concepts Demonstrated

This project demonstrates practical use of the following SQL concepts:

### Basic SQL

- SELECT
- WHERE
- ORDER BY
- GROUP BY
- HAVING
- LIMIT
- DISTINCT

### Aggregation

- COUNT()
- SUM()
- AVG()
- MAX()
- ROUND()

### Joins

- INNER JOIN
- LEFT JOIN

### Common Table Expressions

- WITH
- Multiple CTEs
- CTE-based analysis

### Subqueries

- Scalar subqueries
- Aggregate subqueries
- Comparison with average values

### Window Functions

- RANK()
- DENSE_RANK()
- ROW_NUMBER()
- LAG()
- SUM() OVER()

### Other Techniques

- PARTITION BY
- CASE
- Date extraction
- Timestamp calculations
- Percentage calculations

---

# 📈 Key Analysis Areas

The project analyzes several important areas of music-streaming behavior.

### 🎵 Song Popularity

Identifying:

- Most-played songs
- Top songs by subscription level
- Songs with above-average plays
- Popular songs by release year

### 🎤 Artist Performance

Analyzing:

- Total plays per artist
- Total listening time
- Artist rankings
- Top artists by subscription level

### 👤 User Behavior

Analyzing:

- User listening frequency
- Most-played song per user
- Total listening time per user
- User activity over time
- Heavy, Regular, and Light listeners

### 💳 Subscription Analysis

Comparing:

- Paid users
- Free users
- Song-play activity
- Popular songs by subscription level
- Artist performance by subscription level

### 📅 Time-Based Analysis

Analyzing:

- Daily activity
- Monthly activity
- Song release years
- Consecutive listening events
- Cumulative listening time

---

# 📂 Project Structure

```text
music-streaming-sql-analysis/
│
├── README.md
│
├── Music_Streaming_SQL_28Q_Sample_Style_Presentation.pptx
│
└── Music_Streaming_SQL_Q1_Q28_LinkedIn_Video_16x9.mp4
