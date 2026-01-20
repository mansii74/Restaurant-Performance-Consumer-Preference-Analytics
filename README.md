# Restaurant Performance & Consumer Preference Analytics

## Table of Content

* Case Study
* Dataset Description
* ER Diagram
* Data Cleaning
* Data Analysis
* Dashboard

---

## Case Study

This project analyzes restaurant ratings in Mexico using feedback from real consumers. It combines customer demographics, dining preferences, restaurant attributes, and service quality to understand factors influencing customer satisfaction and overall restaurant performance.

---

## Dataset Description

The dataset consists of multiple relational tables:

### Consumers

* Consumer_ID – Unique consumer identifier
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

The ER diagram illustrates relationships between consumers, restaurants, ratings, and cuisines using unique identifiers to enable structured analysis.

---

## Data Cleaning

### Data Import Steps

* Load datasets using folder-based ingestion
* Expand and transform files
* Remove duplicates and handle missing values
* Validate table relationships

### Calculated Fields

**Age Group**
Children & Adolescents | Young Adults | Adults | Middle-aged Adults | Seniors

**Rating Categories**
Unsatisfactory | Satisfactory | Highly Satisfactory

---

## Data Analysis

### Local Insights

* Majority of consumers belong to San Luis Potosí
* Young adults form the largest demographic group
* Most consumers are non-smokers
* Limited parking availability across restaurants

### Dining Insights

* High-priced restaurants are more likely to offer parking
* San Luis Potosí has the highest restaurant count
* Franchise and non-franchise restaurants show similar rating patterns
* Mexican cuisine is the most preferred

### Hospitality Insights

* Most restaurants do not serve alcohol
* Public transport is the most common travel mode
* Alcohol service shows moderate influence on ratings
* Majority of restaurants follow smoke-free policies

### Behavior Insights

* Students form the majority of consumers
* Drinking habits vary across states
* Budget levels are mostly low to medium

### Review Insights

* Food quality and service strongly impact overall ratings
* Certain restaurants consistently receive higher satisfaction scores

---

## Dashboard

The dashboard presents interactive insights on:

* Consumer demographics
* Restaurant distribution by state
* Cuisine preferences
* Food, service, and overall ratings
* Restaurant performance comparison

---

## Disclaimer

This project is created for educational and analytical purposes using publicly available data. All analysis and dashboards were independently designed.
