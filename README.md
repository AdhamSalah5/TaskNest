# TaskNest

A full-stack task management web application built with Node.js, React, and MongoDB.

## Features

### User Features
- User authentication (Register/Login) using JWT
- Create, read, update, and delete tasks
- Mark tasks as complete/incomplete
- Filter and sort tasks by priority, due date, or completion status
- View assigned tasks

### Admin Features
- View all users and their task statistics
- Assign tasks to users
- Activate/deactivate user accounts
- Delete user accounts
- View all tasks in the system

## Tech Stack

### Backend
- Node.js
- Express.js
- MongoDB with Mongoose
- JWT for authentication
- bcrypt for password hashing

### Frontend (Coming Soon)
- React
- Redux for state management
- Axios for API calls
- Material-UI for styling

## Getting Started

### Prerequisites
- Node.js (v14 or higher)
- MongoDB (v4.4 or higher)
- npm or yarn

### Installation

1. Clone the repository
```bash
git clone https://github.com/yourusername/tasknest.git
cd tasknest
```

2. Install backend dependencies
```bash
cd server
npm install
```

3. Create a .env file in the server directory with the following variables:
```
PORT=5000
MONGO_URI=mongodb://localhost:27017/tasknest
JWT_SECRET=your-super-secret-jwt-key
NODE_ENV=development
```

4. Start the backend server
```bash
npm run dev
```

The server will start on http://localhost:5000

## API Endpoints

### Authentication
- POST /api/auth/register - Register a new user
- POST /api/auth/login - Login user
- GET /api/auth/me - Get current user

### Tasks
- GET /api/tasks - Get all tasks for current user
- POST /api/tasks - Create a new task
- PUT /api/tasks/:id - Update a task
- DELETE /api/tasks/:id - Delete a task
- PATCH /api/tasks/:id/toggle-complete - Toggle task completion status

### Admin
- GET /api/admin/users - Get all users
- GET /api/admin/users/stats - Get user statistics
- PATCH /api/admin/users/:id/status - Update user status
- DELETE /api/admin/users/:id - Delete a user
- GET /api/admin/tasks - Get all tasks

## License

This project is licensed under the MIT License - see the LICENSE file for details. 