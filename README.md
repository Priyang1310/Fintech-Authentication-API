
# FinTech Authentication API

This is a simple authentication system for a FinTech application, implemented using Node.js, Express.js, and MongoDB. The application supports user registration, login functionalities, and includes robust error handling mechanisms.

## Table of Contents

- [Setup Instructions](#setup-instructions)
- [How to Run the Application](#how-to-run-the-application)
- [How to Import and Use the Postman Collection](#how-to-import-and-use-the-postman-collection)
- [Assumptions and Decisions](#assumptions-and-decisions)

## Setup Instructions

1. **Clone the Repository**
   ```bash
   git clone https://github.com/YOUR_USERNAME/Fintech-Authentication-API.git
   cd Fintech-Authentication-API
   ```

2. **Install Dependencies**
   Ensure you have [Node.js](https://nodejs.org/) and [MongoDB](https://www.mongodb.com/) installed. Then, run:
   ```bash
   npm install
   ```

3. **Create a `.env` File**
   Create a `.env` file in the root directory and add the following environment variables:
   ```plaintext
   PORT=5000
   MONGODB_URI=mongodb://localhost:27017/fintech-auth
   JWT_SECRET=your_jwt_secret_key
   ```

   Replace `your_jwt_secret_key` with a secure key of your choice.

## How to Run the Application

1. **Start MongoDB**
   Make sure your MongoDB server is running. If you have MongoDB installed locally, you can start it by running:
   ```bash
   mongod
   ```

2. **Run the Application**
   In the terminal, navigate to your project directory and run:
   ```bash
   npm start
   ```
   The server will start on the specified port (default is `5000`).

3. **Access the API**
   You can access the API at `http://localhost:5000/api`.

## How to Import and Use the Postman Collection

1. **Download the Postman Collection**
   The Postman collection is included in this repository as `FintechAuth.postman_collection.json`.

2. **Import the Collection into Postman**
   - Open Postman.
   - Click on `Import` in the top left corner.
   - Select the `File` tab and drag `FintechAuth.postman_collection.json` into the window or click `Choose Files` and select the file.

3. **Set Up Environment Variables in Postman**
   - Go to the **Environments** tab.
   - Create a new environment and add a variable named `TOKEN`.
   - Use this variable to store your JWT token when logging in.

4. **Testing the API**
   - Use the collection to test all available endpoints, including registration, login, and profile retrieval.
   - Review the expected responses for successful and erroneous requests as documented in the collection.

## Assumptions and Decisions

- **User Passwords**: Passwords are hashed using `bcrypt` before storage to ensure security.
- **JWT Authentication**: JSON Web Tokens are used for user authentication, ensuring secure and stateless sessions.
- **Error Handling**: Appropriate HTTP status codes and error messages are returned for different error scenarios to enhance user experience.
- **Data Validation**: Input validation checks are implemented for registration and login to ensure data integrity and prevent injection attacks.
- **Testing**: The API has been thoroughly tested using Postman, covering various scenarios, including valid and invalid inputs.

## License

This project is licensed under the MIT License.
