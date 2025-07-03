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
- Removed duplicates using Product ID as an Identifier 
- Handled missing values (discount_percent, rating_count)
- Used text to column to split category
2. **Calculated Column;**
- Price Bucket: =IF([@[discounted_price]]<200,"<₹200",IF(OR([@[discounted_price]]=200,[@[discounted_price]]<=500),"₹200-₹500",">₹500"))
- Total Potential Revenue: =actual_price * rating_count
- Discount Bucket; =IF([@[discount_percentage]]<=10%,"0-10%",IF([@[discount_percentage]]<=20%,"11-20%",IF([@[discount_percentage]]<=30%,"21-30%",IF([@[discount_percentage]]<=40%,"31-40%",IF([@[discount_percentage]]<=50%,"41-50%",IF([@[discount_percentage]]<=60%,"51-60%",IF([@[discount_percentage]]<=70%,"61-70%",IF([@[discount_percentage]]<=80%,"71-80%",IF([@[discount_percentage]]<=90%,"81-90%","91-100%")))))))))
- Discount Bucket for 50% or more; =IF([@[discount_percentage]]>=50%,"Yes","No")

3. **Pivot Tables:**
- Created a master Pivot Table on Sheet "Pivot" to answer the business quesions

![![Screenshot (97)](https://github.com/user-attachments/assets/291a22f4-3b10-41bc-a253-361f40f6802e)
Screenshot (76)](https://github.com/user-attachments/assets/356cc85e-cd28-4e16-a3f2-cf3e10082226)

---

### 📊 Dashboard Creation in Excel
 - Bar and pie charts for quick insights
![Screenshot (96)](https://github.com/user-attachments/assets/2b4818c9-43d9-4aa1-bff2-a1b96fde2cfd)
![Screenshot (95)](https://github.com/user-attachments/assets/4992003e-37e1-44a1-bcc8-b6b952597693)

---
### 💡Key Insights
- Musical Instrument enjoy the highest average discount.
-  Electronics dominate review volume and it has the highest potential revenue
-  49% of the total Product is with a discount of 50% or more.
-  Products priced ₹200–₹500 account for 25% of listings.
- There is 308 Products with less than 1000 Reviews.
- B09ZHCJDP1, B0BQRJ3C47, B0BP7XLX48 are products with the highest rating.
- Products with 80-90% discount percentage has the lowest rating.
---
### Conclusion
This dashboard offers a comprehensive overview of product performance across various categories on Amazon. It highlights key patterns in pricing, discounts, customer reviews, and product ratings. By identifying top-performing products and categories, as well as areas with low engagement or high discounts but poor ratings, sellers can make informed decisions. These insights empower e-commerce teams to refine pricing strategies, enhance product quality, and tailor marketing efforts to boost customer satisfaction and drive revenue growth.



 

  
