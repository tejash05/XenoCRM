# ⚙️ XenoCRM Backend – Node.js + Express + MongoDB

This is the backend service for **XenoCRM**, an AI-powered mini CRM platform that supports user authentication, campaign management, AI message suggestions, and delivery simulation.

---

## 🚀 Features

- ✅ JWT-based authentication with Email/Password and Google OAuth  
- ✅ REST APIs for managing campaigns and logs  
- ✅ AI-powered message suggestions using OpenAI or Groq (LLaMA 3)  
- ✅ Delivery simulation and logging  
- ✅ MongoDB integration for storing users, campaigns, and communication logs  

---

## 🛠 Tech Stack Badges

![Node.js](https://img.shields.io/badge/Node.js-339933?style=for-the-badge&logo=nodedotjs&logoColor=white)
![Express](https://img.shields.io/badge/Express-000000?style=for-the-badge&logo=express&logoColor=white)
![MongoDB](https://img.shields.io/badge/MongoDB-4EA94B?style=for-the-badge&logo=mongodb&logoColor=white)
![OpenAI](https://img.shields.io/badge/OpenAI-412991?style=for-the-badge&logo=openai&logoColor=white)
![Render](https://img.shields.io/badge/Render-00979D?style=for-the-badge&logo=render&logoColor=white)

---

## 📁 Folder Structure (Backend only)

xeno-backend/
├── controllers/ # Business logic (auth, campaign, AI)
├── models/ # Mongoose models (User, Campaign, Logs)
├── routes/ # API route definitions
├── scripts/ # Utility scripts (if any)
├── utils/ # Helpers like prompt generators, logger
├── .env # Environment config (MONGO_URI, JWT_SECRET, etc.)
├── package.json # Backend dependencies
└── server.js # Entry point for Express app


---

## ⚙️ Setup Instructions

### 🔹 1. Navigate to Backend Folder

```bash
cd xeno-backend
```
🔹 2. Install Dependencies
```
npm install
```
🔹 3. Set Up Environment Variables

Create a .env file with the following:
```
MONGO_URI=your_mongodb_uri
JWT_SECRET=your_secret
OPENAI_API_KEY=your_openai_or_groq_key
GOOGLE_CLIENT_ID=your_google_client_id
GOOGLE_CLIENT_SECRET=your_google_secret
```

Refer to .env.example if available.
🧠 Key API Endpoints
🧠 Message Suggestions

POST /api/ai/suggest-messages
```
{ "objective": "bring back inactive users" }
```
📤 Simulate Delivery

PATCH /api/campaigns/:id
```
{ "status": "sent", "message": "Hey, we miss you!" }
```
📄 View Logs
```
GET /api/communication-logs/:campaignId
```
🌐 Hosted Backend

🔗 https://xeno-crm-r2jm.onrender.com
📹 Demo Video

🎥 Watch Demo
