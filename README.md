1. Customer Churn Analysis & Predictive Modeling   
An end-to-end data analytics and machine learning framework combining Google BigQuery SQL, a Random Forest Classifier in Python, and an interactive Power BI Dashboard to identify historical churn drivers and predict at-risk customers before they churn.

2. Executive Summary & Key Metrics    
Analytic overview across a customer base of 6,418 records:        
（1）Key Metrics: 6,418 Total Customers | 411 New Joiners | 1,732 Total Churned | 27.0% Churn Rate.           
（2）Primary Churn Drivers: Month-to-month contracts (46.53% churn rate), Competitor defection (44% of total churn), and Fiber Optic service vulnerabilities (41.10% churn rate).           
（3）Predictive Impact: The trained model identified 383 high-risk new joiners (Predictions.csv), enabling targeted retention campaigns prior to account renewal.             

3. Pipeline Architecture & Tech Stack                
[ Raw Data ] ──> [ BigQuery SQL (ETL) ] ──> [ Production Views ] ──> [ Random Forest ML ] ──> [ Power BI Dashboard ]              
(1) Data Warehouse: Google BigQuery (SQL)        
(2) Machine Learning: Python (Pandas, Numpy, Seaborn, Matplotlib, Scikit-Learn)       
(3) Business Intelligence: Power BI        

4. Dashboards & Predictive Insights      
<table border="0" width="100%">
  <!-- 第一行：写标题（两列会自动分开） -->
  <tr>
    <td align="center" width="50%"><b>(1) Summary View (Historical Analytics)</b></td>
    <td align="center" width="50%"><b>(2) Prediction View (At-Risk Customer Targeting)</b></td>
  </tr>
  <!-- 第二行：放图片 -->
  <tr>
    <td align="center" width="50%">
      <img src="https://github.com/user-attachments/assets/4ee632f1-efc9-4747-8e2c-eb04fa8f96d7" style="width:100%;" />
    </td>
     <td align="center" width="50%">
      <img src="https://github.com/user-attachments/assets/8d13a47d-d67b-4460-bde3-3caaa3b8da27" style="width:100%;" />
    </td>
  </tr>
</table>
For the full interactive Power BI dashboard, download the `.pbix` file here: 
👉 [Download churn analysis.pbix](./churn%20analysis.pbix)      

5. SQL & Python Code Implementation       
(1) SQL Data Engineering (Google BigQuery)     
   Data quality checks, missing value imputations, and analytical view creations were performed directly in BigQuery.     
   For the complete SQL script, see [ETL_Process_in_BigQuery.sql](./ETL_Process_in_BigQuery.sql).         
(2) Predictive Modeling & Machine Learning                     
   A Random Forest Classifier was trained on historical customer records (vw_ChurnData) and deployed on new onboarding customers (vw_JoinData) to score churn probabilities in advance, with Overall Accuracy: 85%.         
    For the complete Python script, see [Churn Prediction.py](./Churn%20Prediction.py).    
  
 Model evaluation report (showing an accuracy of 85%).          
   <img width="433" height="167" alt="截屏2026-08-13 19 28 07" src="https://github.com/user-attachments/assets/b964f464-c5a6-40c8-900c-be1d57ec696b" />       
   
Churn feature importance chart (showing that "contract type" and "total charges" are the key factors driving customer churn).       
   <img width="4246" height="1634" alt="feature_importance" src="https://github.com/user-attachments/assets/2f45af21-146e-4a9a-a02e-445ef50cd288" />      

  
6. Strategic Recommendations     
(1) Proactive Retention: Launch personalized contract-upgrade campaigns for the 383 predicted churners before their first renewal cycle.     
(2) Contract Migration: Transition month-to-month accounts to annual contracts via bundle discounts to target the 46.5% churn segment.     
(3) Competitive Pricing: Benchmark Fiber Optic pricing in high-churn regions (e.g., Uttar Pradesh and Tamil Nadu) to mitigate competitor defection.    
