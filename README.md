## ☕ Coffee Shop Sales Dashboard

## 📌 Overview
The **Coffee Shop Sales Dashboard** built in **Power BI** offers a detailed, interactive view of sales data for a coffee shop. The dashboard helps identify top-performing products, locations, and trends across different time periods and product segments.

![Dashboard Preview](./Screenshot%202025-04-09%20190738.png)

## 🧩 Key Features
- 📅 Monthly Revenue Trends to identify seasonal patterns  
- 🛍 Revenue by Product & Category to track what’s selling the most  
- 📍 Store-wise Revenue Distribution for performance comparison  
- 🧃 Sales by Size to understand customer preferences  
- 🔄 Dynamic filtering with slicers (by month) for deeper analysis  
- 📊 KPI cards showing Total Revenue, Quantity Sold, and Orders

## 📁 Dataset
- File: `Coffee Shop Sales.xlsx`  
- Data includes: sales date, product details, product category, location, size, revenue, and quantity sold.

## 🛠 Tools & Technologies
- Power BI Desktop  
- Microsoft Excel  
- DAX Measures

## 💡 Insights Generated
- Coffee category generated the highest revenue ($29.27K, 40.51%)  
- Astoria location had the highest sales performance  
- Large size drinks were most popular with 36.06% of total revenue  
- Revenue peaked around mid-February  
- Balanced distribution of product sales with slight edge to premium products  

## 🚀 How to Use
1. Clone this repository  
2. Open the `.pbix` file in Power BI Desktop  
3. Refresh the data if necessary  
4. Use slicers to explore month-wise performance  

## 🧑‍💼 Author
**Avinash Pareta**  
Power BI Developer | Data Analyst  
📧 [Add your email or LinkedIn here]  
"""

# Save README file
readme_path = os.path.join(base_path, "README.md")
with open(readme_path, "w") as f:
    f.write(readme_content.strip())

# Create ZIP file
zip_path = os.path.join(base_path, "coffee-shop-sales-dashboard.zip")
with zipfile.ZipFile(zip_path, 'w') as zipf:
    for file_name in files_to_include:
        file_path = os.path.join(base_path, file_name)
        zipf.write(file_path, arcname=file_name)

zip_path
