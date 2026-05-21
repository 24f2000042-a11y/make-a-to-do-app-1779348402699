# Todo App (MERN Stack)

A simple, modern, blue‑themed Todo application built with **React + Vite** on the frontend and **Node.js + Express + MongoDB** on the backend.

## Features
- Create, read, update (toggle complete), and delete todos.
- Responsive design with a clean blue UI.
- RESTful API using Express.
- MongoDB for persistent storage.
- Environment variables for configuration.

## Project Structure

root/
├─ backend/          # Express server
│   ├─ server.js
│   ├─ package.json
│   └─ .env.example
└─ frontend/         # Vite + React app
    ├─ src/
    │   ├─ App.jsx
    │   ├─ App.css
    │   └─ main.jsx
    ├─ index.html
    └─ package.json


## Prerequisites
- Node.js (v18 or later)
- npm or yarn
- A MongoDB database (local or Atlas)

## Setup
### Backend
1. Navigate to the backend folder:
   bash
   cd backend
   
2. Install dependencies:
   bash
   npm install
   
3. Create a `.env` file based on `.env.example` and add your MongoDB connection string:
   bash
   cp .env.example .env
   
4. Start the server:
   bash
   npm run dev   # uses nodemon for hot reload
   
   The API will be available at `http://localhost:5000`.

### Frontend
1. Open a new terminal and go to the frontend folder:
   bash
   cd frontend
   
2. Install dependencies:
   bash
   npm install
   
3. (Optional) Create a `.env` file to override the API URL:
   bash
   VITE_API_URL=http://localhost:5000
   
4. Run the development server:
   bash
   npm run dev
   
   Open `http://localhost:5173` in your browser.

## API Endpoints
| Method | Endpoint           | Description                     |
|--------|--------------------|---------------------------------|
| GET    | `/api/todos`       | Get all todos                   |
| POST   | `/api/todos`       | Create a new todo (`{ text }`)  |
| PUT    | `/api/todos/:id`   | Update a todo (e.g., toggle `completed`) |
| DELETE | `/api/todos/:id`   | Delete a todo                   |

## Styling
The app uses a modern blue color palette defined in `src/App.css`. Feel free to customize the colors or layout.

## License
This project is open‑source and available under the MIT License.
