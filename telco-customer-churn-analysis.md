# Telco Customer Churn Analysis

## Objective
Telco Company X, faced a customer churned in California branch on last quarter. The survey was conducted for churned user why they not continued the serviced provide by company. The stakeholder wants to know how the scope of user churned and what the main reason which will point out to strategic action plan to tackle this problem.

- Dataset : Telco Customer Churn IBM Dataset from [Kaggle ](https://www.kaggle.com/datasets/yeanzc/telco-customer-churn-ibm-dataset/data)(7043 observations with 33 variables)
- Tools : Python for Data Cleaning, PowerBI for Analysis

<br>

## Overview

<img width="1680" height="347" alt="overview" src="https://github.com/user-attachments/assets/3a67750a-19fb-4161-9756-5978aab298f8" />


- 26.54% of users have churned, representing 30.8% of total monthly charges, equivalent to approximately USD 7.7M in lost value.
  
- Based on churn score distribution (score >65), an additional ~1.3K users from non-churned group are identified as high risk, representing a potential USD 4.5M in monthly charges if no mitigation actions are taken.

<br>

## Churned User Profiling

<img width="1870" height="942" alt="user-profiling" src="https://github.com/user-attachments/assets/12b6889f-c44f-4535-9561-6b1a4c57b04a" />



- **By City** :
    Churn is broadly dispersed across 1,129 cities in California, with an average distribution of ~0.12% per city, indicating a long-tail pattern rather than localized concentration. Los Angeles (4.82%) and San Diego (2.68%) account for the highest shares.
    
- **By Contract Type** :
    The majority of churned users (88.55%) are on month-to-month contracts, a significantly higher proportion than the overall contract distribution, indicating elevated churn risk for flexible contract users.
    
- **By Tenure** :
    Users with 0–6 months tenure exhibit the highest churn rate, with approximately half of users in this cohort churning. Combined with the dominance of month-to-month contracts, this suggests early-stage users—likely in a trial phase—are more prone to churn than long-tenure users.
    
- **By Product Service** :
    Churn is observed across users subscribed to both phone and internet services, with no clear product-specific bias identified.
    
- **By CLTV (Customer Lifetime Value)** :
    CLTV segments were defined based on the overall user distribution (Low, High, Very High). Churn is concentrated in the Low and High CLTV segments, which show similar churn and non-churn distributions and account for USD 4.27M and USD 3.23M in monthly charge losses, respectively. The Very High CLTV segment shows minimal churn (~2%), indicating strong retention among top-value customers.

<br>

## Churned Reason Analysis

<img width="1874" height="949" alt="churn-reason" src="https://github.com/user-attachments/assets/8bd06e83-0dc8-4c33-9b5c-daad32afef4d" />




To improve clarity, the original 20 churn reasons were grouped into **seven broader categories**. The analysis reveals **two primary churn drivers**: Competitor-related factors and Attitude-related factors.

**1. Competitor-Related Churn (Top Driver)**
- Competitor-related churn is fairly evenly split across four reasons, with "Competitor Offered Higher Download Speed" as the leading factor.
   - Within this segment, 71.82% are Fiber Optic users and 28.18% are DSL users, showing that Fiber customers are more sensitive to speed competition.
- Service usage within this category shows low engagement with both free and paid add-on services:
    - 60.78% of new users do not use any free services (e.g., Streaming Movie, Streaming TV).
    - 63.42% of new users do not subscribe to any paid add-on services (e.g., device protection, tech support).
  
    This points to opportunities to increase value perception and engagement before users switch to competitors.

**2. Attitude-Related Churn**
- Attitude-related churn is evenly spread across tenure and CLTV segments, affecting both new and long-tenure users as well as high- and low-value customers. This indicates the factor is not specific to user lifecycle or value.

- Geographically, attitude-related churn follows a long-tail pattern, with slightly higher counts in San Diego (10 cases), Fresno (5), and Los Angeles (5). However, most cities (255) report only a single case each.

<br>

## Targeted User Segmentation

<img width="1872" height="941" alt="targeted-user" src="https://github.com/user-attachments/assets/5d76758c-95c3-4310-9dbc-0edc742f34dc" />



By segmenting churned users across three key dimensions—monthly charges, tenure, and CLTV—we identify the 7K–10K monthly charge segment as the highest priority, accounting for 55.4% of total profit loss from only 26.97% of churned users. This approach can be expanded incrementally based on budget, with prioritization in the following order: (1) monthly charges 7K–10K, (2) tenure 3–5 years, and (3) high CLTV.

<br>

## Next Step & Recommendations

1. Overall Churn Recovery Prioritization
    - Focus churn recovery efforts on high-value users, starting with the 7K–10K monthly charge segment, which drives a disproportionate share of profit loss. Expand targeting incrementally based on budget, followed by users with 3–5 years tenure and high CLTV.
2. Actions for Competitor-Related Churn
    - Since speed-related churn is concentrated in the Fiber Optic segment, conduct deeper product-level analysis to assess performance gaps, competitive positioning, and customer expectation alignment.
    - For early-tenure users (<6 months), promote free services and selectively offer discounted add-on services to improve early engagement and strengthen retention.
3. Actions for Attitude-Related Churn (Targeted & Personalized)
    - Apply personalized recovery outreach for attitude-related churn cases, focusing on a smaller, high-impact subset of users where individual intervention is more likely to influence retention.
    - Implement targeted training on soft skills, empathy, and professional communication across all teams, with enhanced focus and evaluation in the top five cities.
