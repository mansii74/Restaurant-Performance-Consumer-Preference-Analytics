# Restaurant Performance & Consumer Preference Analytics

## 📌 Project Overview

This project focuses on analyzing restaurant performance and consumer dining preferences using real customer rating data from Mexico. The goal is to understand how customer demographics, restaurant attributes, and service factors influence overall satisfaction and to derive actionable insights that support data-driven decision-making in the food service industry.

---

## 📂 Dataset Overview

The dataset is relational and consists of multiple interconnected tables:

### 1. Consumers

* Consumer_ID (Primary Key)
* City, State, Country
* Latitude, Longitude
* Smoker
* Drink_Level
* Transportation_Method
* Marital_Status
* Children
* Age
* Occupation
* Budget

### 2. Consumer Preferences

* Consumer_ID (Foreign Key)
* Preferred_Cuisine

### 3. Restaurants

* Restaurant_ID (Primary Key)
* Name
* City, State, Country, Zip_Code
* Latitude, Longitude
* Alcohol_Service
* Smoking_Allowed
* Price
* Franchise
* Area
* Parking

### 4. Restaurant Cuisines

* Restaurant_ID (Foreign Key)
* Cuisine

### 5. Ratings

* Consumer_ID (Foreign Key)
* Restaurant_ID (Foreign Key)
* Overall_Rating
* Food_Rating
* Service_Rating

---

## 🧩 Data Model (ER Structure)

* One consumer can rate multiple restaurants
* One restaurant can receive multiple ratings
* Restaurants can serve multiple cuisines
* Consumers can have multiple cuisine preferences

This relational structure enables detailed analysis across customer behavior, restaurant features, and rating outcomes.

---

## 🧹 Data Preparation & Cleaning

* Imported datasets using folder-based ingestion
* Standardized categorical values across tables
* Removed duplicates and handled missing values
* Validated relationships between primary and foreign keys

### Calculated Fields

**Age Group**

* Children & Adolescents (≤18)
* Young Adults (19–30)
* Adults (31–45)
* Middle-aged Adults (46–60)
* Seniors (>60)

**Rating Categories**

* Unsatisfactory
* Satisfactory
* Highly Satisfactory

---

## 🔍 Analytical Approach

The analysis is structured across five major dimensions:

1. Customer Demographics
2. Restaurant Location & Infrastructure
3. Dining Preferences & Lifestyle
4. Service & Food Quality
5. Customer Satisfaction Patterns

---

## 📊 Key Insights

### Customer Demographics

* Young adults form the largest consumer group across all states
* Majority of consumers are non-smokers
* Public transportation is the most commonly used travel method

### Restaurant Characteristics

* Most restaurants do not provide parking facilities
* Higher-priced restaurants are more likely to offer parking options
* Non-franchise restaurants dominate across all regions

### Cuisine Preferences

* Mexican cuisine is the most preferred among consumers
* American cuisine is the second most popular choice

### Alcohol & Smoking Trends

* Most restaurants do not serve alcohol
* Smoke-free policies are followed by the majority of restaurants

### Customer Satisfaction

* Strong correlation observed between food quality and overall ratings
* Restaurants with consistent service quality receive higher satisfaction scores
* Alcohol availability shows moderate influence on consumer ratings

---

## 📈 Dashboard Overview

The interactive dashboard includes:

* City and state-wise consumer distribution
* Restaurant performance comparison by price and facilities
* Food, service, and overall rating analysis
* Cuisine popularity and preference trends

Tools Used:

* Power BI / Tableau
* Excel
* Data Modeling & DAX

---

## 🛠 Tools & Technologies

* Power BI / Tableau
* Excel
* SQL (for data understanding)
* Data Modeling
* Data Cleaning & Preprocessing

---

## 🎯 Business Value

This project helps stakeholders:

* Identify factors impacting customer satisfaction
* Optimize restaurant services and pricing strategies
* Understand customer demographics and preferences
* Support data-driven operational and marketing decisions

---

## 📌 Conclusion

The analysis highlights how demographic patterns, dining behavior, and restaurant features collectively influence customer satisfaction. These insights can guide restaurants in improving service quality, optimizing offerings, and enhancing overall customer experience.

---

## 📎 Disclaimer

This project is created for educational and analytical purposes using publicly available datasets. All analysis, modeling, and dashboards were independently designed and implemented.
