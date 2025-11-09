# 🧩 REST API with Node.js and MongoDB Atlas

This project demonstrates how to build a **REST API** using **Node.js**, **Express**, and **MongoDB Atlas**. It allows users to perform **CRUD operations** (Create, Read, Update, Delete) and test endpoints using **Postman**. The database is hosted entirely in the cloud using MongoDB Atlas, following a complete step-by-step setup process.

---

## 📦 Features
- Node.js backend using Express  
- MongoDB Atlas cloud database  
- CRUD functionality for user data  
- Environment variables stored in `.env`  
- API tested using Postman  
- Step-by-step setup with the modern Atlas interface  

---

## 🧰 Requirements
Before starting, make sure you have:  
- Node.js (version 18 or newer) – https://nodejs.org  
- MongoDB Atlas account (free tier) – https://www.mongodb.com/atlas  
- Postman – https://www.postman.com/downloads/  
- A text editor such as **Visual Studio Code**  

---

## ☁️ MongoDB Atlas Setup (Step-by-Step)

### 1️⃣ Create a New Project
1. Log in to MongoDB Atlas.  
2. Click **“New Project”**.  
3. Enter your project name (for example, `REST-API-Project`).  
4. Leave tags empty (optional).  
5. Click **Next**, confirm you are the **Project Owner**, then click **Create Project**.

---

### 2️⃣ Create a Cluster
1. After your project is created, click **“Create a Cluster”**.  
2. Under **Deploy your cluster**, select the **Free** plan (M0).  
3. Click **Create Deployment**.

---

### 3️⃣ Configure the Cluster
1. Enter a **Cluster Name** (for example, `Clustername`).  
2. Choose **AWS** as the provider.  
3. Select a region such as **Frankfurt (eu-central-1)**.  
4. Click **Create Deployment** and wait for the cluster to be provisioned.

---

### 4️⃣ Set Up Connection Security
When the cluster is ready, Atlas will open the **Connect to Clustername** wizard.

**Step 1 – Add a connection IP address**  
- Click **Add your current IP address** so your local machine can connect.

**Step 2 – Create a database user**  
- Set a username, for example: `danielmiuta11_db_user`.  
- Copy the generated password and store it somewhere safe.  
- Click **Create Database User**.  

Then click **Choose a connection method**.

---

### 5️⃣ Choose Connection Method
1. Under **Connect to your application**, click **Drivers**.  
2. For **Driver**, choose **Node.js**.  
3. For **Version**, choose **6.7 or later**.

---

### 6️⃣ Get Your Connection String
Atlas will show a connection string similar to:

    mongodb+srv://db_user:<password>@clustername.3ufwzrr.mongodb.net/?appName=Clustername

Copy this string. You will use it in your `.env` file.  
Remember to replace `db_user` with your db username `<password>` with your actual database user password.

---

## ⚙️ Local Project Setup

### 1️⃣ Create or Clone the Project
If you already have a GitHub repository:

    git clone https://github.com/DanielMiuta24/rest-api.git
    cd rest-api

Otherwise, create a new folder manually and open it in **VS Code**.

---

### 2️⃣ Initialize Node.js

    npm init -y

This creates a `package.json` file with default settings.

---

### 3️⃣ Install Dependencies

    npm install express mongoose dotenv nodemon

- **Express** – backend framework for handling routes and middleware  
- **Mongoose** – connects and interacts with MongoDB Atlas  
- **Dotenv** – loads environment variables from `.env`  
- **Nodemon** – restarts the server automatically when files change  

---

### 4️⃣ Create Your `.env` File
At the root of your project, create a file named `.env` with:

    MONGO_URI=mongodb+srv://db_user:<password>@clustername.3ufwzrr.mongodb.net/restapi
    PORT=5000

Replace  `db_use`r and `<password>` with your actual Atlas data.  
The `restapi` database will be created automatically when data is inserted.

---

### 5️⃣ Configure `package.json` Scripts
In `package.json`, update the `scripts` section:

    "scripts": {
      "dev": "nodemon server.js",
      "start": "node server.js"
    }

Now you can run the app with `npm run dev` (development) or `npm start` (production).

---

### 6️⃣ Project Structure
Your folder structure should look similar to:

    rest-api/
     ├── server.js
     ├── routes/
     │   └── userRoutes.js
     ├── controllers/
     │   └── userController.js
     ├── models/
     │   └── User.js
     ├── .env
     ├── package.json
     └── README.md

---

### 7️⃣ Start the Server
To start the backend:

    npm run dev

or:

    node server.js

If everything is configured correctly, the terminal should show something like:

    ✅ MongoDB connected
    🚀 Server running on port 5000

---

## 🧪 Testing the API with Postman

1. Open **Postman**.  
2. Use the base URL:

       http://localhost:5000/api/users

3. Test the endpoints:

- **GET** `/api/users` – retrieve all users  
- **GET** `/api/users/:id` – retrieve a specific user by ID  
- **POST** `/api/users` – create a new user  
- **PUT** `/api/users/:id` – update an existing user  
- **DELETE** `/api/users/:id` – delete a user  

4. For POST/PUT requests, go to the **Body** tab → choose **raw** → **JSON** and send something like:

       {
         "name": "Daniel",
         "email": "daniel@example.com",
         "age": 25
       }

5. Go back to MongoDB Atlas → your cluster → **Browse Collections** and confirm that documents are created, updated, or deleted according to your requests.

---

## 📚 Learning Outcomes
After completing this tutorial, you will be able to:

- Understand REST API concepts and HTTP request methods  
- Connect a Node.js application to MongoDB Atlas  
- Organize your backend using models, controllers, and routes  
- Use Postman to test and debug API endpoints  
- Manage and monitor your data directly in MongoDB Atlas  

---

## 👨‍💻 Author
**Daniel Miuta**




