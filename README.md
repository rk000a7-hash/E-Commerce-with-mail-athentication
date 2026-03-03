# Python E-Commerce Project

A fully functional, clean, and modern E-Commerce website built using **Python (FastAPI)** for the backend, **React (Vite + Tailwind CSS)** for the frontend, and **MongoDB** for the database.

## Features

- **Authentication:** JWT-based login, register, and Google OAuth 2.0 integration.
- **Product Management:** Browse all products, view details. Admin routes implemented at the API level for CRUD operations.
- **Cart System:** Add to cart, update quantities, remove items, auto-calculate total price, persists mapping to user IDs in MongoDB.
- **Dashboard:** Private route displaying user profile and cart activity.
- **Modern UI:** Tailwind CSS powered responsive interface with Lucide React icons.

## Tech Stack
- **Backend**: Python 3.11+, FastAPI, Uvicorn, MongoDB (motor), PyJWT, Passlib, Pydantic
- **Frontend**: React (Vite), React Router Dom, Tailwind CSS, Axios, Google OAuth.
- **Database**: MongoDB (Local or Atlas compatible)

---

## Prerequisites (Locally)
- Python 3.9+
- Node.js 18+
- MongoDB instance running locally on default port 27017, or a cloud MongoDB Atlas URI.
- Google OAuth Client ID & Secret

---

## Backend Setup

1. **Navigate to backend folder:**
    ```bash
    cd backend
    ```

2. **Create Virtual Environment & Activate:**
    ```bash
    # Windows
    python -m venv venv
    .\venv\Scripts\activate
    
    # macOS/Linux
    python3 -m venv venv
    source venv/bin/activate
    ```

3. **Install Dependencies:**
    ```bash
    pip install -r requirements.txt
    ```

4. **Environment Variables:**
    Update your `.env` file inside `backend/`:
    ```ini
    MONGO_URI=mongodb://localhost:27017
    JWT_SECRET=supersecretkey123
    GOOGLE_CLIENT_ID=your_client_id
    GOOGLE_CLIENT_SECRET=your_client_secret
    ```

5. **Seed Database (Dummy Products):**
    ```bash
    python seed.py
    ```

6. **Run FastAPI Server:**
    ```bash
    uvicorn main:app --reload
    ```
    *The API will be running on http://127.0.0.1:8000. You can visit http://127.0.0.1:8000/docs for the Swagger UI.*

---

## Frontend Setup

1. **Navigate to frontend folder:**
    ```bash
    cd frontend
    ```

2. **Install Node Modules:**
    ```bash
    npm install
    ```

3. **Fix Google Client ID:**
    In `frontend/src/main.jsx`, replace `YOUR_GOOGLE_CLIENT_ID_HERE` with your actual Google Client ID.

4. **Start Vite Dev Server:**
    ```bash
    npm run dev
    ```
    *The site will be running on http://localhost:5173.*
