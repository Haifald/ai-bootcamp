# Airbnb Listings — Exploratory Data Analysis

## Project Overview

Exploratory Data Analysis of **279,712 Airbnb listings across 10 cities**.

The analysis focuses on listing prices and explores how factors such as capacity, room type, amenities, host characteristics, reviews, and location are related to price.

A few data challenges were also addressed, including different currencies across cities, missing values, and invalid values in some columns.

## Objective

The dataset does not have a specific target variable, so **price** was selected as the main variable of interest.

Since listings come from different cities and prices are recorded in different currencies, raw prices cannot be compared directly. A city-relative price index was created to make comparisons within each city more meaningful.

The analysis then examined the relationship between price and different listing characteristics.

## Dataset

[Airbnb Listings Dataset (Kaggle)](https://www.kaggle.com/datasets/ulrikthygepedersen/airbnb-listings)

* **279,712 listings**
* **33 features**
* **10 cities:** Paris, New York, Sydney, Rome, Rio de Janeiro, Istanbul, Mexico City, Bangkok, Cape Town, and Hong Kong

## Analysis Highlights

* Created a city-relative price index using `price ÷ city median price`
* Examined missing values, duplicates, data types, invalid values, and outliers
* Identified and handled a placeholder value (`2,147,483,647`) in `maximum_nights`
* Created new features from amenities, property types, and host information
* Grouped 144 property types into 5 broader categories
* Used **Spearman correlation** to examine relationships between numerical variables
* Compared prices across capacity, room type, amenities, host status, reviews, and neighborhoods
* Examined interactions between variables, including **Superhost × room type**

## Key Findings

1. **Capacity has the strongest relationship with price** — `accommodates` (0.53) and `bedrooms` (0.49) had the highest numerical correlations with price.

2. **Review scores showed little relationship with price** — the seven review dimensions had correlations between −0.02 and +0.01.

3. **The relationship between Superhost status and price differs by room type** — the Superhost effect was positive for entire places and hotel rooms, but slightly negative for private and shared rooms.

4. **Neighborhood has a strong effect on relative price** — some neighborhoods were priced between 1.2x and 8.9x their city's median price.

5. **Missing values were not automatically imputed** — around 33% of listings had no reviews, while 34–46% had missing host-response information. These missing values were kept because they may reflect characteristics such as newer listings.

## Tools

`Python` · `Pandas` · `NumPy` · `Matplotlib` · `Seaborn`

## Project Structure

```text
EDA_Airbnb/
├── EDA_Airbnb.ipynb      → Full analysis
├── Presentation.pdf      → Project presentation
└── README.md
```
