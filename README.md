
## 🧠 Key Concept

This project demonstrates how to:
- Build a GUI using **Java Swing**
- Connect Java applications to a **MySQL** database using **JDBC**
- Perform **CRUD operations** (Insert specifically)
- Store and retrieve structured data representing **customer orders**
- Work with **CheckBoxes, Spinners**, and **Forms** in a real-world context

---

## 🎯 AIM

To design and implement a lightweight shopping cart system — "Gadget Zone" — that allows users to:
- Enter their name
- Select desired gadgets from a list
- Specify quantity for each
- Save this data into a MySQL database for record-keeping

---

## 🧩 Problem Statement

Traditional paper-based order systems are slow and error-prone, especially for small-scale gadget stores. There is a need for a user-friendly digital system where users can place orders easily, and data can be recorded, stored, and queried efficiently.

**Gadget Zone** solves this problem by:
- Providing a GUI for order placement
- Storing each selected item and its quantity under a customer’s name
- Structuring data for scalability and analysis

---

## 🛠️ Procedure

1. **Frontend**:
   - Built using Java Swing
   - User inputs name, selects gadgets, and sets quantities via spinner controls

2. **Backend**:
   - JDBC used for connecting to MySQL
   - On submission, the data is inserted into the database table

3. **Database**:
   - Each selected item is stored as an individual row with customer name, item, and quantity

4. **Validation**:
   - Ensures name is entered and at least one item is selected

---

## 🗃️ Database Structure

**Database Name**: `shoppingdb`  
**Table Name**: `orders`

```sql
CREATE DATABASE IF NOT EXISTS shoppingdb;
USE shoppingdb;

CREATE TABLE IF NOT EXISTS orders (
    id INT AUTO_INCREMENT PRIMARY KEY,
    customer_name VARCHAR(100) NOT NULL,
    item_name VARCHAR(100) NOT NULL,
    quantity INT NOT NULL
);
