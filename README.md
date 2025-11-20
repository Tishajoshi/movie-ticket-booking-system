# Movie Ticket Booking System

A simple and user-friendly web application for booking movie tickets online. This project is built using **PHP**, **MySQL**, **HTML**, and **CSS**. Users can browse movie schedules, book seats, make payments, and generate receipts.

---

## 📌 Features

- 📅 **View Movie Schedule** (schedule.php)  
- 🎟️ **Book Seats** (booking.php)  
- 💳 **Payment Gateway Flow**  
  - pgRedirect.php  
  - pgResponse.php  
  - TxnStatus.php  
- 🧾 **Generate Booking Receipt** (reciept.php)  
- 📞 **Contact Form** (contact-us.php)  
- ✔️ **Verification Page** (verify.php)  
- ❌ **Failure/Error Screen** (fail.html)  
- 🔗 **MySQL Database Connection** (connection.php)

---

## 🏗️ Project Structure

movie-ticket-booking-system/
│
├── booking.php
├── schedule.php
├── reciept.php
├── connection.php
├── contact-us.php
├── TxnStatus.php
├── pgRedirect.php
├── pgResponse.php
├── fail.html
├── verify.php
├── Verify.png
└── Movie Ticket Booking System Project Report.docx

yaml
Copy code

---

## ⚙️ Installation

### 1️⃣ Clone the Repository
```bash
git clone https://github.com/Tishajoshi/movie-ticket-booking-system.git
cd movie-ticket-booking-system
2️⃣ Set Up the Database
Create a MySQL database, for example:
movie_booking

Create tables for:

Users

Shows

Bookings

Transactions

(Your table structure may be found in connection.php or the project report.)

Update credentials inside connection.php:

php
Copy code
$servername = "localhost";
$username = "root";
$password = "";
$dbname = "movie_booking";
3️⃣ Run on Localhost
Use XAMPP / WAMP / MAMP:

Copy the project folder to:

rust
Copy code
htdocs/  (for XAMPP)
Start Apache & MySQL

Open the application:

perl
Copy code
http://localhost/movie-ticket-booking-system/index.php
🧠 How It Works (Flow)
User visits schedule page

Selects movie + show time

Proceeds to seat booking

Redirects to payment gateway (real or test)

Payment response received

Receipt generated

On failure → redirected to fail.html

🗄️ Database Schema (Suggested)
users
Column	Type
user_id (PK)	INT
name	VARCHAR
email	VARCHAR
phone	VARCHAR

shows
Column	Type
show_id (PK)	INT
movie_name	VARCHAR
show_time	TIME
date	DATE
venue	VARCHAR
available_seats	INT

bookings
Column	Type
booking_id (PK)	INT
user_id (FK)	INT
show_id (FK)	INT
seat_number	VARCHAR
booking_time	TIMESTAMP

transactions
Column	Type
txn_id (PK)	VARCHAR
booking_id (FK)	INT
amount	FLOAT
status	VARCHAR
response_code	VARCHAR
response_msg	VARCHAR

📄 Project Report
A detailed documentation Movie Ticket Booking System Project Report.docx is included, containing:

System analysis

Data flow diagrams

Screenshots

Testing

Future scope

🤝 Contributing
Pull requests are welcome!
If you want to add improvements, open an issue first to discuss suggested changes.

📜 License
This project is created for learning and academic purposes.
Feel free to modify or extend it.

⭐ Acknowledgment
Thanks for checking out this project!
If you like it, consider giving the repo a star ⭐ on GitHub.
