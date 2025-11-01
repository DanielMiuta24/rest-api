# 🧩 REST API with Node.js and MongoDB

This project is a simple REST API built using Node.js, Express, and MongoDB. It demonstrates how to perform CRUD operations (Create, Read, Update, Delete) using HTTP requests tested with Postman. It is part of an E-Portfolio presentation to demonstrate backend development.

---

## 📦 Features

• Express.js backend with controllers, models, and routes  
• MongoDB integration (local or Atlas)  
• CRUD functionality for user data  
• Environment variables using .env  
• Testing with Postman  
• Step-by-step tutorial included  
• Ideal for educational and demo purposes  

---

## 🧰 Requirements

Before starting, make sure you have installed:  
• Node.js (version 18 or newer)  
• MongoDB Community Server or MongoDB Atlas  
• MongoDB Compass  
• Postman  
• A text editor such as Visual Studio Code  

---

## ⚙️ Setup Tutorial (Step by Step)

### 1. Create or Clone the Project
If you already have a GitHub repository, clone it with:  
git clone https://github.com/DanielMiuta24/rest-api.git  
cd rest-api  
Otherwise, create a new folder manually and open it in VS Code.  

---

### 2. Initialize Node.js
Run the following command to create a package.json file:  
npm init -y  

---

### 3. Install Dependencies
Install the required packages:  
npm install express mongoose dotenv nodemon  

Express is used for the backend framework.  
Mongoose is used to interact with MongoDB.  
Dotenv loads environment variables from a .env file.  
Nodemon restarts the server automatically when files change.  

---

### 4. Configure package.json
Open the package.json file and add the following under the scripts section:  
“dev”: “nodemon server.js”  
“start”: “node server.js”  

This allows you to start the app using either npm run dev for development (auto reload) or node server.js for normal runs.  

---

### 5. Create the .env File
At the root of your project, create a file named .env and add:  
MONGO_URI=mongodb://127.0.0.1:27017/restapi  
PORT=5000  

If you use MongoDB Atlas, replace the URI with your Atlas connection string.  

---

### 6. Project Structure
After setup, your project should contain the following folders and files:  
server.js  
routes/  
controllers/  
models/  
.env  
package.json  
README.md  

---

### 7. Start the Server
Start your backend with one of the following commands:  
npm run dev  
or  
node server.js  

If the setup is correct, the terminal will display:  
MongoDB connected  
Server running on port 5000  

---

### 8. Test the API with Postman
Once your server is running, open Postman and test the following endpoints:

GET /api/users → Retrieve all users  
GET /api/users/:id → Retrieve a user by ID  
POST /api/users → Add a new user  
PUT /api/users/:id → Update an existing user  
DELETE /api/users/:id → Delete a user  

Example workflow in Postman:  
1. Create a user using POST with a JSON body containing name, email, and age.  
2. Retrieve all users using GET to confirm creation.  
3. Update a specific user by its ID using PUT.  
4. Delete that user using DELETE.  
5. Confirm changes visually in MongoDB Compass.  

---

### 9. Verify Data in MongoDB Compass
Open MongoDB Compass, connect to mongodb://127.0.0.1:27017, open the database restapi, and view the collection users. You should see the data you created or modified from Postman.  

---

## 📚 Learning Outcomes

After following this tutorial, you will be able to:  
• Understand how REST APIs work.  
• Connect a Node.js app with MongoDB.  
• Handle requests using Express routes and controllers.  
• Use Postman to send and test API requests.  
• Manage persistent data with MongoDB Compass.  

---

## 🔒 Security Notice

This project is intentionally open for learning purposes.  
In a real-world environment, you should implement:  
• Input validation with express-validator.  
• Authentication using JWT tokens.  
• Authorization and user roles.  
• Rate limiting with express-rate-limit.  
• Cross-Origin Resource Sharing (CORS) configuration.  
• Proper error handling middleware.  

---

## 👨‍💻 Author

**Daniel Miuta**  


---

## 📝 License

This project is created for educational purposes.  
You are free to reuse, share, or modify it for your own learning or portfolio.
