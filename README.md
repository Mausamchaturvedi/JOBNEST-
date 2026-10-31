# JOBNEST – Online Job Portal

A web-based **Online Job Portal** developed using **C++ (Winsock), HTML, CSS, and JavaScript**. JOBNEST provides a platform where job seekers can explore job opportunities, register, log in, apply for jobs, save jobs, and receive application notifications. Administrators can manage applications and update their statuses through a dedicated admin dashboard.

---

## 📌 Project Overview

JOBNEST is designed to simplify the job search and recruitment process by connecting job seekers with employment opportunities through a single platform.

The project uses a C++ backend built with Windows Sockets (Winsock) to handle HTTP requests and API operations. The frontend provides a user-friendly interface, while text files are used for storing application data.

## ✨ Features

### 👤 Job Seeker
- User Registration and Login
- Browse Available Jobs
- View Job Details
- Apply for Job Opportunities
- Save Jobs for Later
- View Applied Jobs
- Receive Application Notifications

### 🔐 Admin Panel
- Secure Admin Login
- Admin Dashboard
- View Job Applications
- Manage Application Status
- Update Applications to different statuses
- Send Notifications to Applicants
- Admin Logout

### 🌐 General Features
- Responsive and user-friendly interface
- Dark-themed user interface
- Frontend and backend integration
- REST-style HTTP API endpoints
- File-based data storage

## 🛠️ Technologies Used

| Technology | Purpose |
|---|---|
| C++ | Backend development |
| Winsock2 | HTTP server and network communication |
| HTML5 | Website structure |
| CSS3 | Styling and responsive design |
| JavaScript | Frontend functionality and API integration |
| Text Files | Data storage |
| Visual Studio Code | Development environment |
| MSYS2 UCRT64 / G++ | C++ compilation |

## 📂 Project Structure

```text
JOBNEST - C++/
│
├── Backend/
│   ├── backend.cpp
│   ├── backend.exe
│   ├── admin.txt
│   ├── users.txt
│   ├── jobs.txt
│   ├── applications.txt
│   ├── notifications.txt
│   └── other data files
│
├── Frontend/
│   ├── index.html
│   ├── admin-login.html
│   ├── admin.html
│   │
│   ├── css/
│   │   └── style.css
│   │
│   └── js/
│       ├── auth.js
│       ├── admin-login.js
│       ├── admin.js
│       └── other JavaScript files
│
└── README.md
```

*Note: Adjust the folder and file names above if your actual project structure differs.*

## ⚙️ Requirements

Before running the project, install:

1. **Visual Studio Code**
2. **MSYS2** with the UCRT64 GCC compiler
3. **G++ compiler**
4. **Live Server extension** in VS Code
5. A Windows operating system with Winsock support

## 🚀 Installation and Setup

### Step 1: Clone the Repository

Open your terminal and execute:

```bash
git clone https://github.com/YOUR-USERNAME/JOBNEST.git
```

Navigate into the project folder:

```bash
cd JOBNEST
```

### Step 2: Compile the C++ Backend

Open the `Backend` folder in your terminal:

```powershell
cd Backend
```

Add the MSYS2 compiler path:

```powershell
$env:Path = "C:\msys64\ucrt64\bin;" + $env:Path
```

Compile the backend:

```powershell
g++ backend.cpp -o backend.exe -std=c++17 -lws2_32
```

### Step 3: Run the Backend Server

Execute:

```powershell
.\backend.exe
```

The backend server will start at:

```text
http://127.0.0.1:8080
```

Keep this terminal open while using the application.

### Step 4: Run the Frontend

1. Open the project in Visual Studio Code.
2. Navigate to the `Frontend` folder.
3. Right-click `index.html`.
4. Select **Open with Live Server**.

The frontend will generally open at:

```text
http://127.0.0.1:5500/Frontend/index.html
```

### Step 5: Open the Admin Panel

Visit:

```text
http://127.0.0.1:5500/Frontend/admin-login.html
```

Use the administrator credentials configured in the backend's `admin.txt` file.

**Important:** Keep the backend server and Live Server running in separate terminals.

## 🔗 Backend API Endpoints

The C++ backend handles requests through the following API endpoints:

| Method | Endpoint | Description |
|---|---|---|
| GET | `/api/health` | Check backend server status |
| GET | `/api/jobs` | Retrieve available jobs |
| GET | `/api/admin/applications` | Retrieve applications (admin authentication required) |
| POST | `/api/register` | Register a new user |
| POST | `/api/login` | Authenticate a user |
| POST | `/api/apply` | Apply for a job |
| POST | `/api/applications` | Handle application data |
| POST | `/api/saved-jobs` | Save job information |
| POST | `/api/notifications` | Handle notifications |
| POST | `/api/admin/login` | Authenticate administrator |
| GET | `/api/admin/verify` | Verify admin session |
| POST | `/api/admin/logout` | End admin session |
| POST | `/api/update-application-status` | Update application status (admin authentication required) |

## 💾 Data Storage

JOBNEST uses text files to store application information.

| File | Purpose |
|---|---|
| `admin.txt` | Administrator login credentials |
| `users.txt` | Registered user information |
| `jobs.txt` | Job information |
| `applications.txt` | Job application records |
| `notifications.txt` | Applicant notifications |

The backend reads and updates these files when API requests are received.

## 🔒 Security Note

This project is developed for learning and academic demonstration purposes.

- Admin API operations use token-based session authentication.
- Administrator passwords are currently stored in a local text file.
- The current implementation is not intended for production deployment.
- Production systems should use password hashing, HTTPS, secure database storage, token expiration, and additional security controls.

**Never upload real passwords, private credentials, or personal user data to GitHub.** Add sensitive data files such as `admin.txt`, `users.txt`, and other files containing personal information to `.gitignore`. Provide a separate example file with placeholder values if required.

## 🧪 Testing

The following operations can be tested:

1. Open the JOBNEST home page.
2. Register a new job seeker account.
3. Log in using the registered account.
4. Browse available job opportunities.
5. Apply for a job.
6. Save a job for later.
7. Log in to the admin panel.
8. View submitted applications.
9. Update an application's status.
10. Check applicant notifications.
11. Log out from the admin panel.

## 🔮 Future Enhancements

- Integration with MySQL or another database.
- Resume upload and management.
- Advanced job search and filtering.
- Email notifications.
- Company and employer registration.
- User profile management.
- Job recommendation system.
- Improved authentication and security.
- Deployment on a cloud hosting platform.

## 🎯 Project Objective

The main objective of JOBNEST is to develop a simple and effective online recruitment platform that reduces manual effort in job searching and application management. It demonstrates the integration of a C++ network-based backend with a modern web frontend.

## 👨‍💻 Developer

**Project Name:** JOBNEST – Online Job Portal  
**Project Type:** Web-Based Application  
**Backend Language:** C++  
**Frontend:** HTML, CSS, JavaScript  
**Development Environment:** Visual Studio Code  

---

⭐ If you find this project useful, consider giving the repository a star!

**Made with dedication using C++ and Web Technologies.**
