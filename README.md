```markdown
# UMP Psychology Consultation Application ("MindMate")

**Project Type:** Final Year Project (Undergraduate)  
**University:** University of Mpumalanga (UMP)

---

## 1. Authors (Group 4)

| Name                  | Student ID   |
|-----------------------|--------------|
| Sanele Mabuza         | 222387688    |
| Karabo Makofane       | 222541652    |
| Lufuno Ramuhashi      | 222518863    |
| Siyanda Khanyile      | 220834725    |
| Rito Hlungwani        | 222362723    |
| Sydwel Nhlambo        | 222428554    |

---

## 2. Project Overview

The **UMP Psychology Consultation Application**, codenamed **"MindMate"**, is a web-based platform developed as a final year project. Its primary goal is to bridge the gap between students at the University of Mpumalanga and the university's psychological consultation and wellness services.

This application provides a **secure, confidential, and accessible** environment for students to:
- Seek help
- Manage their well-being
- Book appointments with university counselors

It also enables **staff** to efficiently manage these services. The platform aims to **destigmatize seeking psychological help** and streamline the process for **students, psychologists, and administrators**.

---

## 3. Project Status

This project was submitted in partial fulfillment of the requirements for the Final Year Project module at the University of Mpumalanga.

- **Status:** Completed  
- **Final Mark:** 79%  
- **Version:** 1.0.0

---

## 4. Key Features

The application is divided into **three main user roles**: Student, Psychologist, and Admin.

### Student Features
- **Secure Registration & Login** – Confidential account creation and login.
- **Psychologist Profiles** – View public list with specializations and profile pictures.
- **Appointment Booking** – Select psychologist, method (e.g., *virtual via Zoom*), and available time.
- **Email Notifications** – Automatic confirmation upon booking.
- **Contact Form** – Secure messaging to admin (logged-in only).

### Psychologist Features
- **Secure Login** – Dedicated dashboard access.
- **Appointment Calendar** – View upcoming/past appointments (`fetch_appointments.php`).
- **Email Notifications** – Instant alerts on new bookings.

### Admin Features
- **Admin Dashboard** – Real-time system stats:
  - Total Appointments
  - Sessions This Month
  - Total Students
  - Total Psychologists
- **Session & User Management** – View all users and monitor sessions.
- **Password Security** – Change own password.
- **System Maintenance** – Auto-update past appointments to *Completed*.

### Guest Features (Public)
- **View Psychologists** – Public directory.
- **Guest Contact Form** – Inquiry submission without login.

---

## 5. Technology Stack

Built with a **LAMP-stack** foundation, focusing on server-side rendering and dynamic content.

| Layer               | Technology                              |
|---------------------|-----------------------------------------|
| **Frontend**        | HTML5, CSS3, JavaScript                 |
| **Backend**         | PHP (procedural style)                  |
| **Database**        | MySQL (via phpMyAdmin)                  |
| **Server**          | XAMPP / Apache                          |
| **APIs & Services** | PHPMailer (Gmail SMTP), Calendar API, Chatbot API |

---

## 6. Installation & Setup

To run this project locally, a **PHP/MySQL server environment** is required.

### Prerequisites
- **XAMPP** (or WAMP/MAMP/LAMP)
- **phpMyAdmin** (included with XAMPP) or MySQL Workbench
- **Web Browser** (Chrome, Firefox)
- **Code Editor** (e.g., VS Code)
- **Git** (optional)

### Local Setup

1. **Clone the repository:**
   ```bash
   git clone [Your Repository URL]
   ```
   *Or download and extract the ZIP.*

2. **Move to `htdocs`:**
   ```
   C:/xampp/htdocs/[your-project-folder]
   ```

3. **Database Setup:**
   - Start **Apache** and **MySQL** in XAMPP.
   - Open [http://localhost/phpmyadmin](http://localhost/phpmyadmin)
   - Create database: `ump_psych_db`
   - Import your `.sql` file (e.g., `ump_psych_db.sql`)

4. **Configure `connect.php`:**
   ```php
   $servername = "localhost";
   $username = "root";     // Default XAMPP
   $password = "";         // Default XAMPP
   $dbname = "ump_psych_db";
   ```

5. **Configure Email (PHPMailer):**
   Update SMTP credentials in:
   - `bookappointment.php`
   - `contactform.php`
   - `contactform(guests).php`

   ```php
   $mail->Username = 'smabuza782@gmail.com'; // Your Gmail
   $mail->Password = 'vria ifeb itgz mrsm';   // Gmail App Password
   ```

6. **Launch Application:**
   ```
   http://localhost/[your-project-folder]/
   ```

---

## 7. Usage

1. **Register** as a student → Log in.
2. Browse psychologists → **Book an appointment**.
3. Check **email** for confirmation (student & psychologist).
4. **Admin Login:**  
   - URL: `/admin/login.html`  
   - Default: `admin@ump.ac.za` / `admin123`
5. **Psychologist Login:**  
   - URL: `/psychologist/login.html`  
   - Default: `psychologist@ump.ac.za` / `psych123`

> **Note:** Include default admin/psychologist accounts in your SQL dump.

---

## 8. License

This project is licensed under the **MIT License**.  
See the [`LICENSE.md`](LICENSE.md) file for details.

---
```

> **Tip:** Replace placeholder values like `[Your Repository URL]`, `[your-project-folder]`, and the SQL file name with actual ones before final submission.
```
