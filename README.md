# Loan_Default-Project-Overview
__Loan Analysis & Financial Risk Intelligence Ecosystem__
**Project Overview**
This project focuses on building an end-to-end data intelligence ecosystem to analyze borrower behavior and assess financial risk. By leveraging a dataset of over 255,000 loan records, the system provides deep insights into applicant demographics, loan characteristics, and repayment trends to help financial institutions make data-driven lending decisions.

**Technical Stac**
▪️	Database: SQL Server (On-premise data storage) 
▪️	Data Orchestration: Microsoft Fabric (Dataflow Gen1) 
▪️	Data Lake: Fabric Lakehouse 
▪️	Analytics & Visualization: Power BI Desktop 
▪️	Data Transformation: Power Query & DAX 

**Data Pipeline Architecture**
1️⃣	Data Ingestion: A dedicated database named Loan was created in SQL Server, and the raw Loan_default.csv flat file was imported for initial storage.
2️⃣	ETL & Orchestration: Utilized Microsoft Fabric Dataflows to authenticate with SQL Server and ingest data into the Fabric Lakehouse. A scheduled refresh was implemented to ensure the data remains current.
3️⃣	Data Transformation: Employed Power Query Editor for column profiling and data quality management. This involved handling null values and optimizing data types to ensure high-quality downstream analysis.
   
**Key Metrics & DAX Logic**
__The project utilizes advanced DAX measures to track institutional health and risk exposure__:
▪️	Year-over-Year (YoY) Analysis: Calculates percentage changes in loan volume and default cases to identify growth and risk trends.
▪️	Default Risk Modeling: Measures the annual default percentage and category-specific default rates (e.g., by employment type).
▪️	Segment Intelligence: Calculates average loan amounts and incomes across specific age groups and credit tiers (e.g., "High" credit score borrowers).
▪️	Cumulative Performance: Tracks Year-to-Date (YTD) cumulative loan totals, locked to specific dimensions like marital status and credit bins using ALLEXCEPT.

**Interactive Dashboards**
__The ecosystem features three specialized reporting layers__:
1️⃣ Loan Default & Overview
Provides a high-level summary of the portfolio, including loan amounts by purpose, default rates by year, and demographic distributions by employment and age.
2️⃣ Applicant Demographic & Financial Profile
Deep dives into the borrower persona, visualizing median loan amounts by credit score, educational backgrounds, and the impact of existing mortgages or dependents on loan size.
3️⃣ Financial Risk Metrics
Focuses on advanced risk indicators, including YoY growth trends, YTD totals by marital status, and a decomposition tree analyzing total loan amounts by income bracket and employment type.

**Dataset Description**
__The dataset includes critical borrower attributes such as__:
▪️	Demographics: Age, Education, Marital Status, and Employment Type.
▪️	Financial Status: Annual Income, Credit Score, DTI Ratio, and existing mortgages.
▪️	Loan Details: Loan Amount, Interest Rate, Term, Purpose, and Default status

