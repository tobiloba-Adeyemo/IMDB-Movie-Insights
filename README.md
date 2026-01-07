# IMDB Movie Insights
<img width="750" height="433" alt="image" src="https://github.com/user-attachments/assets/f1c83b2b-de3c-42d5-9260-8fd869f54a98" />


## Project Background

Stakeholders in the media and entertainment sector require a comprehensive performance review of top-rated movies to understand the drivers behind commercial success and audience engagement. The challenge is to identify which genres and specific titles yield the highest financial returns while simultaneously securing high viewer ratings and vote counts.

This project delivers a complete overview of IMDb movie metrics to inform decisions on content strategy, genre focus, and potential budget allocation for future productions.

Insights and recommendations are provided on the following key areas:

- **Revenue vs. Popularity Analysis:** Evaluation of the correlation between **Total Income ($28.9bn)** and **Total Votes (78M)** to determine if popular movies are always the most profitable.
- **Genre Performance Benchmarking:** Comparison of the "Top 10 Voted Genres" against the "Top 5 Profitable Genres" to identify market gaps where audience interest exceeds financial output or vice versa.
- **Top-Tier Movie Analysis:** Deep dive into individual high-performers, such as *The Shawshank Redemption* and *The Dark Knight*, to understand the specific attributes of market leaders.

**Interactive Dashboard:** The full IMDb Movie Insights dashboard can be accessed [here](https://drive.google.com/drive/folders/1VDdJLQSMD2ucIM4Vn3D2GGhlDxifJ_MI).

## Data Structure & Initial Checks

### Data Overview

The analysis was built on a data model developed within Power BI to ensure optimal performance and accurate reporting. The data was sourced from a comprehensive IMDb movie dataset, which was logically segmented and modeled into key tables:
- **'IMDb Movies' (Fact Table):** Contains core performance data including Movie Titles, Total Votes, Total Income (Gross Revenue), User Ratings, Duration, and Genre information.
- **'Calendar' (Dimension Table):** Contains hierarchical time attributes (Year, Month, Release Date) derived from the movie release dates to allow for temporal analysis.

### Data Model

The tables are connected via a **One-to-Many relationship** between the **Calendar Table** (one side) and the **IMDb Movies** table (many side) on the **Release Date** field. This structure allows for accurate filtering and time-intelligence calculations, ensuring that metrics like "Income" can be analyzed by specific release years or periods.

### Data Cleaning and Preparation

The data cleaning and transformation process was entirely executed using **Power Query (M Language)** to ensure data quality and integrity before modeling and visualization.
- **Genre Transformation:** A critical step involved splitting the delimited "Genre" column (e.g., "Action, Adventure") into distinct rows or categories to allow for the granular "Top 10 Voted Genres" analysis.
- **Data Type Standardization:** Power Query was used to correct data types, specifically converting the 'Income' column to Currency and 'Votes' to whole numbers for accurate aggregation.
- **Key Metric Calculation (DAX):** Measures like **Total Income**, **Average Income Per Movie**, and **Vote Rankings** were calculated in Power BI using DAX (Data Analysis Expressions) to create dynamic aggregations rather than relying on static columns.

<img width="1365" height="701" alt="image" src="https://github.com/user-attachments/assets/5ceb5c7c-adca-4a28-9894-f6dcb08b63c1" />

## Executive Summary

The overall performance of the analyzed dataset is robust, with **Total Income reaching $28.9bn** and a massive audience engagement of **78 million votes**. However, the analysis reveals a distinct divergence between genre popularity and financial return. While **Drama** dominates in terms of user engagement and vote volume, **Action/Adventure** genres drive the vast majority of revenue. The primary strategic insight is that while critical acclaim builds brand legacy, high-budget Action franchises remain the primary vehicle for maximizing Return on Investment (ROI).

### Overview of Market Performance

This section presents the high-level financial health and engagement trends, establishing the baseline for movie industry performance within this dataset.

### Genre Popularity vs. Profitability

- **Revenue Drivers:** **Action, Adventure, and Sci-Fi** combinations are the clear financial leaders, generating the highest total income (peaking near $6bn for the top combination).
- **Engagement Leaders:** **Drama** and **Crime** genres consistently receive the highest volume of votes, indicating strong cultural impact and viewer retention, even if they do not always match the box office numbers of Action films.

<img width="631" height="135" alt="image" src="https://github.com/user-attachments/assets/15579d39-597c-4c80-a328-71e8d7e142b7" />

### Top Movie & Title Performance

- **The "Blockbuster" Model:** Movies like **The Dark Knight** represent the ideal balance, ranking #2 in votes while generating over **$1 billion** in income, proving that high quality and high revenue can coexist.
- **The "Cult Classic" Phenomenon:** **The Shawshank Redemption** ranks #1 in total votes (2.2M) and ratings (9.03), yet generated a modest **$28.8M** in income compared to blockbusters. This highlights a segment of films that drive platform longevity rather than immediate box office spikes.
- **Vote Concentration:** The top 5 movies alone account for a significant portion of the total votes, showing that audience attention is heavily skewed toward a few "hall of fame" titles.

<img width="629" height="137" alt="image" src="https://github.com/user-attachments/assets/5631ff5f-0b9f-4c18-be85-a8d52bd6e75e" />

## Business Recommendations

Based on the analysis of the disparity between User Engagement (Votes) and Financial Return (Income), the following strategic actions are recommended to maximize both brand value and revenue:

1. **Adopt a Dual-Portfolio Strategy:**
   - **For Revenue:** Prioritize investment in **Action, Adventure, and Sci-Fi** genres. The "Top 5 Profitable Genres" chart confirms these are the primary drivers of box office gross (peaking at $6bn), despite not always having the highest critical ratings.
   - **For Brand/Retention:** Continue to curate **Drama and Crime** titles. While they generate lower immediate box office returns (e.g., *The Shawshank Redemption* earned only $28.8M), their dominance in "Top 10 Voted Genres" drives long-term platform engagement and viewer loyalty.

2. **Replicate the "Blockbuster Quality" Model:**
   - Analyze the production and marketing strategies of **"The Dark Knight"** and **"Inception"**. These titles represent the ideal market "sweet spot", ranking in the Top 5 for *both* Votes and Income ($1bn+ and $869M respectively). Future productions should aim for this balance of high-budget spectacle with strong narrative depth.

3. **Monetize High-Engagement "Cult Classics":**
   - *The Shawshank Redemption* is the #1 most voted and highest-rated movie (9.03 rating) but yielded the lowest income among the top 5 ($28M). This indicates massive *post-theatrical* popularity.
   - **Recommendation:** Leverage these titles for streaming licensing, merchandising, or "Director's Cut" re-releases to monetize the high viewer sentiment that wasn't captured at the box office.

4. **Revitalize Low-Income High-Vote Genres:**
   - Genres like **Biography and Romance** appear in the "Top 10 Voted" list but fail to appear in the "Top 5 Profitable." Marketing strategies for these genres should focus on lower-budget production to ensure profitability, or target direct-to-streaming models where engagement metrics are more valuable than box office tickets.
