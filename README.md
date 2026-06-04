# ❤️ LoveToConnect

A full-stack language exchange platform that helps people connect with native speakers, practice new languages through real conversations, and build friendships across cultures.

Users can create profiles, discover language partners based on their learning goals, send friend requests, chat in real time, and start video calls directly within the platform.

This project was built to gain hands-on experience with real-time communication systems, third-party SDK integration, authentication, and full-stack application architecture.

---

## ✨ Features

### 👤 User Authentication

* Sign up and log in securely
* JWT authentication using httpOnly cookies
* Persistent user sessions

### 🌍 Language Partner Discovery

* Set your native language and learning language
* Get recommendations for potential language partners
* View user profiles and bios

### 🤝 Friend System

* Send friend requests
* Accept or reject incoming requests
* Manage your connections

### 💬 Real-Time Messaging

* One-on-one chat powered by Stream Chat
* Instant message delivery
* Conversation history

### 📹 Video Calling

* Start video calls directly from chat
* Share join links through messages
* Real-time communication powered by Stream Video

### 🎨 Customizable UI

* 32 DaisyUI themes
* Theme preference persisted across sessions
* Fully responsive design

---

## 🛠 Tech Stack

### Frontend

* React 19
* Vite
* React Router v7
* TanStack Query
* Zustand
* Tailwind CSS
* DaisyUI
* Axios
* React Hot Toast
* Stream Chat React SDK
* Stream Video React SDK

### Backend

* Node.js
* Express.js
* MongoDB
* Mongoose
* JWT Authentication
* bcryptjs
* Stream Chat Node SDK

---

## 📁 Project Structure

```text
LoveToConnect/
├── backend/
│   └── src/
│       ├── controllers/
│       ├── middleware/
│       ├── models/
│       ├── routes/
│       ├── lib/
│       └── server.js
│
├── frontend/
│   └── src/
│       ├── components/
│       ├── pages/
│       ├── hooks/
│       ├── store/
│       ├── lib/
│       └── constants/
│
└── package.json
```

---

## 🔌 API Overview

### Authentication

| Method | Endpoint               | Description            |
| ------ | ---------------------- | ---------------------- |
| POST   | `/api/auth/signup`     | Create account         |
| POST   | `/api/auth/login`      | Login user             |
| POST   | `/api/auth/logout`     | Logout user            |
| POST   | `/api/auth/onboarding` | Complete profile setup |
| GET    | `/api/auth/me`         | Get current user       |

### Users

| Method | Endpoint                               | Description         |
| ------ | -------------------------------------- | ------------------- |
| GET    | `/api/users`                           | Recommended users   |
| GET    | `/api/users/friends`                   | Friend list         |
| POST   | `/api/users/friend-request/:id`        | Send friend request |
| PUT    | `/api/users/friend-request/:id/accept` | Accept request      |
| GET    | `/api/users/friend-requests`           | Incoming requests   |
| GET    | `/api/users/outgoing-friend-requests`  | Sent requests       |

### Chat

| Method | Endpoint          | Description           |
| ------ | ----------------- | --------------------- |
| GET    | `/api/chat/token` | Generate Stream token |

---

## 🚀 Running Locally

### Prerequisites

* Node.js 22+
* MongoDB Atlas or local MongoDB instance
* Stream account for Chat and Video APIs

### 1. Clone the Repository

```bash
git clone https://github.com/gopal092003/LoveToConnect.git
cd LoveToConnect
```

### 2. Backend Environment Variables

Create:

```bash
backend/.env
```

```env
PORT=5001
MONGO_URI=your_mongodb_connection_string

JWT_SECRET_KEY=your_jwt_secret

STREAM_API_KEY=your_stream_api_key
STREAM_API_SECRET=your_stream_api_secret

NODE_ENV=development
```

### 3. Frontend Environment Variables

Create:

```bash
frontend/.env
```

```env
VITE_STREAM_API_KEY=your_stream_api_key
VITE_APP_BACKEND_URL=http://localhost:5001
```

### 4. Install Dependencies

Backend:

```bash
cd backend
npm install
```

Frontend:

```bash
cd frontend
npm install
```

### 5. Start Development Servers

Backend:

```bash
npm run dev
```

Frontend (in a separate terminal):

```bash
npm run dev
```

Frontend:

```
http://localhost:5173
```

Backend:

```
http://localhost:5001
```

---

## 🏗 Production Build

Build the application:

```bash
npm run build
```

Start the server:

```bash
npm start
```

The backend is configured to serve the frontend build files, enabling deployment as a single service.

---

## 🎯 What I Learned

* Building a complete full-stack application from scratch
* JWT authentication and secure session management
* MongoDB data modeling with Mongoose
* Integrating Stream Chat and Stream Video SDKs
* Managing server state with TanStack Query
* Global state management with Zustand
* Designing responsive and themeable user interfaces
* Structuring scalable frontend and backend architectures

---

## 🔮 Future Improvements

* Group conversations
* Audio-only calls
* Advanced user matching based on interests
* Language proficiency levels
* Push notifications
* User blocking and reporting
* Online presence indicators

---

## 👨‍💻 Author

**Gopal**

GitHub: https://github.com/gopal092003

If you found this project interesting, feel free to star the repository.
