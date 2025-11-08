# 🔐 Secure Chat Application

A **real-time end-to-end encrypted chat app** built with the MERN stack and Socket.IO.  
It allows users to register, log in, exchange encrypted messages, and share encrypted files securely.

---

## 🚀 Features

- 🔑 **User Authentication** (JWT-based)
- 💬 **Real-time Messaging** using Socket.IO
- 🧑‍🤝‍🧑 **Search and Chat** with registered users
- 🛡️ **End-to-End Encryption** (public/private key)
- 📁 **Encrypted File Uploads**
- 🔐 **Secure Private Key Storage** (encrypted client-side)
- 🌐 **MERN Stack** (MongoDB, Express, React, Node.js)

---

## 📂 Project Structure

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

## ⚙️ Installation & Setup

### 1. Clone Repository
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

🔌 API Routes Overview
Method	Endpoint	Description
POST	/api/auth/register	Register new user
POST	/api/auth/login	Login existing user
GET	/api/auth/:id/publicKey	Get public key of another user
GET	/api/auth/me/privateKey	Get encrypted private key of logged-in user
GET	/api/messages?with=<userId>	Fetch chat messages with a user
POST	/api/messages/upload	Upload encrypted file

🧠 Tech Stack
Frontend:

React (Vite)

Axios

Tailwind CSS

Socket.IO Client

Backend:

Node.js + Express

MongoDB + Mongoose

JWT Authentication

Socket.IO

Multer (file uploads)

💬 Usage
Register a new user or log in.

You’ll be redirected to the chat dashboard.

Search for other users and start chatting.

Messages and file transfers are securely encrypted.

You can reopen the app anytime and continue chatting safely.

🧰 Development Scripts
Command	Description
npm run dev	Run development server (both backend/frontend)
npm start	Run production mode (for backend only)
npm run build	Build frontend for production

🛠️ Troubleshooting
401 Unauthorized → Make sure JWT secret in .env matches for both login & verification.

404 Errors → Ensure backend is running on port 4000 and frontend .env points correctly.

Socket Connection Failed → Check CORS configuration in src/server.js.

🧾 License
This project is licensed under the MIT License.
