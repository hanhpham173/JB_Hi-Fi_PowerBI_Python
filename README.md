# 📺 JB Hi-Fi TV Product Insights Dashboard - Power BI Project

## 📊 Overview  
This Power BI project delivers **interactive and detailed insights** into TV product performance on the JB Hi-Fi platform. It includes analysis by **brand, price range, customer ratings, promotions**, and **free delivery options**. The dashboard highlights key metrics such as the total number of products, average ratings, total customer reviews, and category-specific trends.

The insights generated help JB Hi-Fi understand **customer preferences**, **market trends**, and make **data-driven decisions** to optimize inventory, enhance customer satisfaction, and improve pricing and promotional strategies.

---

## 🎯 Project Goals

- Identify the most popular brands based on ratings and product availability  
- Highlight top-rated brands and products  
- Compare average ratings across different price groups  
- Track products with free delivery and consistent availability  
- Analyze review counts to evaluate customer satisfaction  
- Explore overall customer sentiment via rating distribution  
- Assess the price–rating correlation to understand price sensitivity  
- Recommend promotional and inventory strategies based on data insights  

---

## 🔄 Data Collection & Transformation

### ✅ Web Scraping (Python - Selenium & BeautifulSoup)
- Used Selenium to automate navigation and scrolling on the [JB Hi-Fi TV collection page](https://www.jbhifi.com.au/collections/tvs)
- Scraped product details:  
  - Product Name  
  - Brand  
  - Price  
  - Promotions  
  - Number of Reviews  
  - Ratings  
  - Free Delivery flag  
- Saved data as a CSV for import into Power BI  

📄 Python Script: [`jb_scraping.py`](jb_scraping.py)  
📊 Sample Data File: `jbhifi_products_data.csv`  

---

## 🗃️ Data Model

![Data Model](https://raw.githubusercontent.com/hanhpham173/JB_Hi-Fi_PowerBI_Python/d7f8f606a7ac554e2cfb8905fe8d85131660e44b/model.JPG)

Data was modeled into 4 separate tables:

- `Promo`: Promotion and Promotion ID  
- `Brand`: Brand Name and Brand ID  
- `Size`: Screen Size and Size ID  
- `TV`: Product-level data (joined with Brand, Size, and Promo)

This star schema model improves query performance and enables flexible slicing/filtering in Power BI.

---

## 📈 Dashboard Features

### Executive Brand Overview

- **Total Products vs. Avg. Rating by Brand**  
  Samsung and TCL have the most models; LG and Sony lead in ratings  
- **Average Rating by Brand**  
  LG, Sony, and Samsung all rate above 4.5  
- **Promotion Analysis**  
  Over 75% of products include “3 months of Apple TV+” offer  
- **Price vs. Rating Correlation (by Brand)**  
  Slight positive trend – higher-priced TVs tend to receive better ratings  

![Dashboard Screenshot](https://raw.githubusercontent.com/hanhpham173/JB_Hi-Fi_PowerBI_Python/d7f8f606a7ac554e2cfb8905fe8d85131660e44b/jb_sc1.JPG)


### Product Insights & Comparisons

- **Top Rated Products**  
  TVs from Hisense, LG, and Samsung with 5.0 ratings  
- **Most Reviewed Products**  
  Sony leads with 1,564 reviews  
- **Lowest Rated Products**  
  Samsung 43” CU8000 (rating: 1.0) and Samsung 32” T5300 (rating: 1.9)  
- **Least Reviewed Products**  
  Some high-end models have only 1 review, suggesting limited feedback  
- **Price vs. Rating Correlation (by Product)**  
  Scatter plot shows that higher prices don’t always guarantee better ratings

![Additional Dashboard Screenshot](https://raw.githubusercontent.com/hanhpham173/JB_Hi-Fi_PowerBI_Python/d7f8f606a7ac554e2cfb8905fe8d85131660e44b/jb_sc2.JPG)


### Product Details Table

A comprehensive view of each product including:
- Brand  
- Name  
- Size  
- Promotion  
- Price  
- Free Delivery  
- Customer Rating  

![Product Insights Screenshot](https://raw.githubusercontent.com/hanhpham173/JB_Hi-Fi_PowerBI_Python/d7f8f606a7ac554e2cfb8905fe8d85131660e44b/jb_sc3.JPG)


---

## 💡 Business Recommendations

- **Expand Inventory for High-Rated Brands**: LG, Sony, and Samsung show strong customer satisfaction  
- **Use Promotions to Boost Lower-Rated Brands**: Brands like Blaupunkt could benefit from targeted offers  
- **Promote Premium High-Rated TVs**: Higher-end products tend to have better reviews – justify price via marketing  
- **Optimize Promotion Strategy**: Focus on expanding effective promotions like “Online Only” or bundle offers  
- **Align Inventory with Demand**: Reallocate stock toward highly-rated and frequently reviewed models  
- **Collaborate with Vendors on Low-Rated Products**: Address quality issues based on customer feedback  
- **Monitor Trends Over Time**: Customer sentiment and market preferences may evolve — stay agile  

---

## ✅ Conclusion

This project showcases advanced Power BI skills and demonstrates the end-to-end workflow from **web scraping** to **data modeling** and **interactive dashboard development**. The dashboard provides actionable insights to help **optimize product strategy** at JB Hi-Fi and improve customer satisfaction.

---

## 🛠️ Tools Used

- **Power BI Desktop**  
- **Python (Selenium, BeautifulSoup, pandas)**  
- **DAX (Data Analysis Expressions)**  
- **Power Query**  
