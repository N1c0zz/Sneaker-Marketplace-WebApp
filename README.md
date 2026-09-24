# 👟 NS_KICKS: Sneaker E-Commerce & Marketplace

## 📋 Project Overview
**NS_KICKS** is a complete e-commerce web application dedicated to the sale of sneakers. Rather than a simple storefront, the platform operates as a **Marketplace** with a multi-role system, allowing distinct functionalities for Buyers (Clienti) and Sellers (Venditori). 

The system handles the entire e-commerce lifecycle: from user authentication and product catalog browsing, to cart management, order placement, and internal notifications.

---

## ✨ Key Features

### 👤 Multi-Role User Management
* **Customers (Clienti):** Can browse products, filter by categories/models, manage their shopping cart, place orders, and receive notifications about their order status.
* **Sellers (Venditori):** Have access to a dedicated dashboard to add new sneaker models, manage inventory (sizes, quantities, prices), and track sales.

### 🛒 Core E-Commerce Logic
* **Dynamic Catalog:** Products are linked to specific Models and Categories, allowing users to filter sneakers effectively.
* **Order Management:** Tracks the state of an order (e.g., Pending, Shipped) keeping the inventory updated.
* **Notification System:** An internal messaging system alerts users regarding order updates and platform events.

---

## 🏗️ Tech Stack & Architecture
*(Note: The system follows a standard web architecture with server-side rendering).*

* **Frontend:** HTML5, CSS3, Vanilla JavaScript
* **Backend:** Native PHP
* **Database:** Relational Database (MySQL / MariaDB)

---

## 🗄️ Database Engineering
A significant focus of this project was the robust design of the underlying relational database to handle marketplace complexities.

* **Generalization Mapping:** The inheritance between the generic `Utente` (User) and its sub-entities (`Cliente` and `Venditore`) was efficiently mapped into a single relational table using a `Tipo` (Type) discriminator column.
* **Many-to-Many Handling:** Complex interactions, such as the relationship between Orders and Products (`Presenze`) or Users and Notifications (`Ricezioni`), are normalized using associative tables.

<details>
<summary><b>Click to expand Database Schemas (ER & Relational)</b></summary>

*(Update the paths below with the actual locations of your images)*

**Entity-Relationship (ER) Diagram**
![ER Diagram](./mockup/db_conceptual_scheme.pdf)

**Logical Relational Schema**
![Logical Schema](./mockup/db_tables.pdf)

</details>

---

## 🚀 Getting Started

To run NS_KICKS locally on your machine, the easiest way is to use a local web server environment like **XAMPP**, **MAMP**, or **WAMP**.

### Prerequisites
* XAMPP (which includes Apache and MySQL)
* PHP (v7.4 or higher)

### Installation
1. **Clone the repository** inside your web server's root directory (e.g., `htdocs` for XAMPP):
   ```bash
   cd xampp/htdocs
   git clone https://github.com/N1c0zz/NS-Kicks-Sneaker-Ecommerce.git
   ```

2. **Database Setup:** 
   * Start Apache and MySQL from the XAMPP Control Panel.
   * Open your browser and go to `http://localhost/phpmyadmin`.
   * Create a new database named `ns_kicks_db` (or check the exact database name inside the SQL dump file).
   * Import the SQL dump file located in the repository.

3. **Configure Connection:** 
   * Open the PHP configuration file responsible for the database connection (e.g., `db.php` or `config.php`).
   * Ensure the credentials match your local MySQL setup (usually username: `root` and an empty password).

4. **Launch:** 
   * Open your browser and navigate to `http://localhost/NS-Kicks-Sneaker-Ecommerce`.

---
*Developed by Nicolò Morini & Simone Mosconi*
