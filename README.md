# **Node.js Authentication App**

This is a basic authentication application built with **Node.js**, **Express**, **EJS**, **MongoDB**, and **bcrypt** for hashing passwords. The app allows users to sign up, log in, and access a protected home page.

---

## **Features**
- User signup with hashed password storage.
- User login with JWT-based authentication.
- Error handling for invalid credentials.
- Uses cookies for secure authentication.
- Dynamic rendering of pages using **EJS** templates.

---

## **Technologies Used**
- **Node.js**: Backend runtime environment.
- **Express**: Web framework for routing and handling requests.
- **EJS**: Templating engine for rendering views.
- **MongoDB**: Database for storing user data.
- **Mongoose**: ODM for MongoDB integration.
- **bcrypt**: Password hashing for secure storage.
- **jsonwebtoken**: JWT creation for user authentication.

---

## **Getting Started**

### **1. Prerequisites**
Ensure you have the following installed:
- Node.js (v14+)
- MongoDB (running locally or cloud service like MongoDB Atlas)

---

### **2. Installation**
1. Clone this repository:
   ```bash
   git clone https://github.com/your-username/auth-app.git
   cd auth-app
   ```

2. Install dependencies:
   ```bash
   npm install
   ```

3. Create a `.env` file in the root of your project and configure the following:
   ```env
   JWT_SECRET=your-secret-key
   MONGO_URI=your-mongodb-connection-string
   ```

4. Start your MongoDB server (if running locally):
   ```bash
   mongod
   ```

---

### **3. Usage**
1. Run the development server:
   ```bash
   npm start
   ```

2. Open your browser and navigate to:
   ```
   http://localhost:3000
   ```

---

### **Project Structure**
```
├── src
│   ├── model
│   │   └── user.js       # Mongoose schema for user
│   ├── routes
│   │   └── authRoute.js  # Authentication routes
│   ├── views
│   │   ├── login.ejs     # Login page
│   │   ├── signup.ejs    # Signup page
│   │   └── home.ejs      # Home page
│   └── app.js            # Main app entry point
├── public
│   └── style.css         # CSS for styling
├── .env                  # Environment variables
├── package.json          # Project dependencies
└── README.md             # Project documentation
```

---

## **Endpoints**
| **Method** | **Route**    | **Description**                  |
|------------|--------------|----------------------------------|
| `GET`      | `/`          | Home page (protected route)     |
| `GET`      | `/signup`    | Signup form                    |
| `POST`     | `/signup`    | Create a new user              |
| `GET`      | `/login`     | Login form                     |
| `POST`     | `/login`     | Authenticate user              |
---

## **Future Improvements**
- Implement password reset.
- Role-based access control (e.g., admin vs. user).
- Improve UI/UX with frameworks like Bootstrap or TailwindCSS.
---

## **License**
This project is licensed under the MIT License. See the `LICENSE` file for details.

---
