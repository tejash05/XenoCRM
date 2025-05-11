# 📊 XenoCRM – AI-Driven Mini CRM Campaign Platform

**XenoCRM** is a dynamic Mini CRM and campaign simulator, designed for real-time customer targeting, AI-assisted messaging, and delivery simulation.  
Built with a robust **MERN + GPT** stack, it enables efficient marketing communication with intelligent message generation, actionable analytics, and secure authentication.

---

## 🚀 Why XenoCRM?

- ✅ Real-time customer targeting by tags and filters  
- ✅ AI-powered message suggestion using GPT-4
- ✅ Simulated delivery system with tracking and logs  
- ✅ Secure login with Email & Google OAuth  
- ✅ Detailed logs for sent, failed, and delivered messages  

---

## 📌 Features

### 🔹 Campaign Management
- Create campaigns with title, objective, and target tags  
- Add message content or auto-generate with AI  
- Simulate delivery to matching users  
- Track communication logs per campaign  

### 🔹 AI Message Suggestions
- Powered by OpenAI 
- Suggests 2–3 message variants per objective  
- Intelligent tone, wordings, and personalization  

### 🔹 Communication Log
- Records delivery per customer  
- Includes status: delivered / failed  
- Logs sent time, message, and target ID  

### 🔹 Authentication System
- Email/password & Google OAuth via Passport.js  
- Stores user name and email  
- Secure token-based session handling  

---

## 🧰 Tools Used

- React + Vite  
- Tailwind CSS  
- Express.js  
- MongoDB  
- OpenAI / Groq  
- Postman  
- Render  
- React Router  
- Google OAuth  

---

## 🛠️ Tech Stack Badges

![React](https://img.shields.io/badge/React-20232A?style=for-the-badge&logo=react&logoColor=61DAFB)
![MongoDB](https://img.shields.io/badge/MongoDB-4EA94B?style=for-the-badge&logo=mongodb&logoColor=white)
![Postman](https://img.shields.io/badge/Postman-FF6C37?style=for-the-badge&logo=postman&logoColor=white)
![Render](https://img.shields.io/badge/Render-00979D?style=for-the-badge&logo=render&logoColor=white)
![OpenAI](https://img.shields.io/badge/OpenAI-412991?style=for-the-badge&logo=openai&logoColor=white)
![Tailwind CSS](https://img.shields.io/badge/Tailwind_CSS-06B6D4?style=for-the-badge&logo=tailwind-css&logoColor=white)
![React Router](https://img.shields.io/badge/React_Router-CA4245?style=for-the-badge&logo=react-router&logoColor=white)
![Vite](https://img.shields.io/badge/Vite-646CFF?style=for-the-badge&logo=vite&logoColor=white)
![Express](https://img.shields.io/badge/Express-000000?style=for-the-badge&logo=express&logoColor=white)

---

## 📁 Folder Structure
```
XenoCRM/
├── xeno-backend/                     # ⚙️ Backend - Node.js + Express
│   ├── controllers/                 # Business logic (auth, campaign, AI)
│   ├── models/                      # Mongoose models (User, Campaign, Logs)
│   ├── routes/                      # API route definitions
│   ├── scripts/                     # Utility scripts (if any)
│   ├── utils/                       # Helpers like prompt generators, logger
│   ├── .env                         # Environment config (MONGO_URI, JWT, etc.)
│   ├── package.json                 # Backend dependencies
│   └── server.js                    # Entry point for Express app

├── xeno-frontEnd/                   # 🎨 Frontend - React + Vite + Tailwind
│   ├── public/                      # Static assets (favicon, etc.)
│   ├── src/                         # Main source folder
│   │   ├── assets/                 # Images, logos, etc.
│   │   ├── components/            # Reusable UI components
│   │   ├── pages/                 # Page components (Home, Auth, History)
│   │   ├── services/              # API integration (axios logic)
│   │   ├── App.jsx                # Root component
│   │   └── main.jsx               # React DOM entry point
│   ├── .env                        # Frontend env (VITE_GOOGLE_CLIENT_ID)
│   ├── package.json                # Frontend dependencies
│   ├── tailwind.config.cjs        # TailwindCSS config
│   └── vite.config.js             # Vite config for dev/build

├── .gitignore                      # Shared git ignore file
└── README.md                       # Project documentation

```

---

## ⚙️ Setup & Installation

### 🔹 1. Clone the Repository
```bash
git clone https://github.com/your-username/XenoCRM.git
cd XenoCRM
```
🔹 2. Install Dependencies
```
cd client
npm install

cd ../server
npm install
```
🔹 3. Set Environment Variables

Create a .env file in the server folder:
```
MONGO_URI=your_mongodb_uri
JWT_SECRET=your_secret
OPENAI_API_KEY=your_openai_or_groq_key
GOOGLE_CLIENT_ID=your_google_client_id
GOOGLE_CLIENT_SECRET=your_google_secret
```

Use .env.example as a template.
🔹 4. Run the App

# Terminal 1
```
cd server
npm run dev
```

# Terminal 2
```
cd client
npm run dev
```

🔄 API Endpoints
🧠 POST /api/suggest-message

Request:
```
{ "objective": "bring back inactive users" }
```
Response: AI-generated message variants.
📤 POST /api/campaign/send

Simulates sending messages and logs delivery.
📄 GET /api/campaign/logs/:campaignId

Returns communication log with delivery/failure timestamps.

🔄 API Endpoints
🧠 Message Suggestions

POST /api/ai/suggest-messages
```
{
  "objective": "bring back inactive users"
}
```
📤 Simulate Delivery

PATCH /api/campaigns/:id
```
{
  "status": "sent",
  "message": "Hey, we miss you!"
}
```
📄 View Logs

-GET /api/communication-logs/:campaignId

✨ Contributors
-Name	Role
-Tejash Tarun	Full Stack Dev, AI Integration, Delivery Logic
-Team	Auth System, UI/UX Design, Backend Setup


## 🌐 Project Links

- 📹 [Demo Video](https://drive.google.com/file/d/1WGbAl9j2kEBCB7TaSfinZqKPM1oaLPut/view?usp=drive_link)  
- 💻 [Frontend (React + Vite)](https://xeno-frontend-3qja.onrender.com)  
- ⚙️ [Backend (Node.js + Express)](https://xeno-crm-r2jm.onrender.com)
