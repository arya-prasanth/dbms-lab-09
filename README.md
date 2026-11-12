# 🏨 Hotel Room Booking System

A database-driven web application developed using **PHP and MySQL** as part of the DBMS Lab project.

## 📌 Project Information

| Detail | Description |
|---|---|
| **Project Title** | Hotel Room Booking System |
| **Name** | Arya PL |
| **Roll Number** | 09 |
| **Database Name** | `hotel_db` |
| **Backend** | PHP |
| **Database** | MySQL |
| **Server Environment** | XAMPP |

## 📖 Project Overview

The Hotel Room Booking System is designed to manage hotel guests, room information and room reservations efficiently.

The application provides a booking interface where users can select guests, choose available rooms and enter check-in and check-out dates. Booking details are stored in a MySQL database, while a separate report page retrieves and displays booking information using SQL JOIN operations.

## ✨ Features

- Guest information management.
- Room details and room type management.
- Room availability checking based on booking dates.
- Room booking through a PHP form.
- Validation of booking details.
- Automatic booking ID generation.
- Booking confirmation message after successful insertion.
- Booking report with guest and room information.
- Relational database using primary and foreign keys.

## 🗄️ Database Structure

**Database:** `hotel_db`

The database consists of three tables:

| Table | Description |
|---|---|
| `guest` | Stores guest ID, name, city and phone number. |
| `room` | Stores room number, room type, tariff per day and floor. |
| `booking` | Stores booking ID, guest ID, room number, check-in and check-out dates. |

### Database Relationships

- `guest_id` is the primary key of the `guest` table.
- `room_no` is the primary key of the `room` table.
- `booking_id` is the primary key of the `booking` table.
- `booking.guest_id` references `guest.guest_id`.
- `booking.room_no` references `room.room_no`.

These relationships maintain referential integrity between the tables.

## 🛠️ Technologies Used

- **PHP** – Server-side programming and database operations.
- **MySQL** – Relational database management.
- **HTML5** – Structure of the web pages.
- **CSS3** – Styling and layout.
- **XAMPP** – Local Apache and MySQL server.
- **phpMyAdmin** – Database administration.

## 📂 Project Structure

```text
dbms-lab-09/
│
├── db.php
├── booking.php
├── report.php
├── header.php
├── footer.php
├── style.css
├── hotel_db.sql
├── README.md
│
└── screenshots/
    ├── booking_form
    ├── check_avail.png
    ├── booked_success.png
    └── booking_report.png
```

## ⚙️ Installation and Execution

1. Install and open **XAMPP**.
2. Start the Apache and MySQL services.
3. Open phpMyAdmin at `http://localhost/phpmyadmin`.
4. Create or import the database using the provided `hotel_db.sql` file.
5. Place the project folder inside the XAMPP `htdocs` directory.
6. Configure the database connection details in `db.php` if required.
7. Open the application in your browser:

```text
http://localhost/dbms-lab-09/booking.php
```

8. Use the booking form to create a reservation.
9. Open the report page to view the saved booking records:

```text
http://localhost/dbms-lab-09/report.php
```

## 🔗 PHP–MySQL Database Connectivity

The application connects PHP to the MySQL database using the MySQLi extension.  
A separate file named `db.php` establishes and manages the database connection.  
The `booking.php` page collects booking details through an HTML form and processes them using PHP.  
A prepared SQL `INSERT` statement stores the guest ID, room number, check-in date and check-out date in the `booking` table.  
The `report.php` page executes a `SELECT` query with `INNER JOIN` operations to retrieve related records from all three tables.  
The retrieved information is displayed in an HTML table as the booking report.

## 📦 Deliverables

- PHP source code.
- MySQL database export (`hotel_db.sql`).
- Application screenshots.
- Project documentation (`README.md`).

---


