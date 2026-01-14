# Infrastructure Tracker - Web GIS Project

<img width="1919" height="917" alt="image" src="https://github.com/user-attachments/assets/53722dcf-d87a-4115-b827-1cfab92ed6a9" />


## 📋 Project Overview
A full-stack Web GIS application to track infrastructure failures. Citizens can report issues, municipality staff can manage them, and administrators can monitor the system.

##  Features

### Completed Features

**User Management**
- Sign up and login
- 3 different roles: Citizen, Municipality, Administrator
- JWT token-based authentication

**Issue Management**
- CRUD operations (Create, Read, Update, Delete)
- Geolocation support
- Filtering and searching
- Status tracking (Open, In Progress, Resolved)

**Map Features**
- Leaflet.js integration
- Location selection (click or coordinate input)
- Markers and popups
- Real-time updates

**UI/UX**
- Responsive design
- Bootstrap icons
- Toast notifications
- User-friendly interface


   
| Role          | Email                                                 | Password | Permissions                    |
| ------------- | ----------------------------------------------------- | -------- | ------------------------------ |
| Citizen       | [citizen@test.com](mailto:citizen@test.com)           | 123456   | View and add issues            |
| Municipality  | [municipality@test.com](mailto:municipality@test.com) | 123456   | Update and manage issues       |
| Administrator | [admin@test.com](mailto:admin@test.com)               | 123456   | Full user and issue management |

| Method | Endpoint           | Description           |
| ------ | ------------------ | --------------------- |
| POST   | /api/auth/register | Register a new user   |
| POST   | /api/auth/login    | User login            |
| GET    | /api/auth/me       | Get current user info |


| Method | Endpoint        | Description                   |
| ------ | --------------- | ----------------------------- |
| GET    | /api/issues     | Get all issues (with filters) |
| GET    | /api/issues/:id | Get single issue details      |
| POST   | /api/issues     | Add a new issue               |
| PUT    | /api/issues/:id | Update an issue               |
| DELETE | /api/issues/:id | Delete an issue               |

Query Parameters
GET /api/issues?type=road&status=open&search=collapse

📁 Project Structure
infrastructure-tracker/
├── backend/
│   ├── server.js          # Main server file
│   ├── package.json       # Dependencies
│   └── .env               # Environment variables
└── frontend/
    ├── index.html         # Main HTML file
    ├── app.js             # Main JavaScript file
    └── style.css          # Inline CSS
## 🔧 Technical Details

### Backend
- **Framework:** Express.js
- **Authentication:** JWT
- **Database:** In-memory (for testing)
- **CORS:** Enabled
- **Port:** 5000

### Frontend
- **Map Library:** Leaflet.js
- **Icons:** Bootstrap Icons
- **CSS:** Custom responsive design
- **JavaScript:** Vanilla ES6+


## 🚀 Setup

### 1. Backend Setup
```bash
# Navigate to the backend directory
cd backend

# Install dependencies
npm install

# Start the server
npm start
# The server will run on port 5000
```

###2. Frontend Setup
```bash
# Navigate to the frontend directory
cd frontend

# Open index.html in your browser
# You can use Live Server or similar tools for hot reload
