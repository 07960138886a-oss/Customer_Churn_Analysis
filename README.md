1. Customer Churn Analysis & Predictive Modeling   
An end-to-end data analytics and machine learning framework combining Google BigQuery SQL, a Random Forest Classifier in Python, and an interactive Power BI Dashboard to identify historical churn drivers and predict at-risk customers before they churn.

2. Executive Summary & Key Metrics    
Analytic overview across a customer base of 6,418 records:        
（1）Key Metrics: 6,418 Total Customers | 411 New Joiners | 1,732 Total Churned | 27.0% Churn Rate.           
（2）Primary Churn Drivers: Month-to-month contracts (46.53% churn rate), Competitor defection (44% of total churn), and Fiber Optic service vulnerabilities (41.10% churn rate).           
（3）Predictive Impact: The trained model identified 383 high-risk new joiners (Predictions.csv), enabling targeted retention campaigns prior to account renewal.             

4. Pipeline Architecture & Tech Stack                
[ Raw Data ] ──> [ BigQuery SQL (ETL) ] ──> [ Production Views ] ──> [ Random Forest ML ] ──> [ Power BI Dashboard ]              
(1) Data Warehouse: Google BigQuery (SQL)        
(2) Machine Learning: Python (Pandas, Scikit-Learn)       
(3) Business Intelligence: Power BI        

5. Dashboards & Predictive Insights      
(1) Summary View (Historical Analytics)      

(2) Prediction View (At-Risk Customer Targeting)       

5. SQL & PYTHON Code Implementation       
(1) SQL Data Engineering (Google BigQuery)     
   Data quality checks, missing value imputations, and analytical view creations were performed directly in BigQuery.     
   For the complete SQL script, see sql/bigquery_etl.sql      
 (2) Predictive Modeling & Machine Learning:      
   A Random Forest Classifier was trained on historical customer records (vw_ChurnData) and deployed on new onboarding customers (vw_JoinData) to score churn probabilities in advance.        
   For the complete SQL script, see sql/bigquery_etl.sql     

6. Strategic Recommendations     
(1) Proactive Retention: Launch personalized contract-upgrade campaigns for the 383 predicted churners before their first renewal cycle.     
(2) Contract Migration: Transition month-to-month accounts to annual contracts via bundle discounts to target the 46.5% churn segment.     
(3) Competitive Pricing: Benchmark Fiber Optic pricing in high-churn regions (e.g., Uttar Pradesh and Tamil Nadu) to mitigate competitor defection.    
