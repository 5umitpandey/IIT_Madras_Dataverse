# IIT Madras | Dataverse Hackathon

![6930a51ac4598_dataverse-the-business-analytics-challenge](https://github.com/user-attachments/assets/b1ee218d-2a35-4ba5-a14e-2adbdac20e6c)


# Food Restaurant Data Intelligence & Market Strategy Analysis

This project presents an end to end data analysis and market intelligence framework built on a global food restaurant dataset.  
The objective is to uncover strategic insights across markets, cuisines, pricing, engagement, and growth opportunities using data driven reasoning.

The analysis was developed as part of a hackathon submission and focuses on **business impact**, not just exploratory analysis.

---

## Dataset Overview

The dataset represents a large scale view of restaurant ecosystems across multiple countries and cities.

### Key Statistics

- **Total restaurants**: 9,551  
- **Countries covered**: 15  
- **Cities covered**: 141  
- **Restaurants in India**: 8,652  
- **India share**: 90.6 percent  
- **Rated restaurants**: 7,403  
- **Rating coverage**: 77.5 percent  
- **Final feature dimensions**: 22  

![Restaurants By Countries](https://github.com/5umitpandey/IIT_Madras_Dataverse/blob/main/Images/Rest_By_Country.png)

This immediately establishes India as the dominant market in both scale and engagement.

---

## Strategic Market Positioning

India is the core driver of platform activity.

More than 90 percent of restaurants belong to India, which means:
- Any improvement in ranking, pricing, discovery, or quality directly impacts the majority of users
- India is the most effective market for experimentation and optimization
- Non India markets are better suited for niche and premium strategies

![India Density Map](https://github.com/5umitpandey/IIT_Madras_Dataverse/blob/main/Images/India_dense_map.png)

**Conclusion**  
India should be treated as the primary experimentation and monetization market.

---

## Data Cleaning & Standardization

Strong insights depend on clean data. The following steps were applied to ensure reliability.

### Country and Currency Fixes

- Numeric country codes were mapped to country names
- Zero missing values after mapping
- Incorrect Philippines currency was fixed
- All costs were standardized to INR for fair comparison

### Column Optimization

Removed non informative columns including:
- Locality Verbose  
- Rating color  
- Rating text  
- Switch to order menu  
- Country code  

**Business Impact**  
Standardized pricing and clean features enable reliable pricing intelligence and cross market analysis.

---

## Cross Country Cost Structure Analysis

Average cost for two was analyzed across countries after INR normalization.

### Market Segmentation

- **India**  
  - Average cost around 623 INR  
  - Large volume market  
  - Best suited for scale driven growth  

- **United States and emerging markets**  
  - Average cost between 2,222 and 2,353 INR  
  - Medium scale  
  - Suitable for feature testing  

- **UAE and United Kingdom**  
  - Average cost between 4,113 and 5,785 INR  
  - Small sample size  
  - Premium positioning markets  

![avg_cost_country](https://github.com/5umitpandey/IIT_Madras_Dataverse/blob/main/Images/avg_cost_country.png)

**Insight**  
Non India markets have limited samples and should focus on premium and niche strategies rather than scale.

---

## Cuisine Intelligence & Portfolio Strategy

Restaurants serve multiple cuisines stored as comma separated values.  
A hybrid feature engineering approach was used to preserve restaurant identity while enabling cuisine level analysis.

### Feature Engineering Flow

1. Original dataset with 9,551 restaurants  
2. Controlled cuisine explosion to 19,710 cuisine rows  
3. Validation of 145 unique cuisines  

---

## Popularity vs Satisfaction Gap

### Most Popular Cuisines

- North Indian: 3,960 restaurants  
- Chinese: 2,735 restaurants  
- Fast Food: 1,986 restaurants  

### Highest Rated Cuisines with scale

- Italian: 3.56 average rating  
- Continental: 3.52 average rating 
- Cafe: 3.32 average rating  

### Popular but Underperforming

- North Indian: 2.51 rating  
- Chinese: 2.62 rating  
- Fast Food: 2.56 rating  

**Key Insight**  
Popularity does not imply satisfaction.

Highly popular cuisines require quality standardization, while high rated cuisines should be boosted in discovery systems.

![cuisine_rating_comparison](https://github.com/5umitpandey/IIT_Madras_Dataverse/blob/main/Images/AvgRating_VS_NoOfRest.png)

---

## Menu Structure & Engagement Dynamics

Menu diversity plays a critical role in engagement and ratings.

### Cuisine Count Distribution

![Cusine Count By Resturants](https://github.com/5umitpandey/IIT_Madras_Dataverse/blob/main/Images/cusineperrest.png)

### Engagement Patterns

- High engagement cuisines consistently exceed 3.5 rating  
- Low engagement cuisines cluster below 3.0 rating  

**Recommendation**  
Recommendation systems should balance popularity with engagement metrics, not popularity alone.

---

## City Level Dynamics in India

### High Volume Cities

![city_visibility_gap](https://github.com/5umitpandey/IIT_Madras_Dataverse/blob/main/Images/Unrated_Vs_City.png)

**Insight**  
This is a discovery problem, not a demand problem.  
User engagement exists but ratings are not being captured.

---

## Locality Level Quality Variation

City level strategies are too coarse.

### Example Localities

- Connaught Place  
  - 3.69 average rating  

- Rajouri Garden  
  - 3.59 average rating  

- Shahdara  
  - 1.41 average rating  


**Business Impact**  
Locality specific onboarding, audits, and promotions deliver higher ROI than city wide actions.

---

## 📈 Pricing Dynamics & Rating Drivers

### Model Performance

- RMSE: 0.41 on a 5 point scale  
- Strong predictive accuracy  

### Correlations

- Price range vs rating: 0.44  
- Votes vs rating: 0.31  

### Feature Importance

- Votes: 71 percent  
- Average cost for two: 20 percent  
- Online delivery: 4 percent  
- Price range: 3 percent  
- Table booking: 2 percent  

![feature_importance](https://github.com/5umitpandey/IIT_Madras_Dataverse/blob/main/Images/Feature_Importance.png)

**Strategic Conclusion**  
Engagement is the single strongest driver of ratings.  
Investment in engagement tools outperforms cosmetic feature additions.

---

### Service Availability Impact on Restaurant Ratings

This section analyzes how **online delivery** and **table booking** features influence restaurant ratings and customer engagement.
The visuals compare rating distributions for restaurants with and without these services, highlighting their relative impact.


| Online Delivery Impact | Table Booking Impact |
|------------------------|----------------------|
| ![online_delivery_impact](https://github.com/5umitpandey/IIT_Madras_Dataverse/blob/main/Images/Ratings_vs_online_delivery.png) | ![table_booking_impact](https://github.com/5umitpandey/IIT_Madras_Dataverse/blob/main/Images/ratings_Vs_Table.png) |

---



## Hidden High Quality Growth Opportunities

Certain cuisines show strong ratings with limited competition.

### High Potential Cuisines

| Cuisine          | Restaurant Count | Average Rating |
|------------------|------------------|----------------|
| Sandwich         | 53               | 4.086038       |
| Steak            | 62               | 3.985484       |
| Sushi            | 75               | 3.973333       |
| Breakfast        | 41               | 3.965854       |
| Mediterranean    | 112              | 3.948214       |
| Bar Food         | 39               | 3.933333       |
| Indian           | 70               | 3.918571       |
| European         | 148              | 3.910811       |
| BBQ              | 33               | 3.903030       |
| Seafood          | 174              | 3.862069       |


**Strategy**  
These cuisines are ideal for premium discovery, editorial promotion, and supply expansion.

---

## Final Takeaways

- India is the core growth and experimentation market  
- Engagement drives ratings more than pricing or features  
- Popular cuisines need quality improvement  
- High quality niche cuisines need visibility  
- Locality level actions outperform city level strategies  

---

## Notebooks and Code

All notebooks used for data cleaning, feature engineering, modeling, and analysis are available here:

🔗 **Drive Link** : https://drive.google.com/drive/folders/1KS_0ilJyk-KP8BpQ8iAdJ--b2_5zZUYC

---

## Team

**Team Name**: ASHSUM
<br>
**Team Members**:  
<table>
<tr>
<td align="center">
<img src="https://github.com/ashir1s.png" width="100px;" alt="Ashirwad Sinha"/><br/>
<a href="https://github.com/ashir1s">Ashiwad Sinha</a>

</td>

<td align="center">
<img src="https://github.com/5umitpandey.png" width="100px;" alt="Sumit Pandey"/><br/>
<a href="https://github.com/5umitpandey">Sumit Pandey</a>
</td>
</tr>
</table>


This project was built as a hackathon submission with a strong focus on real world business decision making using data.
