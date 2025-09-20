# project-name

Description
Overview

## Tech Stack
- React
- Node.js

## Requirements
- Users must authenticate via JWT to access protected routes (Hint: Use jsonwebtoken.verify in auth middleware)
- Support creating, reading, updating and deleting tasks via Express routes (Hint: Use express.Router() to organize endpoints)
- Frontend should store JWT and include it in API requests (Hint: Use React Context or localStorage to manage the token)
- Tasks should include a project field and be filterable by project (Hint: Add project property to task object and UI components)
- Display tasks sorted by priority level (Hint: Use Array.sort either in backend or frontend)

## Installation

### Backend (Node.js + Express)
1. Clone the repo
   bash
   git clone https://github.com/your-username/project-name.git
   cd project-name/server
   
2. Install dependencies
   bash
   npm install
   
3. Create a `.env` file for environment variables:
   env
   JWT_SECRET=your_jwt_secret_key
   PORT=4000
   

### Frontend (React)
1. Navigate to the client folder
   bash
   cd ../client
   
2. Install dependencies
   bash
   npm install
   
3. Create a `.env` file to configure the API endpoint:
   env
   REACT_APP_API_URL=http://localhost:4000/api
   

## Usage
1. Start the backend server
   bash
   cd server
   npm start
   
2. Start the frontend development server
   bash
   cd client
   npm start
   
3. Open your browser and navigate to `http://localhost:3000` to begin using the application.

## Implementation Steps
1. Initialize the Node.js project in `server/` and install Express and jsonwebtoken.
2. Create authentication middleware using `jsonwebtoken.verify` to protect routes.
3. Configure Express routes with `express.Router()` for CRUD operations on tasks.
4. Design the Task model to include a `project` and `priority` field.
5. Implement filtering by project and sorting by priority in the backend or expose query parameters.
6. Scaffold the React application in `client/` and set up React Context or localStorage for JWT storage.
7. Build authentication pages (login/register) to retrieve and store the JWT.
8. Create task management components: list, create, update, and delete tasks with project filter and priority sort.
9. Integrate API calls in React, attaching the JWT in the Authorization header for protected routes.
10. Test all features: authentication flow, task CRUD, filtering, and sorting.

## API Endpoints

### Authentication
- POST `/api/auth/register` : Register a new user and receive a JWT in response.
- POST `/api/auth/login`    : Log in an existing user and receive a JWT in response.

### Tasks
- GET `/api/tasks`          : Retrieve all tasks, with optional project filter (e.g., `?project=ProjectName`).
- POST `/api/tasks`         : Create a new task.
- GET `/api/tasks/:id`      : Retrieve a single task by its ID.
- PUT `/api/tasks/:id`      : Update an existing task by its ID.
- DELETE `/api/tasks/:id`   : Delete a task by its ID.