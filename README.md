
# 🧪 API Testing – Simple Grocery Store API

## 📌 Project Overview

This project focuses on **API testing** for the **Simple Grocery Store API** using **Postman**.
The goal is to validate API functionality, response status codes, performance, and data integrity across multiple modules such as **Products, Cart, Authentication, and Orders**.

Automated tests are written using **JavaScript (Postman Tests)** and variables are dynamically managed using **collection variables**.

---

## 🛠 Tools & Technologies

* **Postman**
* **RESTful APIs**
* **JavaScript (Postman test scripts)**
* **JSON**
* **Bearer Token Authentication**

---

## 📂 API Modules Covered

### 1️⃣ Status

* Check API availability
* Validate HTTP status code `200`

**Endpoint**

```
GET /status
```

---

### 2️⃣ Products

* Get all products
* Get product by ID
* Validate response time (< 3 seconds)

**Endpoints**

```
GET /products
GET /products/{productId}
```

---

### 3️⃣ Cart & Items

* Create cart
* Add item to cart
* Modify item quantity (PATCH)
* Replace item (PUT)
* Delete item
* Retrieve cart details
* Retrieve cart items

**Endpoints**

```
POST   /carts
POST   /carts/{cartId}/items
PATCH  /carts/{cartId}/items/{itemId}
PUT    /carts/{cartId}/items/{itemId}
DELETE /carts/{cartId}/items/{itemId}
GET    /carts/{cartId}
GET    /carts/{cartId}/items
```

✔ Cart ID and Item ID are stored dynamically using collection variables.

---

### 4️⃣ Authentication

* Create API client
* Generate access token
* Store token for authorized requests

**Endpoint**

```
POST /api-clients
```

✔ Token is stored as a collection variable and used in secured endpoints.

---

### 5️⃣ Orders

* Create order
* Update order
* Delete order
* Get all orders
* Get specific order

**Endpoints**

```
POST   /orders
PATCH  /orders/{orderId}
DELETE /orders/{orderId}
GET    /orders
GET    /orders/{orderId}
```

✔ All order requests require **Bearer Token Authentication**.

---

## ✅ Test Scenarios Implemented

* Status code validation (200, 201, 204)
* Response time validation (< 3 seconds)
* Data extraction and variable chaining
* Authentication token handling
* CRUD operations validation
* End-to-end workflow testing (Cart → Order)

---

## 🔄 Variables Used

| Variable    | Description  |
| ----------- | ------------ |
| `grocery`   | Base URL     |
| `cart_id`   | Cart ID      |
| `productId` | Product ID   |
| `itemId`    | Cart Item ID |
| `token`     | Bearer Token |
| `orderId`   | Order ID     |

---

## ▶ How to Run the Tests

1. Import the Postman collection
2. Set the `grocery` base URL in environment or collection variables
3. Run requests manually **or**
4. Use **Postman Collection Runner** to execute all tests

---

## 📈 Expected Outcome

* All APIs respond with correct status codes
* Response times are within acceptable limits
* Secure endpoints work only with valid tokens
* Cart and order flows function correctly end-to-end

---

## 👤 Author

**Ahmed Alashmawy**
API Testing & Quality Assurance

