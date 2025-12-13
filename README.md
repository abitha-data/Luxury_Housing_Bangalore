## 🏡 Luxury Housing Sales Analysis – Bengaluru

### Python • SQL • Power BI • Real Estate Analytics Project

This project delivers a complete end-to-end analytics workflow for Bengaluru’s luxury housing sector by integrating Python for data cleaning, SQL for structured storage, and Power BI for interactive visualization. Using a dataset of 1,00,000+ records containing builder profiles, micro-market locations, pricing, configurations, amenities, sales channels, and booking information, the analysis uncovers key insights on market performance, buyer behaviour, booking conversion trends, and demand patterns. The combined pipeline provides a scalable, enterprise-ready solution for developers, investors, and stakeholders to make informed, data-driven decisions in the real estate domain.

📌 Project Pipeline Overview

This project was developed through a structured, three-stage workflow, enabling a seamless transition from raw data to actionable business intelligence.

🐍 1. Python – Data Cleaning & Feature Engineering

Extensive preprocessing was performed on the raw dataset to ensure analytical accuracy, consistency, and readiness for downstream processing.

✔ Key Data Preparation Activities

Imported and processed the raw CSV using Pandas for efficient tabular manipulation.

Standardized inconsistent inputs across critical fields such as Ticket Price, Amenity Score, and Buyer Comments.

Detected and treated missing values using appropriate imputation and cleaning strategies.

Normalized categorical text fields (Builder, Micro_Market, Configuration) to maintain uniform formatting.

Converted monetary values into Crores (Cr) for consistency in financial analysis.

Engineered supplementary analytical attributes including:

Price_per_Sqft – a unit cost indicator for comparative pricing

Quarter_Label – temporal segmentation for trend evaluation

Booking_Flag – binary classification enabling conversion analysis

Exported the refined dataset for structured loading into the SQL database.
