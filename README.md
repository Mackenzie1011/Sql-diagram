# Sql-diagram
![alt text](Sql.png)

# CREATING TABLES
```    sql
CREATE TABLE customers (
    customer_id NUMBER PRIMARY KEY,
    customer_name VARCHAR2(100),
    address VARCHAR2(200),
    city VARCHAR2(100),
    state VARCHAR2(100),
    zip VARCHAR2(20)
);
```
```sql
CREATE TABLE orders (
    order_id NUMBER PRIMARY KEY,
    customer_id NUMBER REFERENCES customers(customer_id),
    order_date DATE,
    order_status VARCHAR2(50)
);
```
```sql
CREATE TABLE products (
    product_id NUMBER PRIMARY KEY,
    product_name VARCHAR2(100),
    price NUMBER,
    quantity NUMBER
);
```
