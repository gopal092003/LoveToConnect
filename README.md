# LoveToConnect

LoveToConnect is a full-stack language exchange platform that helps people connect with native speakers, practice new languages through real-time conversations, and build friendships across different cultures.

Users can create profiles, discover language partners based on their learning goals, send friend requests, exchange messages, and start video calls directly within the application.

The project was built to explore real-time communication systems, third-party SDK integration, authentication, and scalable full-stack application development.

---

## Overview

The platform enables users to find compatible language partners based on the languages they speak and want to learn. It combines user authentication, social networking features, real-time messaging, and video calling into a single application with a responsive interface.

---

## Features

### User Authentication

* Secure user registration and login
* JWT authentication using HTTP-only cookies
* Persistent user sessions

### Language Partner Discovery

* Set native and learning languages
* Discover recommended language partners
* View user profiles and biographies

### Friend Management

* Send friend requests
* Accept or decline requests
* Manage existing connections

### Real-Time Messaging

* One-to-one messaging using Stream Chat
* Instant message delivery
* Conversation history

### Video Calling

* Start video calls directly from conversations
* Share meeting links through chat
* Real-time communication powered by Stream Video

### User Interface

* Responsive layout
* Multiple DaisyUI themes
* Persistent theme preferences

---

## Technology Stack

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

## Project Structure

```
LoveToConnect/
│
├── backend/
│   └── src/
│       ├── controllers/
│       ├── lib/
│       ├── middleware/
│       ├── models/
│       ├── routes/
│       └── server.js
│
├── frontend/
│   └── src/
│       ├── components/
│       ├── constants/
│       ├── hooks/
│       ├── lib/
│       ├── pages/
│       └── store/
│
└── package.json
```

---

## API Overview

### Authentication

| Method | Endpoint               | Description               |
| ------ | ---------------------- | ------------------------- |
| POST   | `/api/auth/signup`     | Register a new user       |
| POST   | `/api/auth/login`      | Authenticate a user       |
| POST   | `/api/auth/logout`     | End the current session   |
| POST   | `/api/auth/onboarding` | Complete profile setup    |
| GET    | `/api/auth/me`         | Retrieve the current user |

### Users

| Method | Endpoint                               | Description                |
| ------ | -------------------------------------- | -------------------------- |
| GET    | `/api/users`                           | Retrieve recommended users |
| GET    | `/api/users/friends`                   | Retrieve friend list       |
| POST   | `/api/users/friend-request/:id`        | Send a friend request      |
| PUT    | `/api/users/friend-request/:id/accept` | Accept a friend request    |
| GET    | `/api/users/friend-requests`           | Retrieve incoming requests |
| GET    | `/api/users/outgoing-friend-requests`  | Retrieve outgoing requests |

### Chat

| Method | Endpoint          | Description                            |
| ------ | ----------------- | -------------------------------------- |
| GET    | `/api/chat/token` | Generate a Stream authentication token |

---

## Installation

### Prerequisites

* Node.js 22 or later
* MongoDB Atlas or a local MongoDB instance
* Stream account for Chat and Video APIs

---

## Clone the Repository

```
git clone https://github.com/gopal092003/LoveToConnect.git

cd LoveToConnect
```

---

## Backend Configuration

Create a `.env` file inside the `backend` directory.

```env
PORT=5001

MONGO_URI=your_mongodb_connection_string

JWT_SECRET_KEY=your_jwt_secret

STREAM_API_KEY=your_stream_api_key
STREAM_API_SECRET=your_stream_api_secret

NODE_ENV=development
```

Install dependencies:

```
cd backend

npm install
```

Start the development server:

```
npm run dev
```

---

## Frontend Configuration

Create a `.env` file inside the `frontend` directory.

```env
VITE_STREAM_API_KEY=your_stream_api_key

VITE_APP_BACKEND_URL=http://localhost:5001
```

Install dependencies:

```
cd frontend

npm install
```

Start the development server:

```
npm run dev
```

---

## Local Development

Frontend:

```
http://localhost:5173
```

Backend:

```
http://localhost:5001
```

---

## Production Build

Build the application:

```
npm run build
```

Start the production server:

```
npm start
```

The backend is configured to serve the frontend build, allowing deployment as a single application.

---

## What I Learned

This project provided hands-on experience with:

* Building a full-stack application using React and Express
* Implementing JWT-based authentication
* Designing MongoDB schemas with Mongoose
* Integrating Stream Chat and Stream Video SDKs
* Managing asynchronous server state with TanStack Query
* Global state management with Zustand
* Building responsive and customizable user interfaces
* Organizing scalable frontend and backend architectures

---

## Future Improvements

* Group conversations
* Audio-only calls
* Interest-based user matching
* Language proficiency tracking
* Push notifications
* User blocking and reporting
* Online presence indicators

---

## Author

**Gopal Gupta**

GitHub: https://github.com/gopal092003

---

## License

This project is intended for educational purposes and personal learning.
