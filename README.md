

---

# 🗨️ Real-Time Chat Application

A **full-stack real-time chat application** built using the **MERN stack (MongoDB, Express.js, React.js, Node.js)** with **Socket.IO** integration for instant messaging capabilities. Designed with authentication, real-time updates, and modern UI/UX.

---

## 🚀 Features

* 🔐 **User Authentication** (JWT + bcrypt)
* 💬 **1-to-1 Real-Time Messaging**
* 👥 **User Online/Offline Presence**
* 🔔 **Instant Notifications**
* 🧵 **Message Threads / Conversations**
* 📅 **Message Timestamps**
* 📦 **Fully RESTful APIs**
* 🌐 **Socket.IO for real-time updates**
* 💡 **Optimized UI using React + Tailwind**
* 🌈 **Dark/Light Mode (optional)**

---

## 🧰 Tech Stack

| Technology   | Usage                         |
| ------------ | ----------------------------- |
| MongoDB      | Database                      |
| Express.js   | Backend Framework             |
| React.js     | Frontend Library              |
| Node.js      | Server Environment            |
| Socket.IO    | Real-time Communication       |
| JWT + bcrypt | Authentication & Security     |
| Tailwind CSS | UI Design                     |
| Zod / Joi    | Request Validation (Optional) |

---

## 📁 Folder Structure

```bash
.
├── backend
│   ├── controllers/
│   ├── models/
│   ├── routes/
│   ├── middleware/
│   ├── config/
│   └── index.ts        # Entry Point
│
├── frontend
│   ├── src/
│   │   ├── components/
│   │   ├── pages/
│   │   ├── context/
│   │   ├── services/
│   │   └── App.tsx
│   └── public/
│
├── .env
├── README.md
└── package.json
```

---

## 🔐 Authentication Flow

1. **Register / Login** via REST API (`/api/auth`)
2. JWT Token is returned and stored in localStorage
3. Protected routes validated using middleware (`verifyToken`)
4. On socket connection, user ID is sent to authenticate socket session

---

## ⚡ Socket.IO Events

| Event          | Direction       | Description                    |
| -------------- | --------------- | ------------------------------ |
| `connect`      | Client → Server | Establish connection           |
| `join`         | Client → Server | Join a conversation room       |
| `message`      | Client ↔ Server | Send and receive messages      |
| `typing`       | Client → Server | Typing indication              |
| `online-users` | Server → Client | List of currently online users |
| `disconnect`   | Client          | Disconnect socket on logout    |

---

## 🧪 API Endpoints

### Auth Routes

```http
POST /api/auth/register
POST /api/auth/login
```

### User Routes

```http
GET /api/users
GET /api/users/:id
```

### Message Routes

```http
GET /api/messages/:conversationId
POST /api/messages
```

### Conversation Routes

```http
GET /api/conversations/:userId
POST /api/conversations
```

---

## 🛠️ Installation & Running

### 1. Clone the Repository

```bash
git clone https://github.com/your-username/mern-socket-chat-app.git
cd mern-socket-chat-app
```

### 2. Backend Setup

```bash
cd backend
npm install
npm run dev
```

> Set environment variables in `.env` file

```env
PORT=5000
MONGO_URI=your_mongo_connection
JWT_SECRET=your_jwt_secret
```

### 3. Frontend Setup

```bash
cd frontend
npm install
npm run dev
```

---

## 📸 Screenshots

> *Optional – Add screenshots or screen recordings here of chat screen, login, etc.*

---

## 🧠 Future Enhancements

* ✅ Group Chat Support
* ✅ Emoji Picker and Media Support
* ✅ Push Notifications (Firebase/Web Push)
* ✅ Admin Panel for User Moderation
* ✅ P2P File Sharing

---

## 🙌 Contributing

Contributions are welcome! Please fork the repo and submit a pull request.

---

## 📝 License

This project is licensed under the MIT License.

---

## 📬 Contact

Made with ❤️ by \[Tarun Pal]

> 📧 [tarunpal0812@gmail.com](mailto:tarunpal0812@gmail.com)
> 🐦 [@tarun_6174](https://twitter.com/@tarun_6174)

---


