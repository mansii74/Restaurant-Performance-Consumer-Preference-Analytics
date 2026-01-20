# Restaurant Performance & Consumer Preference Analytics

## Table of Content

* [Case Study](#case-study)
* [Dataset Description](#dataset-description)
* [ER Diagram](#er-diagram)
* [Data Cleaning](#data-cleaning)
* [Data Analysis](#data-analysis)
* [Dashboard](#dashboard)

---

## Case Study

This project analyzes restaurant performance and consumer dining preferences using real customer rating data from Mexico. The objective is to understand how customer demographics, restaurant attributes, and service quality influence overall customer satisfaction and restaurant performance.

---

## Dataset Description

The dataset consists of multiple relational tables capturing consumers, restaurants, cuisines, and ratings.

### Consumers

* Consumer_ID – Unique identifier for each consumer
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

### Consumer Preferences

* Consumer_ID
* Preferred_Cuisine

### Ratings

* Consumer_ID
* Restaurant_ID
* Overall_Rating
* Food_Rating
* Service_Rating

### Restaurants

* Restaurant_ID
* Name
* City, State, Country
* Zip_Code
* Latitude, Longitude
* Alcohol_Service
* Smoking_Allowed
* Price
* Franchise
* Area
* Parking

### Restaurant Cuisines

* Restaurant_ID
* Cuisine

---

## ER Diagram

The ER diagram below illustrates the relationships between consumers, restaurants, ratings, and cuisines.

![ER Diagram](images/ER_diagram.png)

---

## Data Cleaning

### Steps to Import Data as a Folder

* Get Data → More → All → Folder → Connect
* Select the folder path containing the dataset and click **OK**
* Click **Transform Data** to open Power Query
* Duplicate files and expand content using the **Binary** option
* Repeat the process for all datasets and validate relationships

### Calculated Fields

**Age Group**

```DAX
AgeGroup = 
SWITCH(
    TRUE(),
    consumers[Age] <= 18, "Children and Adolescents",
    consumers[Age] <= 30, "Young Adults",
    consumers[Age] <= 45, "Adults",
    consumers[Age] <= 60, "Middle-aged Adults",
    "Seniors"
)
```

**Service Rating Category**

```DAX
Service_Rating_Category = SWITCH(
    TRUE(),
    ratings[Service_Rating] = 0, "Unsatisfactory",
    ratings[Service_Rating] = 1, "Satisfactory",
    "Highly Satisfactory"
)
```

**Overall Rating Category**

```DAX
Overall_Rating_Category = SWITCH(
    TRUE(),
    ratings[Overall_Rating] = 0, "Unsatisfactory",
    ratings[Overall_Rating] = 1, "Satisfactory",
    "Highly Satisfactory"
)
```

**Food Rating Category**

```DAX
Food_Rating_Category = SWITCH(
    TRUE(),
    ratings[Food_Rating] = 0, "Unsatisfactory",
    ratings[Food_Rating] = 1, "Satisfactory",
    "Highly Satisfactory"
)
```

---

## Data Analysis

### Local Insights

* Majority of consumers belong to San Luis Potosí
* Young adults form the largest age group across states
* Most consumers are non-smokers
* Limited parking availability across restaurants

### Dining Insights

* High-priced restaurants are more likely to provide parking
* San Luis Potosí has the highest number of restaurants
* Franchise and non-franchise restaurants show similar rating patterns
* Mexican cuisine is the most preferred cuisine

### Hospitality Insights

* Most restaurants do not serve alcohol
* Public transport is the most common travel mode
* Alcohol availability has moderate impact on ratings
* Majority of restaurants follow smoke-free policies

### Behavior Insights

* Students form the majority of consumers
* Drinking habits vary across regions
* Budget levels are mostly low to medium

---

## Dashboard

### Consumer Demographics Overview

![Dashboard](images/d1.jpg)

### Restaurant Distribution & Pricing

![Dashboard](images/d2.jpg)

### Cuisine Preference Analysis

![Dashboard](images/d3.jpg)

### Food & Service Rating Analysis

![Dashboard](images/d4.jpg)

### Overall Restaurant Performance

![Dashboard](images/d5.jpg)

---

## Disclaimer

This project is created for educational and analytical purposes using publicly available data. All analysis and dashboards were independently designed and implemented.
