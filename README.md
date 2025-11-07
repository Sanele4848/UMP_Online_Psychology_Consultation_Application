# MindMate 🧠
### UMP Psychology Consultation Application
**Final Year Project (Undergraduate) | Group 4**

![Project Status](https://img.shields.io/badge/Status-Completed-success?style=flat-square)
![Score](https://img.shields.io/badge/Final_Mark-79%25-blue?style=flat-square)
![Version](https://img.shields.io/badge/Version-1.0.0-orange?style=flat-square)
![License](https://img.shields.io/badge/License-MIT-green?style=flat-square)

> **Bridging the gap between University of Mpumalanga students and wellness services.**

---

## 📖 Table of Contents
- [Overview](#-overview)
- [Authors](#-authors-group-4)
- [Key Features](#-key-features)
- [Technology Stack](#-technology-stack)
- [Installation & Setup](#-installation--setup)
- [Usage](#-usage)
- [License](#-license)

---

## 🔭 Overview

**MindMate** is a web-based platform developed as a final year project at the **University of Mpumalanga (UMP)**. Its primary goal is to accessible, secure, and confidential psychological consultation and wellness services to students.

The platform aims to **destigmatize seeking psychological help** and streamline the administrative process for:
* 🎓 **Students:** Seek help, manage well-being, and book appointments securely.
* 🧠 **Psychologists:** Manage schedules and view upcoming sessions.
* 🛡️ **Administrators:** efficiently oversee system usage and services.

---

## 👥 Authors (Group 4)

| Student ID | Name |
| :--- | :--- |
| **222387688** | Sanele Mabuza |
| **222541652** | Karabo Makofane |
| **222518863** | Lufuno Ramuhashi |
| **220834725** | Siyanda Khanyile |
| **222362723** | Rito Hlungwani |
| **222428554** | Sydwel Nhlambo |

---

## ✨ Key Features

The application is divided into three main secured user roles, plus public guest access.

### 🎓 Student Features
* **Secure Registration & Login:** Confidential account creation.
* **Psychologist Profiles:** Browse specialist profiles and pictures.
* **Appointment Booking:** Select methods (e.g., *Virtual via Zoom*) and real-time availability.
* **Automated Notifications:** Email confirmations upon successful booking.
* **Private Contact Form:** Secure messaging channel to administrators.

### 🧠 Psychologist Features
* **Dedicated Dashboard:** Secure login area.
* **Appointment Management:** View upcoming and past appointments via `fetch_appointments.php`.
* **Instant Alerts:** Email notifications for new bookings.

### 🛡️ Admin Features
* **Real-time Dashboard Stats:**
    * Total Appointments
    * Sessions This Month
    * Total User Counts (Students/Psychologists)
* **System Management:** Monitor all sessions and manage user accounts.
* **Maintenance Tools:** Auto-update past appointments to *Completed* status.

### 🌐 Guest Features (Public)
* **Directory:** View available psychologists without an account.
* **Inquiries:** Submit questions via the public contact form.

---

## 💻 Technology Stack

MindMate is built on a **LAMP-stack** foundation, focusing on robust server-side rendering.

| Layer | Technologies Used |
| :--- | :--- |
| **Frontend** | ![HTML5](https://img.shields.io/badge/-HTML5-E34F26?logo=html5&logoColor=white) ![CSS3](https://img.shields.io/badge/-CSS3-1572B6?logo=css3&logoColor=white) ![JavaScript](https://img.shields.io/badge/-JavaScript-F7DF1E?logo=javascript&logoColor=black) |
| **Backend** | ![PHP](https://img.shields.io/badge/-PHP-777BB4?logo=php&logoColor=white) (Procedural Style) |
| **Database** | ![MySQL](https://img.shields.io/badge/-MySQL-4479A1?logo=mysql&logoColor=white) (via phpMyAdmin) |
| **Server** | Apache (XAMPP) |
| **APIs** | PHPMailer (SMTP), Calendar API, Chatbot API |

---

## ⚙️ Installation & Setup

### Prerequisites
* [XAMPP](https://www.apachefriends.org/) (recommended)
* Web Browser (Chrome/Firefox)
* Code Editor (VS Code recommended)

### Local Deployment Steps

1.  **Clone the Repository**
    ```bash
    git clone [https://github.com/yourusername/mindmate.git](https://github.com/yourusername/mindmate.git)
    # Or download the ZIP and extract it to your htdocs folder
    ```

2.  **Project Location**
    Ensure the project folder is located at:
    `C:/xampp/htdocs/mindmate`

3.  **Database Configuration**
    * Start **Apache** and **MySQL** in XAMPP Control Panel.
    * Navigate to `http://localhost/phpmyadmin`.
    * Create a new database named `ump_psych_db`.
    * Import the provided SQL dump file: `ump_psych_db.sql`.

4.  **Connect Database**
    Verify credentials in `connect.php`:
    ```php
    $servername = "localhost";
    $username = "root";      // Default XAMPP username
    $password = "";          // Default XAMPP password
    $dbname = "ump_psych_db";
    ```

5.  **Configure SMTP (PHPMailer)**
    Update Gmail credentials in `bookappointment.php` and `contactform.php`:
    ```php
    $mail->Username = 'your-email@gmail.com';
    $mail->Password = 'your-app-specific-password';
    ```

6.  **Launch**
    Visit: `http://localhost/mindmate/`

---

## 🚀 Usage

1.  **Students:** Register an account and log in to book sessions.
2.  **Check Email:** Both parties receive immediate confirmation upon booking.
3.  **Administrative Access:**

| Role | Login URL | Default Creds (Dev) |
| :--- | :--- | :--- |
| **Admin** | `/admin/login.html` | `admin@ump.ac.za` / `admin123` |
| **Psychologist** | `/psychologist/login.html` | `psychologist@ump.ac.za` / `psych123` |

> ⚠️ **Note:** Ensure these default accounts exist in your imported `.sql` database.

---

## 📄 License

This project is open-source and available under the **MIT License**. See the [LICENSE](LICENSE.md) file for details.
