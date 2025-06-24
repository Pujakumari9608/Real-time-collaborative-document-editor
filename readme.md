# Your Full-Stack Web Application

This repository contains a full-stack web application demonstrating integration between:
- **Frontend:** ReactJS
- **Backend 1:** Node.js with Express
- **Backend 2:** Python with Flask
- **Database:** MongoDB

## Project Structure


your-fullstack-app/
├── client/             # ReactJS frontend application
├── server/             # Contains both Node.js and Flask backends
│   ├── nodejs/         # Node.js Express backend
│   └── flask/          # Python Flask backend
├── .env                # Environment variables (MongoDB URI, port numbers)
└── README.md           # This file


## Setup and Running Instructions

Follow these steps to get the application running on your local machine.

### 1. MongoDB Setup

Ensure MongoDB is installed and running on your system.
- Download from [https://www.mongodb.com/try/download/community](https://www.mongodb.com/try/download/community)
- Start the MongoDB daemon (e.g., `mongod` in your terminal).

### 2. Environment Variables

Create a `.env` file in the root of the `your-fullstack-app` directory with the following content:


MONGODB_URI=mongodb://localhost:27017/my_first_db
NODEJS_PORT=5000
FLASK_PORT=5001


### 3. Node.js Backend Setup

1.  Navigate to the Node.js backend directory:
    ```bash
    cd your-fullstack-app/server/nodejs
    ```
2.  Install dependencies:
    ```bash
    npm install
    ```
3.  Start the Node.js server:
    ```bash
    npm start
    # Or for development with auto-restart:
    # npm run dev
    ```
    The server will run on `http://localhost:5000`.

### 4. Flask Backend Setup

1.  Navigate to the Flask backend directory:
    ```bash
    cd your-fullstack-app/server/flask
    ```
2.  (Optional but Recommended) Create and activate a Python virtual environment:
    ```bash
    python3 -m venv venv
    # On macOS/Linux:
    source venv/bin/activate
    # On Windows:
    .\venv\Scripts\activate
    ```
3.  Install dependencies:
    ```bash
    pip install -r requirements.txt
    ```
4.  Start the Flask server:
    ```bash
    python app.py
    ```
    The server will run on `http://localhost:5001`.

### 5. React Frontend Setup

1.  Navigate to the React frontend directory:
    ```bash
    cd your-fullstack-app/client
    ```
2.  If you haven't already, create the React app (this will create boilerplate files, some of which you'll replace):
    ```bash
    npx create-react-app .
    ```
3.  **Important:** Replace the content of `src/App.js`, `src/index.js`, `src/index.css`, and `public/index.html` with the provided code.
4.  Install dependencies:
    ```bash
    npm install
    ```
5.  Start the React development server:
    ```bash
    npm start
    ```
    The application will open in your browser, usually at `http://localhost:3000`.

## Usage

Once all components are running:
- The React frontend at `http://localhost:3000` will fetch data from both the Node.js backend (`http://localhost:5000/api/nodejs/data`) and the Flask backend (`http://localhost:5001/api/flask/data`).
- The backends will store and retrieve a simple message in your MongoDB database (`my_first_db`).

This project serves as a foundational example. You can expand upon it by adding more complex data models, user authentication, and advanced UI features.
