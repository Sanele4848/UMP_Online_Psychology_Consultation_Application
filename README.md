# MindMate
### UMP Psychology Consultation Application
**Final Year Project (Undergraduate) | Group 4**

![Project Status](https://img.shields.io/badge/Status-Completed-success?style=flat-square)
![Score](https://img.shields.io/badge/Final_Mark-79%25-blue?style=flat-square)

> **Bridging the gap between University of Mpumalanga students and wellness services.**

---

## Table of Contents
- [1. Project Overview](#1-project-overview)
- [2. Authors](#2-authors-group-4)
- [3. Key Features](#3-key-features)
- [4. Technology Stack](#4-technology-stack)
- [5. Installation & Setup](#5-installation--setup)
- [6. Usage](#6-usage)

---

## 1. Project Overview

**MindMate** is a web-based platform developed as a final year project at the **University of Mpumalanga (UMP)**. Its primary goal is to provide accessible, secure, and confidential psychological consultation and wellness services to students.

The platform aims to destigmatize seeking psychological help and streamline the administrative process for:
* **Students:** Seek help, manage well-being, and book appointments securely.
* **Psychologists:** Manage schedules and view upcoming sessions.
* **Administrators:** Efficiently oversee system usage and services.

---

## 2. Project Team & Roles (Group 4)

| Student ID | Name | Primary Role(s) |
| :--- | :--- | :--- |
| **222387688** | Sanele Mabuza | Project Lead / Full Stack Developer |
| **222541652** | Karabo Makofane | Frontend Developer / UI Designer |
| **222518863** | Siyanda Khanyile | Backend Developer / Database Admin |
| **220834725** | Lufuno Ramuhashi | Quality Assurance / Documentation |
| **222362723** | Rito Hlungwani | Frontend Developer |
| **222428554** | Sydwell Nhlambo | System Analyst / Tester |

---

## 3. Key Features

The application is divided into three main secured user roles, in addition to public guest access.

### Student Features
* **Secure Registration & Login:** Confidential account creation.
* **Psychologist Profiles:** Browse specialist profiles and pictures.
* **Appointment Booking:** Select methods (e.g., *Virtual via Zoom*) based on real-time availability.
* **Automated Notifications:** Email confirmations upon successful booking.
* **Private Contact Form:** Secure messaging channel to administrators.

### Psychologist Features
* **Dedicated Dashboard:** Secure login area for staff.
* **Appointment Management:** View upcoming and past appointments via `fetch_appointments.php`.
* **Instant Alerts:** Email notifications for new bookings.

### Admin Features
* **Real-time Dashboard Stats:**
    * Total Appointments
    * Sessions This Month
    * Total User Counts (Students/Psychologists)
* **System Management:** Monitor all sessions and manage user accounts.
* **Maintenance Tools:** Auto-update past appointments to *Completed* status.

### Guest Features (Public)
* **Directory:** View available psychologists without an account.
* **Inquiries:** Submit questions via the public contact form.

---

## 4. Technology Stack

MindMate is built on a **LAMP-stack** foundation, focusing on robust server-side rendering.

| Layer | Technologies Used |
| :--- | :--- |
| **Frontend** | HTML5, CSS3, JavaScript |
| **Backend** | PHP (Procedural Style) |
| **Database** | MySQL (via phpMyAdmin) |
| **Server** | Apache (XAMPP) |
| **APIs/Services** | PHPMailer (SMTP), Calendar API, Chatbot API |

---

## 5. Installation & Setup

### Prerequisites
* **Server Environment:** [XAMPP](https://www.apachefriends.org/) (recommended for local testing)
* **Browser:** Chrome or Firefox
* **Editor:** VS Code (recommended)

### Local Deployment Steps

1.  **Clone the Repository**
    ```bash
    git clone [https://github.com/yourusername/mindmate.git](https://github.com/yourusername/mindmate.git)
    ```
    *Alternatively, download the ZIP and extract it to your `htdocs` folder.*

2.  **Project Location**
    Ensure the project folder is located at:
    `C:/xampp/htdocs/mindmate`

3.  **Database Configuration**
    * Start **Apache** and **MySQL** via the XAMPP Control Panel.
    * Navigate to `http://localhost/phpmyadmin`.
    * Create a new database named `ump_psych_db`.
    * Import the provided SQL dump file: `ump_psych_db.sql`.

4.  **Connection Setup**
    Verify credentials in `connect.php` match your local environment:
    ```php
    $servername = "localhost";
    $username = "root";      // Default XAMPP username
    $password = "";          // Default XAMPP password
    $dbname = "ump_psych_db";
    ```

5.  **Configure SMTP (PHPMailer)**
    To enable email notifications, update Gmail credentials in `bookappointment.php` and `contactform.php`:
    ```php
    $mail->Username = 'your-email@gmail.com';
    $mail->Password = 'your-app-specific-password';
    ```

6.  **Launch Application**
    Access via browser: `http://localhost/mindmate/`

---

## 6. Usage

1.  **Students:** Register an account and log in to book sessions.
2.  **Email Confirmation:** Both parties receive immediate confirmation upon booking.
3.  **Administrative Access:**

| Role | Login URL | Default Credentials (Dev) |
| :--- | :--- | :--- |
| **Admin** | `/admin/login.html` | `admin@ump.ac.za` / `admin123` |
| **Psychologist** | `/psychologist/login.html` | `psychologist@ump.ac.za` / `psych123` |

> **Note:** Ensure these default accounts exist in your imported `.sql` database before attempting login.

---
