
# 📊 Blinkit Grocery Product Analysis – SQL Project  

## 📌 Project Overview  
This project analyzes grocery product data from **Blinkit** using **SQL queries**.  
The dataset (`Grocery_Store`) includes details about items such as weight, fat content, type, MRP, outlet size, sales, and visibility.  
The goal is to perform **data exploration, aggregation, and insights generation** using SQL.  

---

## Dataset  
The database used: **`fingertips`**  
Main table: **`Grocery_Store`**  

Key columns include:  
- `Item_Identifier`  
- `Item_Weight`  
- `Item_Fat_Content`  
- `Item_Type`  
- `Item_MRP`  
- `Item_Outlet_Sales`  
- `Item_Visibility`  
- `Outlet_Size`  
- `Outlet_Type`  
- `Outlet_Location_Type`  
- `Outlet_Establishment_Year`  

---

## SQL Tasks & Queries  

The project covers **51 SQL queries**, including:  

✔️ Descriptive statistics (`MAX`, `MIN`, `AVG`, `COUNT`)  
✔️ Filtering & conditions (`WHERE`, `BETWEEN`, `IN`)  
✔️ Sorting (`ASC`, `DESC`)  
✔️ Unique values (`DISTINCT`)  
✔️ Grouping & Aggregation (`GROUP BY`, `SUM`, `AVG`)  
✔️ Business insights on sales, pricing, fat content, and outlets  

---

## Sample Query Outputs  

### 🔹 Q7 – Count of Items with Low Fat  
```sql
SELECT COUNT(Item_Fat_Content) 
FROM Grocery_Store 
WHERE Item_Fat_Content = 'Low Fat';
```
**Sample Output:**  

| Count |  
|-------|  
| 3167  |  

---

### 🔹 Q11 – Items with MRP > 200  
```sql
SELECT Item_Identifier, Item_Fat_Content, Item_Type, Item_MRP 
FROM Grocery_Store 
WHERE Item_MRP > 200;
```
**Sample Output:**  

| Item_Identifier | Item_Fat_Content | Item_Type   | Item_MRP |  
|-----------------|------------------|-------------|----------|  
| FDA15           | Low Fat          | Dairy       | 249.80   |  
| DRC01           | Regular          | Soft Drinks | 212.23   |  
| FDN15           | Low Fat          | Meat        | 250.00   |  

---

### 🔹 Q24 – Count of Items by Item_Type  
```sql
SELECT Item_Type, COUNT(Item_Identifier) AS No_Of_Item  
FROM Grocery_Store  
GROUP BY Item_Type  
ORDER BY No_Of_Item DESC;
```
**Sample Output:**  

| Item_Type        | No_Of_Item |  
|------------------|------------|  
| Fruits & Veggies | 1232       |  
| Snack Foods      | 1200       |  
| Household        | 910        |  
| Dairy            | 682        |  

---

### 🔹 Q46 – Total Sales by Item_Type  
```sql
SELECT Item_Type, SUM(Item_Outlet_Sales) AS Total_Sales
FROM Grocery_Store 
GROUP BY Item_Type 
ORDER BY Total_Sales DESC;
```
**Sample Output:**  

| Item_Type        | Total_Sales |  
|------------------|-------------|  
| Fruits & Veggies | 1,258,965   |  
| Snack Foods      | 1,190,320   |  
| Household        | 902,100     |  
| Dairy            | 695,470     |  

---

## 📈 Key Insights
- **Fruits & Vegetables** and **Snack Foods** dominate sales volume.  
- **Low Fat** products have significant demand, highlighting health-conscious buying.  
- High-priced items (`MRP > 200`) contribute notably to revenue.  
- Outlet sales vary heavily by **location type** and **establishment year**.  

---

## 🚀 How to Use
1. Import the dataset into your SQL environment.  
2. Run the queries from `SQL Project Blinkit – Grocery Product Analysis.sql`.  
3. Explore results & derive insights for business strategy.  

---

## 🛠️ Tech Stack
- **SQL** (MySQL / PostgreSQL / SQL Server)  
- **Data Analysis & Visualization** (optional Excel/BI tools)  

---

## 📌 Author
👤 *Shailendra*  
