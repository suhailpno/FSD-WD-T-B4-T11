**User Authorization and Authentication - MERN Backend**
========================================================

This is a **User Authorization and Authentication** project built using the **MERN stack** (MongoDB, Express, React, Node.js). It provides essential routes for user sign-up, login, and logout functionality, along with JWT-based authentication for secure routes.

**Features**
------------

*   **Sign-Up:** Allows new users to create accounts.
    
*   **Login:** Authenticated users can log in using their credentials.
    
*   **Logout:** Users can log out and clear their JWT cookie.
    
*   **JWT Authentication:** Secure user access to protected routes with JWT tokens.
    

**Project Setup**
-----------------

### **1\. Clone the repository**

git clone https://github.com/suhailpno/FSD-WD-T-B4-T11.git   `

### **2\. Install Dependencies**

Navigate to your project folder and run:

npm install   `

### **3\. Create a .env file**

Create a .env file in the root of your project directory and add the following:

DBURI=mongodb+srv://zenfsd:zenfsd@cluster0.wpk7u.mongodb.net/?retryWrites=true&w=majority  
JWT_SECRET=your-secret-key   `

### **4\. Run the Application**

Start your server:

npm start   `

The backend will be running on http://localhost:3000.

**Routes Overview**
-------------------

The following routes are available in the application:

### **1\. Sign Up**

*   **Route:** /signup
    
*   **Method:** GET
    
*   **Description:** Displays the Sign-Up page.
    
*   **Route:** /signup
    
*   **Method:** POST
    
*   **Description:** Registers a new user by creating a user document in the database.
    
    *   { "username": "JohnDoe", "email": "johndoe@example.com", "password": "password123"}
        
    *   { "user": { "id": "userId", "email": "johndoe@example.com" }, "token": "jwtTokenHere"}
        
    *   { "errors": { "email": "Email already exists" }}
        

### **2\. Login**

*   **Route:** /login
    
*   **Method:** GET
    
*   **Description:** Displays the Login page.
    
*   **Route:** /login
    
*   **Method:** POST
    
*   **Description:** Logs in a user and generates a JWT token.
    
    *   { "email": "johndoe@example.com", "password": "password123"}
        
    *   { "user": { "id": "userId", "email": "johndoe@example.com" }, "token": "jwtTokenHere"}
        
    *   { "errors": { "email": "No user found with this email" }}
        

### **3\. Logout**

*   **Route:** /logout
    
*   **Method:** GET
    
*   **Description:** Logs out the user by clearing the JWT cookie.
    
    *   { "message": "Logged out successfully"}
        

**Postman API Documentation**
-----------------------------

The following Postman collection is available for testing the API:

1.  **Sign-Up (POST /signup)**
    
    *   { "username": "JohnDoe", "email": "johndoe@example.com", "password": "password123"}
        
    *   **Response:**
        
        *   { "user": { "id": "userId", "email": "johndoe@example.com" }, "token": "jwtTokenHere"}
            
        *   { "errors": { "email": "Email already exists" }}
            
2.  **Login (POST /login)**
    
    *   { "email": "johndoe@example.com", "password": "password123"}
        
    *   **Response:**
        
        *   { "user": { "id": "userId", "email": "johndoe@example.com" }, "token": "jwtTokenHere"}
            
        *   { "errors": { "email": "No user found with this email" }}
            
3.  **Logout (GET /logout)**
    
    *   { "message": "Logged out successfully"}
        

**License**
-----------

This project is licensed under the MIT License.
