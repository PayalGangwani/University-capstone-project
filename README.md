# University-capstone-project
capstone project on  university success analysis
📌 Project Overview
This is an end-to-end University Success Analysis Capstone Project by Payal Gangwani that investigates various dimensions related to global universities — including their correlations with economic indicators, demographics, ranking criteria, and gender distribution.
The project analyzes 1,247 universities across 74 countries with 29,612+ ranking records spanning multiple years using Power BI, Excel EDA, and MySQL.

🎯 Objectives
Perform comprehensive analysis of global university rankings across multiple ranking systems
Identify key factors influencing university rankings
Analyze historical trends in university performance
Study the impact of gender distribution & international students on rankings
Derive meaningful conclusions and recommendations for improving ranking methodologies

🗂️ Project Structure
📁 POWER_BI-CAPSTONE_UNIVERSITY/
│
├── 📊 CAPSTONE EDA OF POWER BI.pbix          # Power BI Dashboard
├── 📓 CAPSTONE . EDA.xlsx                     # Excel EDA file
│
├── 📂 DATA/
│   ├── 📂 CSV/
│   │   ├── university.csv                     # 1,247 universities
│   │   ├── country.csv                        # 74 countries
│   │   ├── university_year.csv                # Year-wise student data
│   │   ├── ranking_system.csv                 # 3 ranking systems
│   │   ├── ranking_criteria.csv               # 21 ranking criteria
│   │   └── university_ranking_year.csv        # 29,612 ranking records
│   │
│   └── 📂 SQL/
│       ├── universities_university.sql
│       ├── universities_country.sql
│       ├── universities_ranking_system.sql
│       ├── universities_ranking_criteria.sql
│       ├── universities_university_year.sql
│       └── universities_university_ranking_year.sql
│
├── 📂 MECE/
│   ├── final mece 2.docx                      # MECE Framework document
│   └── final mece 2.jpg                       # MECE diagram
│
├── 📋 UNIVERSITY SUCCESS ANALYSIS PPT.pptx   # Project presentation
├── 📄 UNIVERSITY SUCCESS ANALYSIS WORD.docx  # Project documentation
└── 📖 README.md

📊 Dataset Description
Tables Overview
Table
Rows
Description
university
1,247
University names & country mapping
country
74
Country names worldwide
university_year
1,085
Students, staff ratio, gender % per year
ranking_system
3
THE, Shanghai, CWUR ranking systems
ranking_criteria
21
Criteria used by each ranking system
university_ranking_year
29,612
University scores per criteria per year
Key Columns
Column
Description
university_name
Name of the university
country_name
Country of the university
num_students
Total number of students
student_staff_ratio
Students per staff member
pct_international_students
% of international students
pct_female_students
% of female students
score
Ranking score per criteria
year
Year of ranking
criteria_name
Teaching / Research / International etc.

🛠️ Tools & Technologies
Tool
Purpose
Power BI Desktop
Interactive dashboards & visualizations
DAX
Calculated measures & KPIs
Power Query
Data transformation & ETL
MySQL Workbench
Database setup & SQL queries
Microsoft Excel
Exploratory Data Analysis (EDA)
MECE Framework
Structured problem-solving approach

🔄 Project Process
1. Data Acquisition from GitHub
        ↓
2. Data Transformation & Enhancement (Power Query)
        ↓
3. Database setup in MySQL Workbench
        ↓
4. Connected with Power BI, Excel & MySQL
        ↓
5. Problem Statement Solutions in Power BI
        ↓
6. Exploratory Data Analysis (EDA) in Excel
        ↓
7. Creation of Visuals & Dashboards
        ↓
8. MECE Framework Documentation
        ↓
9. Detailed Presentation & Report

🧩 Data Model (ER Diagram)
        ranking_system
              │
              ▼
      ranking_criteria
              │
              ▼
university_ranking_year ◄──── university ◄──── country
              │                    │
              ▼                    ▼
           score            university_year
                          (students, gender,
                           staff ratio)
Relationships:
university → country (Many to One)
university_ranking_year → university (Many to One)
university_ranking_year → ranking_criteria (Many to One)
ranking_criteria → ranking_system (Many to One)

💼 Business Problem Statements & Insights
Q1. How many universities are there in each country?
🔍 Insight: USA and UK have the highest number of universities, reflecting their substantial investment in education and research.
Q2. What is the distribution of international students across countries?
🔍 Insight: USA, UK, and Australia are top destinations for international students due to extensive academic offerings and inclusive environments.
Q3. Which country has the highest number of female students?
🔍 Insight: United States leads in promoting gender equality in higher education.
Q4. How many universities are ranked by each ranking system?
🔍 Insight: KPI chart shows university distribution across THE, Shanghai, and CWUR ranking systems.
Q5. How does ranking system affect student-staff ratio?
🔍 Insight: Different ranking systems show varying student-to-staff ratios across universities.
Q6. What are the most important ranking criteria?
🔍 Insight: CWUR places highest importance on criteria while Shanghai Ranking places the lowest.
Q7. Is there a correlation between score and international students?
🔍 Insight: Positive correlation — higher ranked universities attract more international students.
Q8. How does female student % impact university ranking?
🔍 Insight: Universities with scores below 10K tend to have higher female enrollment (50–60%).

💡 Key Insights
🇺🇸 USA dominates global rankings with the highest number of universities
🌍 74 countries represented — truly a global analysis
👩‍🎓 Gender equality — USA leads in female student enrollment
📈 Positive correlation between university score and international student %
🏆 3 Ranking Systems analyzed — THE, Shanghai, CWUR
📊 CWUR uses the most criteria for ranking universities
🤝 International diversity strongly linked to higher university rankings

🗄️ Database Setup (MySQL)
-- Create database
CREATE DATABASE universities;
USE universities;

-- Tables are available in DATA/SQL/ folder
-- Run files in this order:
-- 1. universities_country.sql
-- 2. universities_ranking_system.sql
-- 3. universities_ranking_criteria.sql
-- 4. universities_university.sql
-- 5. universities_university_year.sql
-- 6. universities_university_ranking_year.sql
