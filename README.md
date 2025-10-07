# 🚖 Uber Sales Data Analysis Project

## 📊 Project Overview
This project analyzes **Uber NCR Ride Bookings Data** to uncover insights related to sales trends, booking patterns, payment methods, and customer-driver behavior.  
Using **Python (Pandas, NumPy, Matplotlib, Seaborn)**, I performed **data cleaning, transformation, and visualization** to identify key performance indicators and relationships within the dataset.

---

## 🧰 Tools & Libraries Used
- 🐍 **Python**
- 📚 **Pandas** – Data manipulation and cleaning  
- 🔢 **NumPy** – Numerical computations  
- 📊 **Matplotlib & Seaborn** – Data visualization  
- ⚠️ **Warnings** – To suppress irrelevant warning messages  

---

## 🗂️ Dataset Information
**File Used:** `ncr_ride_bookings.csv`  
**Total Rows:** 150,000  
**Total Columns:** 21  

### 📑 Columns Overview:
| Column Name | Description |
|--------------|-------------|
| Date | Booking Date |
| Time | Booking Time |
| Booking ID | Unique Booking Identifier |
| Booking Status | Completed / Cancelled / Incomplete etc. |
| Customer ID | Unique Customer Identifier |
| Vehicle Type | Auto, Bike, Sedan, UberXL, etc. |
| Pickup Location | Starting Point |
| Drop Location | Destination Point |
| Avg VTAT | Average Vehicle Turnaround Time |
| Avg CTAT | Average Customer Turnaround Time |
| Booking Value | Total Value of Ride |
| Ride Distance | Total Distance of Ride |
| Driver Ratings | Ratings given by the customer |
| Customer Rating | Ratings given by the driver |
| Payment Method | Cash / UPI / Wallet / Card etc. |

---

## 🧹 Data Cleaning & Transformation Steps
✅ Changed `Date` column datatype from **object → datetime**  
✅ Checked and replaced all **null values with 0**  
✅ Created a new column **Monthly Sales Trends** from the `Date` column  
✅ Converted months into an **ordered categorical variable** for proper visualization  
✅ Created a correlation feature between **Ride Distance** and **Booking Value**

---

## 📈 Exploratory Data Analysis (EDA)

### 🔹 Monthly Sales Trends
- Maximum bookings occurred in **July (12,897)**, **January (12,861)**, and **May (12,778)**  
- Lowest bookings were recorded in **February (11,927)**, **April (12,199)**, and **September (12,248)**  

📉 **Visualization:** Line Chart showing Monthly Sales Trends  
```python
sns.lineplot(x=monthly_sales.index, y=monthly_sales.values, marker="o", color="g")
