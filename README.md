# Netflix Movies & TV Shows Analysis

A data cleaning, transformation, and visualization project focused on analyzing Netflix Movies and TV Shows using **Power Query** and **Power BI**.  
The project improves data quality, resolves inconsistencies, and delivers interactive insights through a well structured dashboard.


---

## 📌 Project Overview

This project analyzes the Netflix Movies and TV Shows dataset with the goal of preparing it for accurate analysis and professional visualization.

### Objectives
- Clean and standardize raw Netflix data
- Handle missing and inconsistent values
- Create calculated fields for better categorization
- Build interactive and insight driven Power BI visuals

---

## 🗂️ Dataset Information

**Dataset:** Netflix Movies and TV Shows  
**Records:** 8,300+ titles  
**Content Types:** Movies and TV Series  

### Key Columns
- 🎞️ Title  
- 🎭 Cast  
- 🎬 Director  
- 🌍 Country  
- 📅 Date Added  
- ⏱️ Duration  
- 🏷️ Type (Movie / TV Show)  


## [Netflix Raw Dataset](https://github.com/IsmailO-Portfolio/Netflix-TV--Shows---Movies-Analysis/blob/main/Netflix_Raw_Data.csv.xlsx)


---

## 🛠️ Tools Used

- Microsoft Power Query  
- Microsoft Power BI  
- Microsoft Excel  

---

## ⚙️ Power Query Transformation Steps

### 1️⃣ Handling Missing Values
To prevent errors and improve visual quality:

- **Text Columns:**  
  Replaced null values with `"Unknown"` for fields such as Director, Cast, and Country.

- **Date Columns:**  
  Replaced null dates with a placeholder date (`01/01/2020`) to allow time based filtering without losing records.

---

### 2️⃣ Date and Duration Parsing

- **Date Extraction:**  
  Extracted:
  - Year  
  - Month Name  
  from the `Date Added` column to support time series analysis.

- **Duration Splitting:**  
  Used *Text Before Delimiter* to extract numeric values from:
  - `"90 min"`  
  - `"2 Seasons"`  

  This enabled conversion to a numeric data type for aggregation and comparison.

---

### 3️⃣ Calculated Columns

- **Conditional Column (Type Standardization):**  
  Logic applied:
  - If `Type = Movie` → `Film`  
  - Else → `Series`  

  This improves naming consistency and dashboard presentation.

---

### 4️⃣ Final Applied Steps
All transformations were applied sequentially in Power Query to ensure data integrity and reproducibility before loading into Power BI.

---

## 🚧 Challenges & Solutions

### Challenge 1: Mixed Duration Formats
- **Problem:** Duration column contained both minutes and seasons.
- **Solution:** Extracted numeric values using delimiter based text transformation before type conversion.

---

### Challenge 2: Null Values Affecting Visuals
- **Problem:** Nulls created blank slicer and chart entries.
- **Solution:**  
  - Replaced descriptive nulls with `"Unknown"`  
  - Replaced date nulls with a base date  

This ensured a clean and professional dashboard experience.

## [NetFlix Analyzed Dataset](https://github.com/IsmailO-Portfolio/Netflix-TV--Shows---Movies-Analysis/blob/main/Netflix_Analyzed.xlsx)
---

## 📊 Visualizations & Insights

### Key Metrics
- 📌 **Total Titles:** 8.3K  
- 🎥 **Movies:** 5.7K  
- 📺 **Series:** 2.6K  

---

### Major Insights

- **Top Producing Countries:**  
  United States leads, followed by India and Unknown (previously null values).

- **Content Growth Over Time:**  
  Significant increase in titles after 2015, with Films consistently outnumbering Series.

- **Average Duration:**  
  - Films average **98 minutes**  
  - Series average **2 seasons**

---

## 🧭 Dashboard Features

- 🎛️ Type Slicers: Instantly filter between Films and Series  
- 📈 Interactive Charts: Hover enabled for detailed yearly insights  
- 🌙 Dark Mode Theme: High contrast red and gray design for readability  

---

## 🧠 Key Takeaways

- Netflix content expanded rapidly post 2015  
- Movies dominate the platform’s content library  
- Proper null handling significantly improves dashboard quality  
- Power Query is essential for preparing clean, analysis ready data  

---

## 📁 Use Cases

- Streaming content analysis  
- Media library trend analysis  
- Dashboard and BI portfolio projects  
- Data cleaning and transformation demonstrations  

---

**Author:** Zen  

