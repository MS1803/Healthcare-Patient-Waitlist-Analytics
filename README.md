 🏥 Healthcare Patient Waitlist Analysis (2018–2021) | Power BI

 📌 Project Overview
Healthcare administrators need clear visibility into patient waitlists to manage capacity, reduce excessive waiting times, and improve patient outcomes. This project focuses on analyzing patient waitlist data to understand the current status, historical trends, and granular specialty- and age-level patterns.

The dashboard is designed to support operational and strategic decision-making for hospital management.

---

 🎯 Project Goals
1. Track the current status of the patient waitlist
2. Analyze historical monthly trends of the waitlist for:
   - Inpatient
   - Outpatient
3. Perform detailed specialty-level and age profile analysis

---

 📊 Data Scope & Dataset
- Time Period: 2018 – 2021
- Data Source: Multiple CSV files
  - Inpatient waitlist data
  - Outpatient waitlist data

 Data Grain
- One row per patient referral on the waitlist

---

 🗂️ Data Preparation & Transformation (Power Query)

 Multiple File Handling
- Imported separate inpatient and outpatient CSV files
- Standardized column names and data types
- Appended both datasets into a single fact table named `All_Data`
- Added a derived column to identify Care Type (Inpatient / Outpatient)

 Data Cleaning
- Removed duplicate records
- Handled missing values
- Standardized date formats
- Created derived columns for:
  - Patient age groups
  - Monthly reporting periods
  - Wait time bands

---

 🧠 Data Modeling

 Model Type
- Star Schema

 Tables Used
- Fact Table
  - `All_Data` – consolidated inpatient and outpatient waitlist data

- Dimension Tables
  - Date
  - Specialty
  - Patient (Age Profile)
  - Care Type

 Specialty Mapping
- Created a Mapping_Specialty table containing:
  - Specialty Name
  - Specialty Group
- Established a relationship between `All_Data` and `Mapping_Specialty`
- Enabled analysis at both specialty and specialty group levels

Design Rationale
- Simplifies DAX calculations
- Improves performance
- Enables grouped specialty-level insights for stakeholders

---

 🧮 Metrics & KPIs

 Core Metrics
1. Current Total Waitlist
2. Average Wait Time
3. Median Wait Time

 Analytical Concepts Used
- DAX measures
- Context filtering
- Time-based analysis

---

 📈 Dashboard Views

 1️⃣ Summary Page
Purpose: High-level monitoring of patient waitlists

Key Elements
- Current total waitlist KPI
- Average and median wait time KPIs
- Monthly trend of waitlist (2018–2021)
- Inpatient vs Outpatient comparison

---

 2️⃣ Detailed Analysis Page
Purpose: Granular analysis for operational insights

Key Elements
- Waitlist by specialty and specialty group
- Age profile distribution of patients
- Specialty-level wait time analysis
- Monthly trends by specialty

---

 🎯 Tooltip Implementation
- Created a custom tooltip using specialty mapping data
- Tooltip displays:
  - Total patients in waitlist
  - Specialty group
- Enables contextual insights without cluttering the main dashboard

---

 💡 Key Insights & Business Value

 Insights
- Clear visibility into how waitlists evolved from 2018 to 2021
- Identification of specialties and specialty groups with consistently high wait times
- Differences in waitlist behaviour between inpatient and outpatient services
- Age groups disproportionately impacted by longer waiting periods

 Business Impact
- Helps administrators identify capacity bottlenecks
- Supports informed staffing and resource allocation decisions
- Enables proactive waitlist management
- Improves transparency in healthcare operations

---

 🧠 Stakeholder Decision Support

This dashboard enables stakeholders to:
- Prioritize specialties and specialty groups requiring capacity expansion
- Optimize inpatient vs outpatient workflows
- Plan age-specific care pathways
- Use historical trends to anticipate future demand

---

 🛠️ Tools & Skills Used
- Power BI Desktop
- Power Query (M)
- DAX
- Data Modeling (Star Schema)
- Healthcare Operations Analytics
- Data Visualization & Storytelling




