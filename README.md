# Project Camp Backend

Project Camp Backend is a **RESTful API service** designed for collaborative project management. It supports secure authentication, role-based permissions, project organization, task workflows, subtasks, notes, and file uploads — providing a complete backend foundation for team productivity applications.

---

## 🚀 Features

### 🔐 Authentication & Authorization
- User registration & login (JWT authentication)
- Email verification + password reset workflow
- Refresh token mechanism
- Secure logout
- Role-based access: **Admin**, **Project Admin**, **Member**

### 📁 Project Management
- Create, update, delete, and list projects
- Project-level role control and member management
- View project details and team members

### 📝 Tasks & Subtasks
- Task creation with assignees and descriptions
- Status tracking: `todo`, `in_progress`, `done`
- Subtask creation, updates, and completion
- Role-controlled task and subtask operations
- File attachments with secure upload handling

### 🗒 Project Notes
- Admin-only note management
- All project members can view notes

### 🩺 System Health
- `/api/v1/healthcheck/` endpoint for monitoring service status

---

## 📌 Roles & Permissions

| Feature                        | Admin | Project Admin | Member |
|-------------------------------|:-----:|:-------------:|:------:|
| Manage Projects               | ✓ | ✗ | ✗ |
| Manage Members                | ✓ | ✗ | ✗ |
| Create/Update/Delete Tasks    | ✓ | ✓ | ✗ |
| View Tasks                    | ✓ | ✓ | ✓ |
| Manage Subtasks               | ✓ | ✓ | ✗ |
| Update Subtask Status         | ✓ | ✓ | ✓ |
| Manage Notes                  | ✓ | ✗ | ✗ |
| View Notes                    | ✓ | ✓ | ✓ |

---

## 📂 API Structure

 - /api/v1/auth → Authentication
 - /api/v1/projects → Projects & members
 - /api/v1/tasks → Tasks & subtasks
 - /api/v1/notes → Project notes
 - /api/v1/healthcheck → Status check

---

## 🛡️ Security

- JWT-based authentication (access + refresh tokens)
- Email verification system
- Strict role-based middleware
- Input validation on requests
- CORS configuration
- Secure file uploads via Multer

---

## 📸 File Management

- Multiple attachments for tasks
- Stored in `public/images`
- Metadata logged: URL, MIME type, size

---

## ✔️ Success Criteria

- Complete authentication and authorization system  
- Full project, task, subtask workflow  
- Robust access control  
- File attachment support  
- Email-driven verification and recovery  
- Clean and well-documented API  

---