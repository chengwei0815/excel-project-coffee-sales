# Coffee Sales Dashboard Creation in Excel

This project outlines the creation of a **dynamic and interactive Coffee Sales Dashboard** in Excel. Follow the steps below to gather, transform, and visualize data effectively.

---

## 📊 Final Dashboard Overview

The dashboard includes:
1. **Line Chart**: Total sales over time split by coffee type:
   - Arabica, Excelsa, Liberica, and Robusta.
2. **Bar Chart - Sales by Country**:
   - Sales data segmented for the U.S., Ireland, and the UK.
3. **Bar Chart - Top 5 Customers**:
   - Displays top-performing customers.
4. **Interactive Filters**:
   - **Timeline Slicer**: Adjusts data visualizations by specific time periods.
   - **Roast Type Slicer**: Filters visuals by dark, light, or medium roast.
   - **Size Slicer**: Filters based on coffee package sizes (0.2 kg, 0.5 kg, 1 kg, and 2.5 kg).
   - **Loyalty Card Slicer**: Filters customers with or without a loyalty card.

---

## 📁 Data Overview

The source data is divided across three tabs:

### 1. **Orders Tab**
- Fields: `Order ID`, `Order Date`, `Customer ID`, `Product ID`, and `Quantity`.
- Additional fields (`F–M`) are populated using lookup formulas from other tabs.

### 2. **Customers Tab**
- **Primary Key**: `Customer ID`.
- Fields: `Customer Name`, `Email`, `Phone`, `Address`, `Country`, `Postcode`, and `Loyalty Card Status`.

### 3. **Products Tab**
- **Primary Key**: `Product ID`.
- Fields: `Coffee Type`, `Roast Type`, `Size`, `Unit Price`, `Price per 100 Grams`, and `Profit Margin`.

---

## 🛠️ Steps to Build the Dashboard

### 1. **Data Gathering**
- Populate missing data in the **Orders Tab** using lookup formulas:
  - **XLOOKUP**: Fetch customer-related information (Name, Email, Country) from the **Customers Tab**.
  -    =IF(XLOOKUP(C2,customers!$A$1:$A$1001,customers!$C$1:$C$1001,,0)=0,"",XLOOKUP(C2,customers!$A$1:$A$1001,customers!$C$1:$C$1001,,0))
  
  - **INDEX-MATCH**: Dynamically retrieve product-related data (Coffee Type, Roast Type, Size, Unit Price, etc.) from the **Products Tab**.
  -    =INDEX(products!$A$1:$G$49,MATCH(orders!$D2,products!$A$1:$A$49,0),MATCH(orders!I$1,products!$A$1:$G$1,0))

### 2. **Data Transformation**
- Clean and consolidate the data for analysis.
- Ensure all missing values are filled, and columns are mapped correctly.

### 3. **Dashboard Construction**
- Create **Pivot Tables** for:
  1. Total sales by coffee type over time.
  2. Sales by country.
  3. Top 5 customers based on sales.
- Add slicers for interactivity:
  - **Timeline Slicer**: Filters by date.
  - **Categorical Slicers**: Filters by roast type, size, and loyalty card status.
- Build **Pivot Charts**:
  - Line chart for sales trends.
  - Bar charts for country-wise sales and top 5 customers.

---

## ✨ Key Highlights

- **Dynamic Features**:
  - Filters and slicers provide a user-friendly and interactive experience.
- **Efficient Lookups**:
  - **XLOOKUP** for simplicity and clarity.
  - **INDEX-MATCH** for dynamic and flexible data retrieval.
- **Visual Appeal**:
  - Clear and intuitive visuals for effective data-driven decision-making.

---

## 🏁 Outcome

By the end of this project, you will have a fully functional **Coffee Sales Dashboard** capable of real-time filtering and data analysis.

---

## 📎 Resources

All necessary files and data can be found in the project repository. If you create your own version, feel free to share it in the comments or submit a pull request. We'd love to see your creativity!

---

**Happy Analyzing!**

Gathered the customer data using XLOOKUP

Used INDEX MATCH to gather the product data

<img width="1205" alt="Screenshot 2025-01-14 at 1 56 19 AM" src="https://github.com/user-attachments/assets/78eb7a29-d5a7-45cd-8915-6397829b17da" />


