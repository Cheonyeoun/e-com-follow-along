#ECommerce-Follow-Along 

##Milestone 1: Project Overview to summarize what was covered in the session.

##Project Overview

This project will guide you through building a full-stack e-commerce web application using the MERN stack (MongoDB, Express.js, React.js, Node.js). You will learn how to implement key functionalities such as user authentication, product management, and order handling while gaining hands-on experience with REST APIs, database schema design, and frontend development with React.


###Key Features

-  User Authentication: login and registration with JWT.

-  Product Management: CRUD operations for products, with features like filtering and sorting.

-  Order Handling: Users can place and view orders.

-  REST API: Build scalable API endpoints for managing users, products, and orders.

-  Frontend: Responsive UI built with React for a smooth user experience.


###Technologies Used :

-  Frontend: React.js, Tailwind CSS

-  Backend: Node.js, Express.js

-  Database: MongoDB

## Milestone 2 : Project Setup and Login Page
-  Create a structured folder hierarchy for the project.
-  Set up a React app for the frontend.
-  Set up a Node.js server for the backend.
-  Using Tailwind CSS for streamlined styling.
-  Adding optional extensions for improving development efficiency.
-  Built a styled Login Page for the frontend.

## Milestone 3: Backend Setup and Database Integration  
 
-  **Created folders:**  config,controller,db,middleware,model,utils.
-  Created .env in config, which is used to store environmental variables in a node.js application.

- Made an Errorhandler.js in utils

-  Created auth.js, catchAsyncErrors.js, error.js in middlewares

- **MongoDB Connection:** Configure Mongoose, store credentials in `.env`.  

-  Set up server.js and App.js in the backend folder.

- In db made Database.js which is responsible for connecting your backend to MongoDB using Mongoose.

## Milesstone 4: User Management and File Uploads with Multer

- **Created a User Model:** Defined user schema with required fields.  
- **Developed User Controllers:**  
  - `createUser`: Handles user registration and saves user data.  
  - `getUsers`: Retrieves all registered users.  
- **Set Up Multer for File Uploads:** Configured middleware to handle image uploads.  
- **Created Routes for User Management:**  
  - `POST /users`: Register a new user with profile image upload.  
  - `GET /users`: Fetch all users from the database.  
- **Updated Error Handling:** Improved error handling with `ErrorHandler` and `catchAsyncErrors`.  
- **Tested Endpoints:** Verified functionality using Postman.  

#### Milestone 5: Signup page and Validation  

This milestone focuses on creating a user-friendly Sign-Up page and implementing essential form validation. Key tasks include:  

1. *Frontend UI:* Designed a clean and intuitive Sign-Up page where users can provide their details (Name, Email, Password) to create an account.  
2. *Form Validation:* Ensured user inputs are validated before submission, checking for proper email formats and secure passwords to prevent errors and maintain data integrity.  

By completing this milestone, the application now has a functional and secure user registration interface.

## Milestone 6: User Registration and Authentication
1. User Creation Endpoint (/create-user):
 Implemented an endpoint to create a new user.
 Validated the email to ensure the user doesn’t already exist.
 Successfully handled file uploads (e.g., avatar) using multer.

 2. Password Hashing:
 Used bcryptjs to hash passwords before saving them to the database, ensuring secure password storage.

4. Error Handling:
Incorporated centralized error handling using a custom ErrorHandler class.
Applied catchAsyncErrors middleware to manage asynchronous errors in the routes.

5. User Data Storage:
Stored user details (e.g., name, email, password, avatar) in MongoDB with encrypted password.

6. Email Notification (Optional):
Integrated an email notification system to send a welcome email to the user after successful registration (using sendMail).

7. JWT Token Generation:
Added a method to generate JWT tokens upon user login (for future use in authentication routes).

#### Milestone 7: User Authentication and Login  

This milestone focused on implementing a secure login system by verifying user credentials and ensuring proper authentication.  

**Key tasks included:**  

1. **Create Login Endpoint:**  
   - Developed an API endpoint to accept user credentials (email/username and password).  
   - Retrieved the corresponding user from the database for authentication.  

2. **Validate Password:**  
   - Used `bcrypt` to hash the entered password.  
   - Compared the hashed input with the stored hashed password to authenticate users.  

This milestone enhances security by ensuring only authenticated users gain access.  

#### Milestone 8: Product Card Component and Display  

This milestone focused on designing and implementing a reusable card component to display products effectively on the products page.  

**Key tasks included:**  

1. **Create the Card Component:**  
   - Designed a reusable card component with props for product details (e.g., name, image, price).  
   - Ensured a visually appealing layout to enhance user experience.  

2. **Design the Homepage Layout:**  
   - Implement a grid or flexbox layout for structured product display.  
   - Used mapping to dynamically render multiple product cards with unique details.  

This milestone improves product presentation, creating a clean and user-friendly browsing experience.

**###Milestone 9:Create Product Form**

In this milestone, we have successfully implemented a product creation form that allows users to input all necessary product details and upload multiple images. This form serves as the foundation for managing product data, which will eventually be stored in a database and displayed on the product homepage.

Key Features Implemented

Created a form to input product details, including:

Product Name

Description

Category

Tags

Price

Stock

Email

Product Images (multiple uploads supported)

Implemented image preview functionality for uploaded images.

Used React state management (useState) to handle form inputs dynamically.

Configured React Router to include a new route for the product creation page.

###Milestone 10: Product Management Enhancements


**Milestone 10 focuses on refining the product creation and management process. This includes improving the form submission flow, handling errors effectively, and ensuring a seamless user experience.**

Key Features Implemented

Form Submission & Error Handling

Implemented a structured form to capture product details including:

Name

Description

Price

Category

Tags

Stock

Email

Multiple Images

Integrated multiple image selection for better product representation.

Enhanced error handling using try-catch methods to catch and display errors during product creation.

Debugging tools added to log form data before submission for easier troubleshooting.

API Integration

Built a POST endpoint to receive and validate product data.

Used FormData to handle file uploads efficiently.

Sent form data to the backend API, ensuring proper request formatting (multipart/form-data).

Provided real-time feedback to users on successful product creation or errors encountered.

Why Validation & Error Handling?

Ensures only valid data is stored in the database.

Helps users identify and correct input mistakes quickly.

Prevents incomplete or invalid submissions, reducing inconsistencies in the system.

Technologies Used

React.js for frontend UI

Express.js for backend API handling

MongoDB & Mongoose for database storage

Axios for HTTP requests

Postman for API testing

Next Steps & Enhancements

Implement user authentication to restrict product uploads to authorized users.

Develop an admin panel to manage and moderate product listings.

Introduce real-time image preview and editing capabilities.

Optimize database indexing for faster search and retrieval.

Repository & Submission Details

GitHub Repository: [Your Repository Link Here]

Progress Summary: This milestone enhanced the product creation process by improving form submission, adding error handling, and integrating API communication.

Submission: The repository has been updated, and all changes have been pushed successfully.
**#Milestone 11 - Fetch and Display Products Data**

In this milestone, we implemented the functionality to fetch all products from the backend and dynamically display them on the frontend using components.

Backend (Node.js & Express)
Created an API endpoint to send all product data from the backend to the frontend.
Added a route in index.js to fetch product data.
Used Mongoose to retrieve product details from the database.
Sent the retrieved data as a JSON response.
Frontend (React)
Created a function to fetch product data from the backend.

Used fetch or axios to make a GET request to the backend endpoint.
Stored the response in a state variable using the useState hook.
Used useEffect to trigger the data fetch on component mount.
Displayed the data dynamically using the ProductCard component.

Passed fetched product data as props to the ProductCard component.
Rendered multiple ProductCard components dynamically using .map().

# Milestone 12: My Products Page

## Overview
In this milestone, we will create a "My Products" page that displays all products added by a user based on their email. We will accomplish this by writing a backend endpoint to fetch products from MongoDB filtered by the user's email and dynamically displaying them on the frontend using the previously created product card component.

## Learning Goals 🎯
By the end of this milestone, you will:

- Learn how to write an endpoint to filter and send data from MongoDB based on a user's email.
- Understand how to fetch and receive data on the frontend.
- Display data dynamically using a product card component.

## Steps to Complete Milestone 12 📝

### Backend:
1. **Create an endpoint** in your backend application that retrieves all products associated with a user's email from MongoDB.
2. **Filter products** based on the email provided in the request.
3. **Send the filtered data** as a response to the frontend.

### Frontend:
1. **Write a function** to fetch the filtered product data from the backend.
2. **Process the received data** and pass it to the product card component.
3. **Dynamically display** the products on the "My Products" page.

## Notes
- This lesson will help in understanding how to filter data based on specific constraints and send it to the client efficiently.
- Ensure proper error handling for scenarios where no products are found for a given email.

## Next Steps
- Enhance the UI with better styling and user experience.
- Implement pagination if needed for better performance.
- Add authentication checks to ensure only the logged-in user's products are displayed.

**# Milestone 13: Edit Uploaded Products**
🚀 Overview
In this milestone, we implemented the Edit Product feature. Users can now update product details, with the form auto-filling existing data for a seamless editing experience.

🎯 Key Features
Edit Button added to product cards.
Auto-Fill Form with existing product details.
Update API to modify product data in MongoDB.
Form Submission updates the database with new details.
🛠️ Implementation Steps
Backend: Created an API endpoint to update product details.
Frontend: Added an edit button and handled navigation.
Auto-Fill Form: Preloaded data when editing a product.
Save Changes: Updated product details in the database.
📂 How to Run
Start the backend and frontend servers.
Click "Edit" on a product to update details.
Submit the form to save changes.



**# Milestone 14 - Product Deletion Functionality 🚀**
Overview
In this milestone, we implemented the Delete Product functionality. Users can now remove products from the database using a delete button.

Key Updates
✅ Created a backend endpoint to delete a product by ID in MongoDB.
✅ Updated the frontend to include a delete button for each product.
✅ Integrated API calls to handle the deletion process.

Submission
Code is pushed to the GitHub repository.
The repository is publicly accessible.
Ready for submission in the assignment section.

### Milestone 15: Navbar Component Integration

In this milestone, we'll create and integrate a reusable Navbar component across all screens for smooth navigation.

#### Key Tasks:
- Create a Navbar with links to:
  - Home
  - My Products
  - Add Product
  - Cart
- Make the Navbar responsive.
- Add the Navbar to all pages for easy navigation.

This milestone teaches how to build and reuse a responsive Navbar for seamless navigation.

### Milestone 16: Product Info Page

In this milestone, we will create a page to display product details, choose quantity, and add to the cart.

#### Key Tasks:
- Create a page to display product data.
- Add a quantity selector.
- Implement an "Add to Cart" button.

This milestone focuses on building a functional product info page for users.

### Milestone 17 - Cart Functionality
Overview
In this milestone, we implemented the cart functionality by creating a schema to store products in the cart and an API endpoint to handle product storage.

Tasks Completed
Created a Cart Schema to store product details.
Developed an API Endpoint to receive and store products in the cart.
Integrated the cart functionality with the backend.

Repository
The updated code is available in the GitHub repository.

Submission
Code has been pushed to the repository.
README has been updated with the progress summary.
The repository link has been shared for submission.

### Milestone 18 - Cart Page Backend
Summary
Implemented backend functionality for the cart page by creating endpoints to fetch products inside the cart for a user.

Progress
Developed an API Endpoint for the cart page.
Created an endpoint to retrieve cart products for a user.
Integrated the cart retrieval functionality with the backend.

### Milestone 19: Cart Page UI and Quantity Adjustment
Achievements
In this milestone, I developed the cart page UI and added functionality for adjusting product quantities:

Frontend: Created a Cart Page displaying products with options to increase or decrease the quantity using + and - buttons.
Backend: Developed API endpoints to handle quantity adjustments for each product in the cart.
User Interaction: Enabled real-time updates of the cart quantity on the frontend, ensuring a smooth user experience.
Files Updated
Cart page UI and API integration.
Next Steps
Implement functionality for removing items from the cart.
Add total price calculation and checkout process.

### Milestone 20: User Profile Page

In this milestone, we will build a frontend profile page to display user data and create a backend endpoint to retrieve that data.

#### Key Tasks:
- Create a backend endpoint to send user data using their email.
- Design a frontend profile page to display the user’s profile photo, name, email, and addresses.
- Add a section for addresses with an “Add Address” button, and display “No address found” if no address exists.

This milestone enhances the user experience by providing a profile page to view and manage their information.


### 🏡 Address Form – Milestone 21
📌 Overview
This project implements a frontend Address Form that allows users to input their address details, including:

Country
City
Address Line 1 & 2
Zip Code
Address Type
🎯 Features
✔️React-based address form
 Uses state management to store input data
✔️ Navigates to the form when clicking "Add Address" in the profile page
✔️ Submits the form data via API

📥 Submission
Code pushed to GitHub
Repository is publicly accessible
README updated with progress


### Milestone 22 - Save Address in User Profile
Overview
In this milestone, we created a backend endpoint to store user addresses in the database. The endpoint receives address details from the frontend form and appends them to the address array in the user collection.

Learning Outcomes
Implemented an API endpoint to handle address storage.
Updated the user collection to include multiple addresses.
Strengthened backend skills for handling user profiles.
Submission Details
Code pushed to GitHub repository.
Repository is publicly accessible.

=======
=======


### Milestone 23: Implementing Place Order & Select Address Page
Overview
In this milestone, we implemented the Place Order functionality in our e-commerce project. This includes adding a button inside the cart page, creating a select address page, and setting up the backend to handle addresses.

Features Implemented
✔️ Place Order Button: Added inside the cart page, redirects to the select address page.
✔️ Select Address Page: Displays all saved addresses and allows the user to choose a delivery address.
✔️ Backend API for Addresses: Created an endpoint to fetch user addresses.
✔️ Order Schema: Defined the schema for storing order details in MongoDB.

Steps Completed
Added a "Place Order" button inside the cart page.
Created a select address page with all saved addresses.
Developed a backend API to retrieve user addresses.
Defined a MongoDB schema to store order details.
Submission Details
Code pushed to GitHub ✔️
Repository is publicly accessible ✔️
README updated ✔️
=======




### Milestone 24 - Order Confirmation Page 🚀
Overview
In this milestone, we implemented the Order Confirmation Page, where users can review their order details before finalizing the purchase.

Key Features
✔️ Display all the ordered products.
✔️ Show the selected delivery address.
✔️ Calculate and display the total price of the cart.
✔️ Provide a "Place Order" button to confirm the purchase.

Implementation Steps
1️⃣ Fetch and display ordered products.
2️⃣ Show the selected address for delivery.
3️⃣ Calculate the total order value dynamically.
4️⃣ Add a "Place Order" button to proceed with checkout.

Submission Details
📌 Code pushed to GitHub 📂
📌 Public repository link updated 🔗
📌 Assignment submitted successfully ✅

🎉 Milestone 24 completed!

# Milestone 25 - Place Order Endpoint  

## Overview  
In this milestone, we created a backend endpoint to handle order placement in our e-commerce application.  

## Key Tasks  
- Developed an endpoint to receive product, user, and address details.  
- Retrieved the user's `_id` using their email.  
- Created separate orders for each product with the same address.  
- Stored order details in the MongoDB `orders` collection using the order schema.  

## Learning Outcome  
- Gained experience in handling order processing through a backend API.  

## Submission  
- Code pushed to GitHub (public repository).  
- README updated with milestone progress.  
- Repository link shared for submission.  


# Milestone 26 - Get User Orders Endpoint  

## Overview  
In this milestone, we created a backend endpoint to retrieve all orders placed by a user.  

## Key Tasks  
- Developed an endpoint that receives the user's email.  
- Retrieved the user's `_id` using their email.  
- Fetched all orders associated with the user's `_id` from the database.  
- Sent the list of orders in the response.  

## Learning Outcome  
- Gained experience in fetching and managing user-specific order data.  

## Submission  
- Code pushed to GitHub (public repository).  
- README updated with milestone progress.  
- Repository link shared for submission.  

## README - Milestone 27: My Orders Page  

### Overview  
In this milestone, we created a **My Orders** page for our frontend. This page fetches and displays all user orders by sending a GET request to the `my-orders` endpoint using the user’s email.  

### Learning Goals 🎯  
- Implement a frontend page to display user orders.  
- Send a request to retrieve order data from the backend.  
- Integrate the **My Orders** page into the navbar for easy access.  

### Implementation Steps 📝  
1. Created a **My Orders** page.  
2. Sent a GET request to fetch user orders using their email.  
3. Displayed the retrieved orders on the page.  
4. Updated the navbar to include the **My Orders** page for better navigation.  

### Submission Guidelines 📥  
- Code pushed to the GitHub repository.  
- Repository is publicly accessible.  
- README updated with milestone details.  
- Repository link submitted as per guidelines.  

🚀 **Milestone 27 completed successfully!**



## README - Milestone 28: Cancel Order Feature  

### Overview  
In this milestone, we enhanced the **My Orders** page by adding a **Cancel Order** button and implemented a backend endpoint to handle order cancellations.  

### Learning Goals 🎯  
- Enable users to cancel placed orders.  
- Implement order cancellation logic in the frontend and backend.  
- Prevent the cancel button from appearing for already canceled orders.  

### Implementation Steps 📝  
1. Added a **Cancel Order** button for each order in the **My Orders** page.  
2. Ensured the button is hidden for already canceled orders.  
3. Created a backend endpoint to receive an `order-id`, find the order, update its status to **canceled**, and save the changes.  

### Submission Guidelines 📥  
- Code pushed to the GitHub repository.  
- Repository is publicly accessible.  
- README updated with milestone details.  
- Repository link submitted as per guidelines.  

🚀 **Milestone 28 completed successfully!**


### Milestone 29 - PayPal Integration
### Milestone Overview
In this milestone, I have started integrating an online payment gateway using the PayPal API in my application.

Key Implementations
✔ Created a PayPal Developer Account and set up a Sandbox Account.
✔ Retrieved and saved the Sandbox User ID and Client ID.
✔ Updated the order confirmation page with two payment options:

Cash on Delivery (COD)
Online Payment via PayPal
✔ Implemented radio buttons to toggle between COD and PayPal payment.
✔ Prepared the UI to display PayPal payment buttons (to be coded in the next milestone).
Next Steps
Implement the functionality for PayPal payment processing in the upcoming milestone.

# Milestone 30 - PayPal Payment Integration

This project implements an online payment gateway using the PayPal API in a React application.

## Features
- Integrated PayPal API for secure payments.
- Used `react-paypal-js` for seamless UI integration.
- Supports multiple payment methods like credit/debit cards.

## Installation
1. Clone the repository:
    ```bash
    git clone <repository-url>
    ```
2. Install dependencies:
    ```bash
    npm install
    ```
3. Add your PayPal client key in a `.env` file:
    ```env
    REACT_APP_PAYPAL_CLIENT_ID=your-client-id
    ```
4. Start the application:
    ```bash
    npm run dev
    ```

## Usage
- Access the payment page and proceed with PayPal payment.

## Technologies Used
- React
- PayPal API
- react-paypal-js

---

✅ Successfully completed Milestone 30.  


# Milestone 31: Global State Management with Redux

## Overview
In this milestone, I implemented global state management using **Redux** to store user data.

## Features Implemented
- Installed `react-redux` for state management.
- Created a `store` folder with:
  - **store.js**: Configured a Redux store with a `userReducer` to manage user email state.
  - **userActions.js**: Implemented a `setEmail` action to update the email in the global state.
- Wrapped the App component with the Redux `Provider` in **index.js**.

## Installation
1. Clone the repository:
    ```bash
    git clone <repo-link>
    ```
2. Install dependencies:
    ```bash
    npm install
    ```
3. Start the project:
    ```bash
    npm run dev
    ```

## Usage
- The global state now holds the user email, which can be accessed and updated from any component.

## Next Steps
- In the next milestone, I will implement email state management across components.

 
### Milestone 32: Global State Management with Redux
Overview
In this milestone, we implemented Redux to manage the global state for user authentication. Specifically, we stored the user's email in the Redux store and accessed it across all pages.

Steps Completed
✅ Used useDispatch to store the email in the global state upon login.
✅ Used useSelector to access the email across all pages.
✅ Integrated Redux for centralized state management.

Technologies Used
React

Redux Toolkit

React-Redux

### Milestone 33: JWT Token & Cookie Storage
Overview
In this milestone, we implemented JSON Web Token (JWT) authentication by generating a token and storing it in a cookie for secure session management.

Steps Completed
✅ Installed jsonwebtoken package using NPM.
✅ Used sign method to generate a JWT with email and user ID.
✅ Set maxAge to define the token expiration time.
✅ Stored the JWT inside a cookie in the response.

Technologies Used
Node.js

Express.js

JSON Web Token (JWT)

Cookie Parser

### Milestone 34: JWT Token Validation
Overview
This milestone focuses on implementing JWT authentication by validating the token stored in cookies. It ensures that only authenticated users can access protected routes.

Learning Goals
Extract the JWT token from browser cookies and send it to the server.

Validate the received JWT token on the backend.

Prevent unauthorized users from accessing protected pages.

Implementation Steps
1️⃣ Extract JWT Token from Cookies
The frontend retrieves the token stored in cookies and sends it with requests to the server.

Ensure that requests include credentials for secure authentication.

2️⃣ Validate JWT Token in Backend
The backend middleware extracts and verifies the token using a secret key.

If valid, the user is granted access; otherwise, an error response is sent.

3️⃣ Protect Routes
Apply authentication checks to restrict access to certain API endpoints.

Ensure that only logged-in users can access protected data.

4️⃣ Enforce Authentication in Frontend
Redirect users to the login page if they are not authenticated.

Prevent navigation to protected pages without a valid session.
---

### Milestone 35: Deployment done.
- Frontend & Backend Deployed.

Conclusion
By implementing JWT validation, we enhance security and ensure users can only access resources they are authorized for. 🚀
