# 📊 Amazon-Product-Analysis
This is a Microsoft Excel project for Amazon product review analysis, it includes an Excel interactive dashboard and a pivot table that  answers the business questions.

## 📌 Project Objective
To support sellers on Amazon with data‑driven recommendations on product improvement, marketing strategies, and customer engagement.

## 📂 Dataset Used
- Source: Scraped Amazon product pages (internal pipeline)
- Records: 1,465
- Fields: 16 columns — including product details (Product ID, Product name, category, actual price, discount price,discount percentage, rating, review ID, product link) and aggregated reviewer data (review_count, rating_count, etc.)

## 🎯 Objectives/ Business Questions
- Average discount percentage by product category
- Product count per category
- Total number of reviews per category
- Products with the highest average ratings
- Average actual vs. discounted price by category
- Products with the highest number of reviews
- Count of products with ≥ 50 % discount
- Distribution of product ratings (e.g., how many products are rated 3.0, 4.0, etc.)
- Total potential revenue (actual_price × rating_count) by category
- Unique products per price‑range bucket (<₹200, ₹200–₹500, >₹500)
- Relationship between rating and discount level
- Products with fewer than 1,000 reviews
- Categories hosting the highest discounts
- Top 5 products by combined rating & review volume

  ## 🔄 Process
1. **Data Cleaning & Preparation:**
- Imported amazon product review file into Microsoft Excel.
- Removed duplicates udisin Product ID as Identifier 
- Handled missing values (discount_percent, rating_count)
- Used text to column to split category
     
  
