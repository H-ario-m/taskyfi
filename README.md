# Taskyfi - Modern Project Management Solution

[Insert Hero Image Here]

Taskyfi is a modern, real-time project management application that combines the power of Kanban boards with automated workflows and team collaboration features. Built with a focus on real-time updates and seamless team coordination, it offers a comprehensive solution for managing projects of any size.

##  Features

### Authentication & Authorization
- Secure user authentication system
- Role-based access control
- Session management
- Password encryption and security measures

###  Project Management
- Create and manage multiple projects
- Invite team members to projects
- Real-time project updates
- Project activity timeline
- Custom project roles and permissions

### Kanban Board
- Drag-and-drop task management
- Customizable task columns
- Real-time task updates
- Task filtering and search
- Task priority levels
- Due date tracking

### Automation Engine
- Custom workflow automation
- Trigger-based actions
- Email notifications
- Task auto-assignment
- Due date reminders
- Priority-based workflows

### Real-Time Communication
- In-app notifications
- Real-time task comments
- Team chat functionality
- @mentions and user tagging
- Email notifications for important updates

### Notification System
- In-app notifications
- Email notifications
- Custom notification preferences
- Real-time alerts
- Notification history

## Getting Started

### Prerequisites
- Node.js (v14 or higher)
- MongoDB (v4.4 or higher)
- npm or yarn package manager

### Environment Setup

1. Clone the repository:
\`\`\`bash
git clone https://github.com/H-ario-m/taskyfi.git
cd taskyfi
\`\`\`

2. Create environment files:

Backend (.env):
\`\`\`env
MONGODB_URI=your_mongodb_uri
JWT_SECRET=your_jwt_secret
PORT=5000
SMTP_HOST=your_smtp_host
SMTP_PORT=587
SMTP_USER=your_smtp_user
SMTP_PASS=your_smtp_password
SMTP_FROM_ADDRESS=noreply@yourdomain.com
\`\`\`

Frontend (.env):
\`\`\`env
VITE_API_URL=http://localhost:5000/api
VITE_WS_URL=ws://localhost:5000
\`\`\`

### Installation

1. Install Backend Dependencies:
\`\`\`bash
cd backend
npm install
\`\`\`

2. Install Frontend Dependencies:
\`\`\`bash
cd frontend
npm install
\`\`\`

### Running the Application

1. Start the Backend Server:
\`\`\`bash
cd backend
npm run dev
\`\`\`

2. Start the Frontend Development Server:
\`\`\`bash
cd frontend
npm run dev
\`\`\`

The application will be available at:
- Frontend: http://localhost:5173
- Backend API: http://localhost:5000
- WebSocket: ws://localhost:5000

## Screenshots
![Screenshot From 2025-05-17 05-55-00](https://github.com/user-attachments/assets/6c67d7cf-a4ae-48ba-914e-d3a37390e2d2)

![Screenshot From 2025-05-17 05-55-17 (Copy)](https://github.com/user-attachments/assets/487b4441-413d-4ba9-8cdd-123c6cd28291)\

![Screenshot From 2025-05-17 05-55-33](https://github.com/user-attachments/assets/98bf791c-2926-4b67-a4b8-0c5587d9d949)


### Dashboard
[Insert Dashboard Screenshot]

### Project Board
[Insert Project Board Screenshot]

### Task Details
[Insert Task Details Screenshot]

### Automation Workflow
[Insert Automation Workflow Screenshot]

## 🛠 Technology Stack

### Backend
- Node.js
- Express.js
- MongoDB with Mongoose
- WebSocket (ws)
- JSON Web Tokens
- Nodemailer

### Frontend
- React
- Vite
- TailwindCSS
- React Query
- React DnD
- WebSocket Client

## 🔄 Workflow Automation Examples

### 1. Task Status Change Notification
\`\`\`javascript
{
    "name": "Task Completion Alert",
    "trigger": {
        "type": "task_status_changed",
        "parameters": {
            "targetStatus": "completed"
        }
    },
    "actions": [{
        "type": "send_notification",
        "parameters": {
            "title": "Task Completed",
            "message": "Task '${task.title}' has been completed"
        }
    }]
}
\`\`\`

### 2. Due Date Reminder
\`\`\`javascript
{
    "name": "Due Date Reminder",
    "trigger": {
        "type": "due_date_approaching",
        "parameters": {
            "daysThreshold": 2
        }
    },
    "actions": [{
        "type": "send_email",
        "parameters": {
            "subject": "Task Due Soon",
            "body": "Task '${task.title}' is due in 2 days"
        }
    }]
}
\`\`\`

## 📝 API Documentation

### Authentication Endpoints
- POST /api/auth/register
- POST /api/auth/login
- POST /api/auth/logout
- GET /api/auth/me

### Project Endpoints
- GET /api/projects
- POST /api/projects
- GET /api/projects/:id
- PUT /api/projects/:id
- DELETE /api/projects/:id

### Task Endpoints
- GET /api/tasks
- POST /api/tasks
- GET /api/tasks/:id
- PUT /api/tasks/:id
- DELETE /api/tasks/:id
- PATCH /api/tasks/:id/assign - Assign task to a project member
- POST /api/tasks/:id/badge - Add badge to task

### Workflow Endpoints
- GET /api/workflows/project/:projectId
- POST /api/workflows/project/:projectId
- PUT /api/workflows/:workflowId
- DELETE /api/workflows/:workflowId
- PATCH /api/workflows/:workflowId/toggle

## API Examples

### Assign Task to User
\`\`\`http
PATCH /api/tasks/:taskId/assign
Content-Type: application/json
Authorization: Bearer YOUR_JWT_TOKEN

{
    "assigneeId": "user_id"
}
\`\`\`

Response:
\`\`\`json
{
    "_id": "task_id",
    "title": "Task Title",
    "description": "Task Description",
    "status": "In Progress",
    "assignee": {
        "_id": "user_id",
        "name": "John Doe",
        "email": "john@example.com"
    },
    "creator": {
        "_id": "creator_id",
        "name": "Jane Smith",
        "email": "jane@example.com"
    },
    "project": "project_id",
    "createdAt": "2024-01-01T00:00:00.000Z",
    "updatedAt": "2024-01-01T00:00:00.000Z"
}
\`\`\`

## 🤝 Contributing

1. Fork the repository
2. Create your feature branch (\`git checkout -b feature/AmazingFeature\`)
3. Commit your changes (\`git commit -m 'Add some AmazingFeature'\`)
4. Push to the branch (\`git push origin feature/AmazingFeature\`)
5. Open a Pull Request

## 🙏 Acknowledgments

- [React Documentation](https://reactjs.org/)
- [Express.js Documentation](https://expressjs.com/)
- [MongoDB Documentation](https://docs.mongodb.com/)
- [TailwindCSS Documentation](https://tailwindcss.com/)

## 📞 Contact

Your Name - Anshuman Ojha (<anshumanojha91@gmail.com>)
