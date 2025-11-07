UMP Psychology Consultation Application ("MindMate")

Project Type: Final Year Project (Undergraduate)
University: University of Mpumalanga (UMP)

1. Authors (Group 4)

Sanele Mabuza (222387688)

Karabo Makofane (222541652)

Lufuno Ramuhashi (222518863)

Siyanda Khanyile (220834725)

Rito Hlungwani (222362723)

Sydwel Nhlambo (222428554)

2. Project Overview

The UMP Psychology Consultation Application, "MindMate," is a web-based platform developed as a final year project. Its primary goal is to bridge the gap between students at the University of Mpumalanga and the university's psychological consultation and wellness services.

This application provides a secure, confidential, and accessible environment for students to seek help, manage their well-being, book appointments with university counselors, and for staff to manage these services. It aims to destigmatize seeking psychological help and make the process more efficient for students, psychologists, and administrators.

3. Project Status

This project was submitted in partial fulfillment of the requirements for the Final Year Project module at the University of Mpumalanga.

Status: Completed
Final Mark: 79%
Version: 1.0.0

4. Key Features

The application is divided into three main user roles: Student, Psychologist, and Admin.

Student Features

Secure Registration & Login: Students can create a confidential account and log in.

Psychologist Profiles: View a public list of available psychologists, their specializations, and profile pictures.

Appointment Booking: An intuitive system to select a psychologist, consultation method (e.g., 'virtual' via Zoom), and an available date/time.

Email Notifications: Receive automatic email confirmation upon successfully booking an appointment.

Contact Form: A secure contact form for logged-in students to send messages to the admin team.

Psychologist Features

Secure Login: Psychologists log in to their dedicated dashboard.

Appointment Calendar: View all upcoming and past appointments in a calendar format (fetched via fetch_appointments.php).

Email Notifications: Receive an automatic email notification when a student books a new appointment.

Admin Features

Admin Dashboard: A central hub to view key system statistics:

Total Appointments

Sessions This Month

Total Students

Total Psychologists

Session & User Management:

View lists of all students and psychologists in the system.

Monitor recent (past) sessions and upcoming appointments.

Password Security: Ability for the admin to change their own password.

System Maintenance: Automatically updates the status of past appointments to 'Completed'.

Guest Features (Public)

View Psychologists: View the public-facing list of university psychologists.

Guest Contact Form: A contact form for non-logged-in users to send inquiries to the admin team.

5. Technology Stack

This project is built with a LAMP-stack foundation, focusing on server-side rendering and dynamic content generation.

Frontend: HTML5, CSS3, JavaScript

Backend: PHP (procedural style)

Database: MySQL (via phpMyAdmin)

Server Environment: XAMPP / Apache

APIs & Services:

PHPMailer (for Gmail SMTP)

Calendar API (for scheduling)

Chatbot API

6. Installation & Setup

To run this project locally, you will need a PHP/MySQL server environment.

Prerequisites

XAMPP (or WAMP/MAMP/LAMP): This provides Apache, MySQL, and PHP in one package.

Database Tool: phpMyAdmin (comes with XAMPP) or a similar tool like MySQL Workbench.

Web Browser: e.g., Chrome, Firefox.

Code Editor: e.g., VS Code.

Git (optional, for cloning).

Local Setup

Clone the repository:

git clone [Your Repository URL]


Or, download the ZIP file and extract it.

Move Project to htdocs:

Place the entire project folder inside your XAMPP installation's htdocs directory (e.g., C:/xampp/htdocs/[your-project-folder]).

Database Setup:

Start Apache and MySQL services from the XAMPP Control Panel.

Open phpMyAdmin (e.g., http://localhost/phpmyadmin).

Create a new database (e.g., ump_psych_db).

Import the [your_database_file.sql] file to set up the tables. (You should include this SQL file in your project).

Configure connect.php:

Open the includes/connect.php file.

Update the database credentials ($servername, $username, $password, $dbname) to match your local MySQL setup.

$servername = "localhost";
$username = "root"; // Default for XAMPP
$password = "";     // Default for XAMPP
$dbname = "ump_psych_db"; // The database you created


Configure Email Credentials (Important!):

For email notifications to work, you must update the SMTP credentials in the following files:

bookappointment.php

contactform.php

contactform(guests).php

Find these lines and replace them with your own Gmail "App Password".

$mail->Username = 'smabuza782@gmail.com'; // Your email
$mail->Password = 'vria ifeb itgz mrsm';   // Your Gmail App Password


Access the Application:

Open your browser and navigate to http://localhost/[your-project-folder]/.

7. Usage

After starting the application:

Navigate to the Register page to create a new student account.

Log in with your new student credentials.

Explore the psychologist list and book a test appointment.

Check your email (and the psychologist's email) for the confirmation.

Log in as an Admin to see the statistics update on the dashboard.

Admin URL: [e.g., /admin/login.html]

Default Admin: [e.g., admin@ump.ac.za / admin123]

Log in as a Psychologist to view the new appointment on your calendar.

Psychologist URL: [e.g., /psychologist/login.html]

Default Psychologist: [e.g., psychologist@ump.ac.za / psych123]

(Note: You should create default admin/psychologist accounts in your SQL file for testing purposes).

8. License

[e.g., This project is licensed under the MIT License. See the LICENSE.md file for details.]
