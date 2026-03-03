# 🏙️ Airbnb New York 2024 – Pricing & Market Analysis using Python

## 📌 Introduction

The Airbnb market in New York City is highly competitive, with thousands of listings across different boroughs. Pricing varies significantly depending on location, property size, and listing characteristics.

This project performs an end-to-end **Exploratory Data Analysis (EDA)** on the Airbnb New York 2024 dataset using Python to uncover pricing patterns, borough-level trends, and normalized cost insights.

---

## ❓ Problem Statement

Raw listing prices alone do not provide a meaningful comparison because:

- Listings have different numbers of beds  
- Some properties contain extreme price outliers  
- Pricing varies significantly across boroughs  
- Central locations may inflate overall averages  

Without proper cleaning and normalization, pricing comparisons can be misleading.

---

## 🎯 Project Goal

The objectives of this project were to:

- Clean and preprocess the Airbnb NYC dataset  
- Remove extreme pricing outliers  
- Engineer a **price-per-bed** metric for fair comparison  
- Compare borough-level pricing trends  
- Extract actionable insights from the data  

---

## 📂 Dataset Information

- **Dataset:** Airbnb New York Listings 2024  
- **Total Listings Analyzed:** 20,770  
- **Format:** CSV  

### Key Features Used:
- `price`
- `beds`
- `neighbourhood_group`
- `room_type`
- `availability_365`
- `number_of_reviews`
- `rating`

---

## 🛠️ Tools & Technologies Used

- **Python**
- **Pandas** – Data cleaning & aggregation  
- **NumPy** – Numerical operations  
- **Jupyter Notebook** – Analysis environment  

---

## 🔍 Methodology

### 1️⃣ Data Cleaning

- Converted `price` and `beds` columns to numeric format  
- Handled missing and invalid values  
- Removed extreme outliers (price < $1500)  
- Addressed zero-bed listings to prevent division errors  

---

### 2️⃣ Feature Engineering

Created a normalized pricing metric:

```python
price_per_bed = price / beds
```
---

## 3️⃣ Aggregation & Grouping

Used Pandas `groupby()` to compute:

- Average price by neighbourhood group  
- Average price per bed by borough  
- Percentage comparison across boroughs  

---

## 📊 Key Outcomes 

### 🔢 Overall Pricing Statistics

- **Total Listings:** 20,770  
- **Average Listing Price:** $187.71  
- **Price Range (before filtering):** $10 – $100,000  
- **Outlier Filter Applied:** Price < $1500  

---

### 🏙️ Average Price by Borough

| Borough         | Average Price ($) |
|-----------------|-------------------|
| Manhattan       | 204.15 |
| Brooklyn        | 155.14 |
| Queens          | 124.67 |
| Staten Island   | 115.54 |
| Bronx           | 92.76 |

- Manhattan is **31% more expensive than Brooklyn** on average.

---

### 🛏️ Average Price Per Bed (Engineered Metric)

| Borough         | Avg Price per Bed ($) |
|-----------------|-----------------------|
| Manhattan       | 138.71 |
| Brooklyn        | 99.79 |
| Queens          | 76.34 |
| Staten Island   | 71.88 |
| Bronx           | 63.52 |

- Manhattan charges **~39% more per bed than Brooklyn**.  
- Bronx has the lowest normalized cost per bed.  

---

## 📈 Business Insights

- Location strongly influences Airbnb pricing.  
- Manhattan dominates premium pricing across both raw price and normalized price-per-bed.  
- Price-per-bed is a more reliable metric than raw listing price.  
- Outer boroughs present lower-cost hosting opportunities.  
- Removing outliers provides a more realistic market representation.  

---

## 📸 Project Output Screenshot

After uploading your image to the repository, add:

```markdown
![Borough Price Analysis](Availability 365 distribution.png)
