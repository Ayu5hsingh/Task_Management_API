# **Task Management API (Express, MongoDB, JWT)**

## **🚀 Overview**
The **Task Management API** is a **secure, token-based authentication system** built with **Node.js, Express.js, MongoDB, and JWT**. This API allows users to manage their tasks efficiently while ensuring data privacy and security.  

### **🔹 Features**
✅ **User Registration & Login** (JWT-based authentication)  
✅ **CRUD Operations on Tasks** (Create, Read, Update, Delete)  
✅ **Mark Tasks as Completed**  
✅ **JWT Protected Routes** (Users can only manage their own tasks)  
✅ **Secure Password Hashing** with `bcrypt.js`  
✅ **RESTful API with JSON Responses**  

---

## **🛠️ Installation & Setup**
### **1️⃣ Clone the Repository**
```sh
git clone https://github.com/ayu5hsingh/Task_Management_API.git
cd Task_Management_API
```

### **2️⃣ Install Dependencies**
```sh
npm install
```

### **3️⃣ Set Up Environment Variables**
Create a `.env` file in the root directory and add the following:
```env
PORT=5000
MONGO_URI=mongodb+srv://your_username:your_password@your_cluster.mongodb.net/taskdb
JWT_SECRET=your_super_secret_key
```

### **4️⃣ Start the Server**
#### Development Mode:
```sh
npm run dev
```
#### Production Mode:
```sh
npm start
```

---

## **🔗 How to Use**
### **🔹 User Authentication**
- **Register**: `POST /api/auth/register`
- **Login**: `POST /api/auth/login` _(Returns JWT token)_

### **🔹 Task Management (Requires JWT)**
- **Create Task**: `POST /api/tasks`
- **Get All Tasks**: `GET /api/tasks`
- **Update Task**: `PUT /api/tasks/:id`
- **Delete Task**: `DELETE /api/tasks/:id`

#### **🛠️ Authorization**
All task-related requests must include a **JWT token** in the headers:
```http
Authorization: Bearer your_jwt_token
```

---

## **🔐 Security Features**
- Passwords are **hashed** using `bcrypt.js` before storing them.
- JWT ensures **secure, token-based authentication**.
- API routes are **protected**, ensuring users access only their own data.
- **Helmet.js** for additional security headers.

---

## **📁 Project Structure**
```
task-manager-api/
│── models/                # Database models (User, Task)
│── routes/                # API route handlers
│── middleware/            # JWT Authentication Middleware
│── .env                   # Environment Variables
│── server.js              # Entry point of the API
│── package.json           # Dependencies and scripts
└── README.md              # Documentation
```

---

## **🚀 Next Steps**
✅ Deploy the API on **Render, Vercel, or Heroku**  
✅ Build a **React.js frontend** to create a full-stack app  
✅ Add **Task Prioritization, Due Dates, and Notifications**  

---

## **📜 License**
This project is licensed under the **MIT License**.  

For questions or contributions, feel free to reach out! 🚀🔥

