## 🏡 Luxury Housing Sales Analysis – Bengaluru

### Python • SQL • Power BI • Real Estate Analytics Project

This project delivers a complete end-to-end analytics workflow for Bengaluru’s luxury housing sector by integrating Python for data cleaning, SQL for structured storage, and Power BI for interactive visualization. Using a dataset of 1,00,000+ records containing builder profiles, micro-market locations, pricing, configurations, amenities, sales channels, and booking information, the analysis uncovers key insights on market performance, buyer behaviour, booking conversion trends, and demand patterns. The combined pipeline provides a scalable, enterprise-ready solution for developers, investors, and stakeholders to make informed, data-driven decisions in the real estate domain.

### 🏗️ Project Architecture (High-Level):

       Raw Data (CSV)
           ↓
       Python (Data Cleaning & Features)
           ↓
       SQL Database
           ↓
       Power BI Dashboard
           ↓
       Business Insights


### 📌 Project Pipeline Overview

The project follows a structured three-stage analytics pipeline.

### 🐍 1. Python – Data Cleaning & Feature Engineering
- Loaded raw CSV data using Pandas  
- Cleaned inconsistent fields (Ticket Price, Amenity Score, Buyer Comments)  
- Handled missing and null values  
- Normalized categorical text fields (Builder, Micro_Market, Configuration)  
- Converted pricing values into Crores (Cr)  
- Engineered features such as Price_per_Sqft, Quarter_Label, and Booking_Flag  
- Exported the cleaned dataset for SQL integration 

### 🧹 Data Cleaning (Python)

Key cleaning steps done in Jupyter Notebook:

1. Clean Configuration Column

                 df['Configuration'] = (
                    df['Configuration']
                     .astype(str)
                     .str.lower()
                     .str.strip()
                   )

2. Clean Ticket Price Column

               df['Ticket_Price_Cr'] = (
                  df['Ticket_Price_Cr']
                    .astype(str)
                    .str.replace('c', '', regex=False)
                    .astype(float)
                  )

3. Convert Purchase Date to Date Format

              df['Purchase_Date'] = pd.to_datetime(df['Purchase_Date'], errors='coerce')


Engineered supplementary analytical attributes including:

         1. Price_per_Sqft – a unit cost indicator for comparative pricing

         2. Quarter_Label – temporal segmentation for trend evaluation

         3. Booking_Flag – binary classification enabling conversion analysis

Exported the refined dataset for structured loading into the SQL database.

### 🧠 2. SQL – Data Loading & Validation

Cleaned data was inserted into a SQL relational database.

✔ SQL Activities

Created SQL table schema

Inserted cleaned records via Python + SQLAlchemy

Ran validation queries:

        SELECT COUNT(*) FROM luxury_sales;
        SELECT Builder, SUM(Ticket_Price_Cr) FROM luxury_sales GROUP BY Builder;
        SELECT Micro_Market, AVG(Amenity_Score) FROM luxury_sales GROUP BY Micro_Market;


Verified data integrity & duplicates.

### 📊 3. Power BI – Interactive Dashboard & Business Insights

Power BI was employed to transform the validated SQL dataset into interactive, enterprise-ready dashboards that support strategic real estate decision-making. A direct connection was established between Power BI and the SQL database, followed by the creation of a robust data model and essential DAX measures. The dashboards were designed with dynamic slicers for Builder, Quarter, Micro_Market, and Configuration, and included comprehensive visualizations covering market trends, builder performance, booking conversion analysis, configuration demand, sales channel effectiveness, possession status impact, geographical distribution, and top-performing builders. KPI indicators and drill-through functionality were implemented to enable detailed project-level analysis and deeper business insights.

### 🚀 Business Insights:

Most luxury projects are concentrated in Bangalore East & North.

Prestige, Embassy, RMZ dominate overall revenue.

Booking success rate averages around 50% across builders.

Ready-to-Move homes show stronger booking rates.

Online + Direct Sales channels have higher conversion success.

### 🛠️ Tools & Technologies

- Python (Pandas, NumPy)  

- SQL (PostgreSQL)  

- Power BI (DAX, KPIs, Interactive Visuals)  

- Jupyter Notebook, VS Code

### 📂 Dataset
- Size: 100,000+ records  

- Key fields include Builder, Micro_Market, Ticket_Price_Cr, Configuration, Buyer_Type, Booking_Status, Sales_Channel, Amenity_Score, Possession_Status  

### 📌 How to Run the Project

Run Notebook:

       jupyter notebook notebooks/data_cleaning.ipynb

Open Power BI:

       Download Luxury_Housing.pbix

       Refresh data model

### 🎯 Outcome
   
   This project demonstrates an enterprise-ready analytics solution, showcasing an end-to-end data pipeline from raw data to actionable insights for the real estate domain.

### 📂 Project Contents:

           ├── data/
           │   └── luxury_house_bangalore.csv
           ├── notebooks/
           │   └── data_cleaning.ipynb
           │   └── EDA_analysis.ipynb
           ├── powerbi/
           │   └── Luxury_Housing.pbix
           ├── README.md


### Screenshot:
<img width="1920" height="1019" alt="luxury house 12_13_2025 5_42_09 PM" src="https://github.com/user-attachments/assets/036ac98b-38ac-4b41-aa6f-aa22569d76d0" />

