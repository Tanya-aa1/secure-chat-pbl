#  Secure Chat Application

A **real-time end-to-end encrypted chat app** built with the MERN stack and Socket.IO.  
It allows users to register, log in, exchange encrypted messages, and share encrypted files securely.

---

##  Features

-  **User Authentication** (JWT-based)
-  **Real-time Messaging** using Socket.IO
-  **Search and Chat** with registered users
-  **End-to-End Encryption** (public/private key)
-  **Encrypted File Uploads**
-  **Secure Private Key Storage** (encrypted client-side)
-  **MERN Stack** (MongoDB, Express, React, Node.js)

---

##  Project Structure

secure-chat/
│
├── backend/ # Express + MongoDB + Socket.IO server
│ ├── src/
│ │ ├── models/ # Mongoose models (User, Message)
│ │ ├── routes/ # Auth, User, Message routes
│ │ ├── middleware/ # Auth middleware (JWT verification)
│ │ ├── utils/ # JWT helpers
│ │ └── server.js # Main entry point
│ ├── .env.example # Example environment variables
│ ├── package.json
│ └── ...
│
├── frontend/ # React + Vite frontend
│ ├── src/
│ │ ├── pages/ # Login, Register, Chat
│ │ ├── components/ # ChatWindow, MessageInput, etc.
│ │ └── ...
│ ├── vite.config.js
│ ├── package.json
│ └── ...
│
└── README.md

---

##  Installation & Setup

1. Clone Repository

```bash
git clone https://github.com/<your-username>/secure-chat.git
cd secure-chat

2. Backend Setup

cd backend
npm install
Create .env file inside backend/:
MONGO_URI=mongodb://localhost:27017/secure_chat
JWT_SECRET=your_secret_key_here
PORT=4000
Start backend:
npm run dev
Server will run at http://localhost:4000

3. Frontend Setup

Open a new terminal:
cd frontend
npm install
Create .env file inside frontend/:
VITE_API_URL=http://localhost:4000
Run frontend:
npm run dev
Frontend will run at http://localhost:5173

