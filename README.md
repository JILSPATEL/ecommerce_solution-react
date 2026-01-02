# E-commerce Solution - React & MySQL

A modern, full-stack e-commerce application built with React, Node.js, and MySQL.

## 📋 Prerequisites

-   **Node.js** (v16+)
-   **MySQL** (Running on Linux or locally)
-   **Terminal**: Bash / Terminal

## 🚀 Quick Setup (5 Minutes)

### 1. Database Setup (Linux)

Run these commands in your terminal to set up the database and seed it with data.

```bash
# Start MySQL Service
sudo systemctl start mysql

# Login to MySQL
mysql -u root -p
# Password: root
```

Inside the MySQL shell:

```sql
CREATE DATABASE IF NOT EXISTS ecommerce_solution;
USE ecommerce_solution;

-- Run Schema (Adjust path if needed)
SOURCE ./database/schema.sql;

-- Load Seed Data (Adjust path if needed)
SOURCE ./database/seed.sql;

EXIT;
```

### 2. Backend Setup
Open a **new terminal** (PowerShell/CMD) and run:

```bash
cd backend
npm install
npm run dev
```
> **Note**: The server runs on `http://localhost:5000`.

### 3. Frontend Setup
Open **another new terminal** and run:

```bash
cd react-ecommerce
npm install
npm run dev
```
> **Note**: The frontend runs on `http://localhost:5173`.

---

## 🔐 Credentials & Testing

### Database Access
-   **User**: `root`
-   **Password**: `root`
-   **Database**: `ecommerce_solution`

### Test Accounts (Pre-seeded)
Use these accounts to log in immediately.

| Role   | Email | Password |
| :--- | :--- | :--- |
| **User** | `jils@user.com` | `abc@123` |
| **Seller** | `jils@seller.com` | `abc@123` |

> **Login Tips**:
> - Go to **User Login** for customer features (Buying).
> - Go to **Seller Login** for seller features (Adding/Managing Products).
> - You can also **Sign Up** a new account; passwords will be automatically hashed.

---

## 🛠️ Project Structure

```
ecommerce_solution/
├── backend/            # Express.js API
├── react-ecommerce/    # React Frontend
├── database/           # SQL Schema & Seeds
└── README.md           # This file
```

## 🐛 Troubleshooting

### MySQL Connection Failed
-   **Error**: `Error connecting to MySQL database`
-   **Fix**: Ensure MySQL is running (`sudo systemctl start mysql`) and the password in `backend/.env` is correct.

### Database Not Found
-   **Error**: `Unknown database 'ecommerce_solution'`
-   **Fix**: Rerun the **Database Setup** steps above.

### Port Conflicts
-   **Error**: `EADDRINUSE :::5000`
-   **Fix**: Kill the process using port 5000 or change the `PORT` in `backend/.env`.

### Login Fails
-   **Fix**: If standard credentials don't work, try creating a **new account** via the Sign Up page. New accounts always work correctly.

---

## 🌟 Features
-   **User**: Browse products by category, Search, View details, User Authentication.
-   **Seller**: Manage products (Add/Edit/Delete), Seller Dashboard.
-   **Tech**: React 18, Vite, Node.js, Express, MySQL, JWT Authentication.
