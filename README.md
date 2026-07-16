# 🎬 Netflix Movies & TV Shows Data Analysis (SQL)

![Netflix Logo](https://github.com/ansarishams/netflix_sql_project/blob/main/Netflix%20logo.png)

## 📌 Overview
This project performs an end-to-end **exploratory data analysis** of the Netflix Movies and TV Shows dataset using **PostgreSQL**. The goal is to clean, query, and extract meaningful business insights around content trends, genres, countries, ratings, cast/director patterns, and content classification.

The dataset contains **8,807 titles** with details on type, director, cast, country, date added, release year, rating, duration, genre, and description.

---

## 🎯 Objectives
- Analyze the distribution of content types (Movies vs TV Shows)
- Identify the most common ratings for each content type
- Explore content by release year, country, and duration
- Identify content added in the last 5 years
- Analyze content based on specific directors and actors
- Categorize content based on the presence of specific keywords in the description

---

## 🗂️ Dataset

| File | Description |
|---|---|
| `netflix_titles.csv` | Raw dataset containing 8,807 Netflix titles with 12 columns |
| `netflix_solution.sql` | SQL script with table schema and all 15 business problem solutions |

**Columns:** `show_id`, `type`, `title`, `director`, `casts`, `country`, `date_added`, `release_year`, `rating`, `duration`, `listed_in`, `description`

---

## 🛠️ Tools & Tech Stack
- **PostgreSQL** – Database & querying
- **SQL** – Data cleaning, aggregation, window functions, string operations
- **Concepts used:** `GROUP BY`, `CASE WHEN`, `RANK() OVER()`, `UNNEST + STRING_TO_ARRAY`, `SPLIT_PART`, `ILIKE`, date parsing with `TO_DATE`

---

## 🧱 Schema

```sql
CREATE TABLE netflix(
    show_id       VARCHAR(20) PRIMARY KEY,
    type          VARCHAR(20),
    title         VARCHAR(200),
    director      VARCHAR(250),
    casts         VARCHAR(1000),
    country       VARCHAR(200),
    date_added    VARCHAR(50),
    release_year  INT,
    rating        VARCHAR(20),
    duration      VARCHAR(50),
    listed_in     VARCHAR(100),
    description   VARCHAR(300)
);
```

---

## 🔍 Business Problems Solved

1. Count the number of Movies vs TV Shows
2. Find the most common rating for Movies and TV Shows
3. List all movies released in a specific year (e.g., 2020)
4. Find the top 5 countries with the most content on Netflix
5. Identify the longest movie
6. Find content added in the last 5 years
7. Find all movies/TV shows by director 'Rajiv Chilaka'
8. List all TV shows with more than 5 seasons
9. Count the number of content items in each genre
10. Find each year and the average number of content releases in India; return the top 5 years with highest average
11. List all movies that are documentaries
12. Find all content without a director
13. Find how many movies actor 'Salman Khan' appeared in over the last 10 years
14. Find the top 10 actors who have appeared in the highest number of movies produced in India
15. Categorize content as **'Good'** or **'Bad'** based on the presence of keywords like *'kill'* and *'violence'* in the description, and count items in each category

---

## 💡 Key Insights
- Netflix's catalog is dominated by a specific content type, with a clear split between Movies and TV Shows.
- **TV-MA** and **TV-14** are among the most frequent ratings, indicating a strong focus on mature/adult audiences.
- The **United States** and **India** rank among the top content-producing countries on the platform.
- A significant share of content was added in the last 5 years, reflecting Netflix's aggressive content expansion strategy.
- Genre-wise breakdown highlights **Dramas**, **International Movies**, and **Comedies** as leading categories.
- Content classification by keyword ('kill'/'violence') shows the majority of titles fall under the **'Good_Content'** category.

---

## 🚀 How to Run
1. Install PostgreSQL (or use any SQL-compatible database).
2. Create a database and run the schema from `netflix_solution.sql`.
3. Import `netflix_titles.csv` into the `netflix` table using `\copy` (psql) or your DB client's import tool.
4. Run each query section-by-section to reproduce the analysis.

```sql
\copy netflix FROM 'netflix_titles.csv' DELIMITER ',' CSV HEADER;
```

---

## 📁 Repository Structure
```
├── netflix_titles.csv        # Raw dataset
├── netflix_solution.sql      # SQL schema + all business problem queries
└── README.md                 # Project documentation
```

---

## 👤 Author
**Shamsul Hoda**
Data Analyst | SQL • Python • Power BI • Advanced Excel
📧 shamsbusiness4632@gmail.com
🔗 [LinkedIn](https://www.linkedin.com/in/shamsulhoda-s4632)

---

⭐ If you found this project useful, consider giving it a star on GitHub!
