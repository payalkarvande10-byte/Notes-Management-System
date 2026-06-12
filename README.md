# Notes Management System (NMS)

## Overview

The **Notes Management System (NMS)** is a role-based academic platform designed to simplify and organize the sharing of study materials within educational institutions.

Traditional note-sharing methods such as WhatsApp groups or physical distribution often lead to disorganization, file loss, and lack of access control. This system solves those problems by providing a centralized, department-wise structured platform for managing academic notes.

The platform supports three user roles:

* **Student**
* **Teacher**
* **Administrator**

Built using **React.js**, **Node.js**, **Express.js**, and **MySQL**, the system ensures secure authentication, structured content management, and scalable API architecture.

---

## Objective

The main objective of this project is to create a secure and structured academic notes sharing system where:

* Teachers can create classes and upload subject-wise notes.
* Students can request access to classes and download notes.
* Admin can monitor all system activities.

This eliminates unorganized note sharing and provides controlled academic resource management.

---

##  Features

### Student Module

* Student Registration & Login
* JWT Authentication
* Browse available classes by department & semester
* Send join requests to teachers
* View approved classes
* Access subjects and notes
* Download notes
* View profile details

---

### Teacher Module

* Teacher Registration & Login
* Create and manage classes
* Add and manage subjects
* Upload notes (PDF, DOC, DOCX)
* View uploaded notes
* Delete notes
* Approve/Reject student join requests
* View teacher profile

---

###  Admin Module

* Secure Admin Login
* View all teachers by department
* View all students by department
* View all classes
* View all subjects
* View all uploaded notes
* Read-only dashboard for institutional monitoring

---

##  Tech Stack

### Frontend

* React.js
* Axios
* React Router DOM
* Bootstrap / CSS

### Backend

* Node.js
* Express.js
* JWT Authentication
* Multer (File Upload)

### Database

* MySQL

---

##  Authentication System

The project uses **JWT (JSON Web Token)** for role-based authentication.

Roles:

* Student
* Teacher
* Admin

Each API route is protected using middleware to verify:

* Token validity
* User role authorization

---

##  Project Structure

```
NMS/
│── client/              # React Frontend
│── server/              # Node.js Backend
│── routes/
│── controllers/
│── middleware/
│── uploads/             # Uploaded Notes
│── config/
│── models/
│── database/
│── package.json
│── README.md
```

---

##  Installation

### 1. Clone the repository

```bash
git clone https://github.com/your-username/notes-management-system.git
```

---

### 2. Install dependencies

#### Frontend

```bash
cd client
npm install
```

#### Backend

```bash
cd server
npm install
```

---

### 3. Configure environment variables

Create a **.env** file inside the server folder:

```
PORT=5000
DB_HOST=localhost
DB_USER=root
DB_PASSWORD=yourpassword
DB_NAME=nms
JWT_SECRET=your_secret_key
```

---

### 4. Start backend

```bash
npm start
```

---

### 5. Start frontend

```bash
npm start
```

---

##  API Endpoints

### Authentication

* POST /api/auth/student/register
* POST /api/auth/teacher/register
* POST /api/auth/login

### Teacher

* POST /api/teacher/classes

* GET /api/teacher/classes

* DELETE /api/teacher/classes/:id

* POST /api/teacher/subjects

* DELETE /api/teacher/subjects/:id

* POST /api/teacher/notes/upload

* DELETE /api/teacher/notes/:id

* PUT /api/teacher/requests/:id

### Student

* GET /api/student/classes
* POST /api/student/join-request
* GET /api/student/subjects/:classId
* GET /api/student/notes/:subjectId

### Admin

* GET /api/admin/teachers
* GET /api/admin/students
* GET /api/admin/classes
* GET /api/admin/subjects
* GET /api/admin/notes

---

##  Software Development Model

This project follows the **Agile Software Development Model**.

### Sprint Breakdown:

* Sprint 1 → Authentication & Registration
* Sprint 2 → Class & Subject Management
* Sprint 3 → Notes Upload System
* Sprint 4 → Join Request Workflow
* Sprint 5 → Admin Dashboard & Testing

---

##  Benefits of Agile in NMS

* Incremental development
* Faster testing
* Easy bug detection
* Flexible requirement changes
* Parallel role-based development

---

##  Future Enhancements

* Search functionality for notes
* Notifications for join approvals
* Note preview before download
* Version history for notes
* AI-based note recommendations

---

##  Author

**Payal Karvande**

---

##  License

This project is developed for educational purposes.
