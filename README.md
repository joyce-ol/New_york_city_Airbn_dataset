# 🏙️ Airbnb NYC 2019 Data Cleaning Project

## 📌 Overview
This project focuses on cleaning and preparing the **Airbnb NYC 2019 dataset** for analysis.  
The dataset contains listings information such as price, location, availability, and reviews.  

The goal of this project is to ensure the dataset is:
- **Accurate** – free from inconsistencies and errors  
- **Consistent** – standardized formatting across all columns  
- **Reliable** – missing values handled and outliers treated  

---

## ⚙️ Data Cleaning Steps

### 1. Standardize Column Names
- Converted column names to lowercase  
- Replaced spaces with underscores (`"room type"` → `"room_type"`)  

### 2. String Formatting
- Stripped extra whitespace  
- Converted all text to lowercase  
- Converted `last_review` column to proper datetime format  

### 3. Handle Missing Values
- Dropped rows with missing `name` or `host_name`  
- Filled `reviews_per_month = 0.0` where `number_of_reviews = 0`  

### 4. Remove Duplicates
- Removed duplicate records to maintain uniqueness  

### 5. Consistent Formatting
- Standardized categorical columns using `.title()`, e.g.  
  - `"brooklyn"` → `"Brooklyn"`  
  - `"entire home/apt"` → `"Entire Home/Apt"`  

### 6. Outlier Treatment
- Defined an **IQR-based capping function** to handle extreme values  
- Applied outlier capping to:
  - `price`  
  - `minimum_nights`  
  - `availability_365`  

### 7. Export Cleaned Data
- Saved the cleaned dataset as **`cleaned_AB_NYC_2019.csv`**

---

## 📂 Project Structure
