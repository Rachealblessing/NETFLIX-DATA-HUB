
# NETFLIX-DATA-HUB
Project hub for analyzing Netflix datasets, generating trends, and building visualizations

### Project Title: NETFLIX DATA HUB
---

TABLE OF CONTENT
---
[Project Overview](#Project_Overview)

[Data Source](#Data_Source)

[Tool Used](#Tool_used)

[Data Cleaning](#Data_Cleaning)

[Exploratory Data Analysis](#Exploratory_Data_Analysis)

[Data Visualization](#Data_Visualization)

[Insight](#Insight)

[Recommendation](#Recommendation)

### Project Overview
---
The goal of this project is to explore and analyse Netflix's content library to uncover trends, patterns, and insights related to its titles. 
This includes evaluating content distribution by genre, country, release year, and ratings, as well as identifying user-relevant insights such as content availabiltty and popularity

### Data Source
---
The dataset used is a publicly available Netflix dataset from Kaggle, which includes information on movies and TV shows available on the platform, including title, genre, cast, country, release year, duration, and user ratings

### Tool Used
---
- Microsoft Excel
  1. For data cleaning
  2. For data preparations
- SQL - Structured Query Language
  1. For Manipulation of data
  2. For extraction of data
- Power BI
  1. For data visualization
- GITHUB
  1. For portfolio building

### Data Cleaning
---
Prior to importing the netflix dataset into SQL, i performed essential cleaning in Excel- removing duplicates, addressing missing values, standardizing text formats, and verifying data types- to ensure data integrity and optimize it for analysis

### Exploratoy Data Analysis
---
# SQL
- How many movies and tv shows available on netflix
- Top 10 countries producing most netflix content
- Most common rating for movie
- Top 5 director with most content
- Title added in 2024
- Top 5 genre with most content

  ![SQL N1](https://github.com/user-attachments/assets/64c9e7fc-b5d6-4ae3-8f98-7c57fd164b32)
  
  ```sql
  select type,
  count(*) as total_count
  from[dbo].[Netflix data]
  where
  type is not null
  group by
  type;
  ```

  ![SQL N2](https://github.com/user-attachments/assets/9f7a2e75-f1d3-4a4c-8966-3a124d27e50a)

  ```sql
  select top 10
  country,
  count(*)as title_count
  from
  [dbo].[Netflix data]
  where
  country is not null
  group by
  country
  order by
  title_count desc
  ```

  ![SQL N3](https://github.com/user-attachments/assets/bf007ea5-2bf8-439f-adc2-3b3f199720aa)

  ```sql
  select top 1
  rating,
  count(*) as movie_count
  from [dbo].[Netflix data]
  where
  type='movie'and
  rating is not null
  group by
  rating
  order by
  movie_count desc;
  ```

  ![SQL N4](https://github.com/user-attachments/assets/f7835892-ea61-4b0f-bc79-66930f0ac0f9)
  
```sql
  select top 5 director,
  count(*)as total_titles
  from[dbo].[Netflix data]
  where directorbis not null
  group by
  director
  order by
  total_titles desc;
  ```
  

  ![SQL N5](https://github.com/user-attachments/assets/1787070d-98e0-4833-ace3-fd5ce068c699)

  ```sql
select title,
date_added
from {dbo}.{Netflix data]
where
TRY_CAST(date_added as date) is not null and
year(cast(date_added as date))=2024;
```

  ![SQL N6](https://github.com/user-attachments/assets/cc8b70c1-38b8-4976-a4ef-b340abd4c2ac)

  ```sql
select top 5
listed_in
count(*)as total_titles
from[dbo].[Netflix data]
where
listed_in is not null
group by
listed_in
order by
total_titles desc;
```

### Data Visualization
---

An interactive Power BI dashboard exploring Netflix's global catalog of over 26000 titles across 750+ countries. Key insight include:
- 69.6%Movies, 30.4% TV shows
- Top Countries: United States, India, UK, Japan, South Korea
- Content spans from 1925 to 2021
- Popular genres: Dramas, Documentaries,Comedies
- Most common ratings: TV-MA, TV-14
This visual project highlights content trends, growth, and diversity across NETFLIX'S library

![Netflix proof github](https://github.com/user-attachments/assets/7e52ab7e-2ecc-4a04-bb6d-aec4756d4b1a)

![netflix github 2](https://github.com/user-attachments/assets/38c843bd-4e10-4ad7-ba0b-f6e86a9e2548)

### Insight
---

- Most of Netflix's content is movies- around 70%
- People love watching dramas, documentaries, and comedies.
- A lot of show are rated TV-MA OR TV-14, so they are mostly for teens and adults
- Countries like the US, India,UK,Japan and South korea have the most titles.
- Netflix added a ton of content between 2019 and 2021

### Recommendations
---

- Add more TV series - they keep people watching longer.
- Mix in more Variety - like sci-fi, kids shows, or leser-known genres
- Create more family-friendly content to reach all age groups
- keep investing in local content for fast- growing countries.
- Keep investing in local content for fast-growing countries
- Shine a spotlight on some of the classic old titles- there's a market for them too








