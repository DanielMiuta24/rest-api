# 🧩 REST API with Node.js and MongoDB

This project is a simple REST API built using **Node.js**, **Express**, and **MongoDB Atlas**. It demonstrates how to perform **CRUD operations** (Create, Read, Update, Delete) using HTTP requests tested with **Postman**. It was developed as part of an **E-Portfolio presentation** to demonstrate backend development in practice.

---

## 📦 Features
- Express.js backend with controllers, models, and routes  
- MongoDB Atlas cloud integration  
- CRUD functionality for user data  
- Environment variables using `.env`  
- Testing with Postman  
- Step-by-step setup tutorial included  
- Ideal for educational and demo purposes  

---

## 🧰 Requirements
Before starting, make sure you have:  
- [Node.js (version 18 or newer)](https://nodejs.org)  
- [MongoDB Atlas account (free tier)](https://www.mongodb.com/atlas)  
- [Postman (API testing tool)](https://www.postman.com/downloads/)  
- A text editor such as **Visual Studio Code**  

---

## ☁️ MongoDB Atlas Setup (Cloud Database)
### 1️⃣ Create a Free Atlas Account  
Go to [https://www.mongodb.com/atlas](https://www.mongodb.com/atlas) and create a free account. You can sign up using your Google account or with an email and password.

### 2️⃣ Create a New Cluster  
After logging in:  
- Click **“Build a Database”**  
- Choose **Free Tier (M0)**  
- Select a region near you  
- Click **“Create Deployment”**  
Atlas will take a few minutes to deploy your free cluster.

### 3️⃣ Add a Database User  
Once your cluster is ready:  
- Go to **Database Access** → click **“Add New Database User”**  
- Choose a username (for example, `daniel`) and create a password  
- Select **“Read and write to any database”**  
- Click **“Add User”**  
Keep your username and password handy — you’ll need them to connect.

### 4️⃣ Allow Network Access  
Go to **Network Access** → click **“Add IP Address”**.  
Choose **“Allow access from anywhere (0.0.0.0/0)”** → Confirm.  
This will allow your application to connect to your Atlas cluster from your computer.

### 5️⃣ Get the Connection String  
Return to **Database → Connect → Drivers → Node.js**.  
Copy the connection string — it should look similar to this:  
`mongodb+srv://<username>:<password>@cluster0.xxxxxx.mongodb.net/`

### 6️⃣ Create Your .env File  
In the root of your project, create a file named `.env` and paste this:  
`MONGO_URI=mongodb+srv://daniel:<password>@cluster0.xxxxxx.mongodb.net/restapi`  
`PORT=5000`  
Replace `<password>` with your actual password from step 3.  
The database **restapi** will be automatically created when you add your first data.

---

## ⚙️ Project Setup (Step-by-Step)
### 1️⃣ Create or Clone the Project  
If you already have a GitHub repository, clone it with:  
`git clone https://github.com/DanielMiuta24/rest-api.git`  
`cd rest-api`  
Otherwise, create a new folder manually and open it in **VS Code**.

### 2️⃣ Initialize Node.js  
Run this command to create a new Node.js project:  
`npm init -y`

### 3️⃣ Install Dependencies  
Install the required packages by running:  
`npm install express mongoose dotenv nodemon`  
Here’s what each package does:  
- **Express** – Framework for creating the backend server  
- **Mongoose** – Connects Node.js to MongoDB Atlas  
- **Dotenv** – Loads environment variables from a `.env` file  
- **Nodemon** – Automatically restarts the server during development  

### 4️⃣ Configure package.json  
Open your `package.json` and update the **scripts** section:  
`"scripts": { "dev": "nodemon server.js", "start": "node server.js" }`  
Now you can use:  
- `npm run dev` for development mode (auto-reload)  
- `node server.js` for normal run  

### 5️⃣ Project Structure  
After setup, your project should contain the following files and folders:  
- `server.js` → main entry file  
- `routes/` → contains API route definitions  
- `controllers/` → contains business logic  
- `models/` → defines data structure for MongoDB  
- `.env` → stores environment variables  
- `package.json` → project configuration  
- `README.md` → project documentation  

### 6️⃣ Start the Server  
Start your backend server using one of the following commands:  
`npm run dev`  
or  
`node server.js`  
If everything is set up correctly, you should see in your terminal:  
✅ MongoDB connected  
🚀 Server running on port 5000  

### 7️⃣ Test the API with Postman  
Once your server is running, open **Postman** and test the API endpoints.  
Available routes:  
- **GET** `/api/users` → Retrieve all users  
- **GET** `/api/users/:id` → Retrieve a specific user  
- **POST** `/api/users` → Add a new user  
- **PUT** `/api/users/:id` → Update an existing user  
- **DELETE** `/api/users/:id` → Delete a user  
**Example testing flow:**  
1. Send a **POST** request to create a new user with fields like name, email, and age.  
2. Use **GET** to retrieve all users and confirm the new one appears.  
3. Send a **PUT** request to update user data.  
4. Use **DELETE** to remove that user.  
5. Open your MongoDB Atlas cluster → click **Browse Collections** → confirm your changes are reflected.  

---

## 📚 Learning Outcomes  
After completing this tutorial, you will:  
- Understand REST API architecture and HTTP methods  
- Learn how to connect Node.js with MongoDB Atlas  
- Organize your project using routes, controllers, and models  
- Use Postman to send and test API requests  
- Manage and view your data directly in MongoDB Atlas  

---

## 👨‍💻 Author  
**Daniel Miuta**




