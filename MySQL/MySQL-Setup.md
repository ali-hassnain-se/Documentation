# 🐬 MySQL Environment Setup Guide

**Prepared for:** BS Software Engineering Students  
**Institution:** Superior College, Mian Channu  
**Tools:** MySQL Server 8.0, MySQL Workbench, MySQL Shell

---

## 1. 📥 Downloading the Software
To begin, we used the official **MySQL Community Installer**. This is the industry-standard way to manage MySQL products on Windows.

* **Official Link:** [Download MySQL Installer](https://dev.mysql.com/downloads/installer/)
* **Selection:** We chose the **"mysql-installer-community"** version (~556 MB) because it contains all necessary files offline, making the installation smoother on your Lenovo T480.

---

## 2. 🛠️ Installation Steps
During the installation, we selected the **"Full"** setup type to ensure a complete development environment.

* **Setup Type:** "Full" (Includes Server and Workbench).
* **Requirements:** We fixed missing dependencies (like Microsoft Visual C++) by clicking **Execute** within the installer.
* **Execution:** Clicked **Execute** to install all components (Server, Workbench, Shell, etc.).

---

## 3. 🔐 Configuration & Security
This is the most critical part where we connected the software to the system:

* **Port:** Default **3306**.
* **Authentication:** Strong Password Encryption.
* **Root Password:** Set up a Master Password.
    > **⚠️ Note:** Always remember this password! You cannot run SQL queries in the Workbench without entering this.

---

## 4. ⚡ Running Your First SQL Query
Once installed, we use **MySQL Workbench** to interact with the database.

### How to use MySQL Workbench:
1.  **Open Connection:** Click on "Local Instance MySQL80".
2.  **Login:** Enter your Root Password.
3.  **The Lightning Bolt (⚡):** Click this icon to run your code.

### Practice Code Snippet:
```sql
-- Create a new database
CREATE DATABASE UniversityDB;

-- Select the database
USE UniversityDB;

-- Create a table for student records
CREATE TABLE Students (
    ID INT PRIMARY KEY,
    Name VARCHAR(100),
    Semester INT
);

-- View the table
SELECT * FROM Students;
