# 🏪 Supermarket Management Database Project

This project is a **fully functional database** for managing supermarket operations,  
created using **Microsoft Access** and **Excel**.

## 📋 Included Tables
- Customer  
- Category  
- Product  
- Supplier  
- Order  
- Order_Details  
- Payment  
- Inventory_Log  

Each table contains realistic data based on well-known Egyptian products and suppliers to simulate real supermarket operations.

## 🧠 Purpose
The goal of this project is to design and implement a practical **Relational Database System**  
that covers all daily operations: sales, stock tracking, suppliers, and payments.  
It also demonstrates understanding of key concepts like:
- Relationships between tables  
- Normalization  
- Data integrity  

## ⚙️ Tools Used
- Microsoft Access  
- Microsoft Excel  
- Draw.io (for ER Diagram)

## 📈 Features
- Organized and normalized database structure  
- Clear relationships between all entities  
- Ready-to-import Excel tables  
- Realistic and practical data  

---
Customer
- Customer_ID (PK, AutoNumber)
- Full_Name
- Phone
- Email
- Address
- Join_Date
- Points

Category
- Category_ID (PK, AutoNumber)
- Category_Name
- Description

Supplier
- Supplier_ID (PK, AutoNumber)
- Name
- Phone
- Email
- Address
- Company_Name
- Contract_Start_Date

Employee
- Employee_ID (PK, AutoNumber)
- Full_Name
- Phone
- Position
- Salary
- Hire_Date

Product
- Product_ID (PK, AutoNumber)
- Product_Name
- Category_ID (FK -> Category.Category_ID)
- Supplier_ID (FK -> Supplier.Supplier_ID)
- Price
- Quantity_in_stock
- Expiry_Date
- Barcode

Order
- Order_ID (PK, AutoNumber)
- Customer_ID (FK -> Customer.Customer_ID)
- Employee_ID (FK -> Employee.Employee_ID)   <-- الموظف اللي سجّل الفاتورة
- Order_Date
- Total_Amount
- Status

Order_Details
- OrderDetail_ID (PK, AutoNumber)
- Order_ID (FK -> Order.Order_ID)
- Product_ID (FK -> Product.Product_ID)
- Quantity
- Unit_Price
- Discount
- Subtotal

Payment
- Payment_ID (PK, AutoNumber)
- Order_ID (FK -> Order.Order_ID)
- Payment_Method
- Payment_Date
- Amount_Paid

Inventory_Log
- Log_ID (PK, AutoNumber)
- Product_ID (FK -> Product.Product_ID)
- Action_Type (Add/Subtract)
- Quantity_Changed
- Date
- Supplier_ID (FK -> Supplier.Supplier_ID)  [اختياري]
