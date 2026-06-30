# 📊 EdTech Recorded Lecture Analytics Dashboard

## 📝 Project Overview
This project involves the end-to-end development of an interactive Power BI analytics dashboard using a dataset sourced from a major EdTech platform. The goal of the project was to transform raw, scraped web data into a fully functional Star Schema data model to analyze course catalog distribution, audience engagement (viewership), and instructor performance.

## 🛠️ Tools & Technologies
* **Data Cleaning & Transformation:** Power Query
* **Data Modeling:** Power BI (Star Schema)
* **Calculations:** DAX (Data Analysis Expressions)
* **Visualization:** Power BI

## 🗂️ Data Modeling
The raw dataset (8,000+ rows) required significant cleaning, including extracting numerical durations from text strings and standardizing viewership metrics. A **Star Schema** was implemented to ensure optimal dashboard performance:
* **Fact Table:** `FactCourses`
* **Dimension Tables:** `DimCategory`, `DimLanguage`, `DimInstructor`
* **Bridge Table:** A dedicated `DimSkills` bridge table was created using advanced split-by-delimiter logic to normalize comma-separated skill tags without violating schema integrity.

## 📈 Dashboard Features
The final three-page interactive dashboard features a synchronized vertical Filter Panel and a cohesive "Executive Teal" theme. 

1. **Catalog Overview:** Drill-down matrices and 100% stacked column charts analyzing course volume by category, sub-category, and course type.
2. **Audience Engagement:** Scatter plots and clustered column charts identifying the "sweet spot" for course duration and proving the massive viewership impact of subtitle availability.
3. **Instructor & Advanced Metrics:** Contextual DAX rankings (`RANKX` and `ALL`) to dynamically showcase the Top 3 highest-rated instructors per discipline.

## 💡 Key Business Insights
* **Micro-Credentials Over Marathons:** Highly technical fields (Data Science & IT) drive the most traffic but have the longest durations. Breaking these into shorter "micro-credentials" could boost completion rates.
* **The Accessibility Premium:** Courses offering translated subtitles generate roughly three times the average viewership compared to those without, proving that accessibility is a primary driver of global engagement.
* **Curriculum Focus:** Scatter plot correlation between 'Skill Variety' and 'Views' indicates that highly focused courses often outperform those with sprawling, bloated curriculums.

## 📂 Repository Contents
* `/Data` - The initial raw dataset.
* `/Dashboard` - The interactive `.pbix` Power BI file.
* `/Report` - The comprehensive PDF project report detailing methodologies and limitations.
* `/Screenshots` - Visuals captured directly from the dashboard.
