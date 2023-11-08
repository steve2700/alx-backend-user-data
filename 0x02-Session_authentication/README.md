
# 0x02-Session_authentication Project README

Welcome to 0x02-Session_authentication, a secure and user-friendly authentication project implemented in Python 3.7 using Flask. This project utilizes session-based authentication, storing user data in cookies for seamless and secure user experiences.

## Features:

1. **User Registration:**
   - Users can register by providing a unique username and a strong password.
   - Passwords are securely hashed and stored for enhanced security.

2. **User Login:**
   - Registered users can log in using their credentials.
   - Passwords are verified securely, and users are granted access upon successful login.

3. **Session Authentication:**
   - User sessions are managed securely using cookies.
   - Authenticated users can navigate through the application without re-entering credentials for each request.

4. **User Profile Management:**
   - Authenticated users can manage their profiles, update information, and change passwords.

5. **Logout Functionality:**
   - Users can log out securely, terminating their active session.

6. **Error Handling:**
   - Robust error handling mechanisms to provide meaningful messages for different scenarios.

7. **Simple and Intuitive UI:**
   - User-friendly interfaces for registration, login, and profile management.

8. **Secure Data Storage:**
   - User data and session information are securely stored and managed.

## Getting Started:

To run this project locally, follow these steps:

1. **Clone the Repository:**
   ```
   git clone https://github.com/steve2700/0x02-Session_authentication.git
   ```

2. **Navigate to the Project Directory:**
   ```
   cd 0x02-Session_authentication
   ```

3. **Install Dependencies:**
   ```
   pip install -r requirements.txt
   ```

4. **Run the Application:**
   ```
   python app.py
   ```

   The application will be accessible at `http://localhost:5000` in your web browser.

## Usage:

1. **Registration:**
   - Access the registration page and provide a unique username and password to create an account.

2. **Login:**
   - Use your registered credentials to log in securely.

3. **Profile Management:**
   - Navigate to the profile section to update your information or change your password.

4. **Logout:**
   - Log out of your account to terminate the active session.

## Contributors:

- Stewart Nyaruwata(nyaruwatastewart27@gmail.com)

## Issues and Feedback:

If you encounter any issues or have suggestions for improvement, please [create an issue](https://github.com/steve2700/0x02-Session_authentication/issues) in this repository.

---

### Understanding Session Authentication:

Session authentication is a method of verifying the identity of users during their interaction with a web application. Unlike basic authentication, which requires sending credentials with every request, session authentication allows users to log in once and then access protected resources without re-entering their credentials. This is achieved through the use of session tokens stored in cookies.

#### How Session Authentication Works:

1. **User Login:**
   - When a user successfully logs in, the server generates a unique session token.
   - This session token is associated with the user's account and stored in a secure server-side data store (e.g., a database).

2. **Sending Session Token to Client:**
   - The server sends the session token to the client's browser in the form of a cookie.
   - The cookie is automatically included in the headers of subsequent requests made by the client.

3. **Session Verification:**
   - When the client makes a request, the server reads the session token from the cookie.
   - The server verifies the session token against the stored session data to ensure the user is authenticated.

4. **Access Control:**
   - Authenticated users are granted access to protected resources.
   - If the session token is invalid or expired, the user is redirected to the login page.

#### Diagram:

```
+-------------+                   +-------------+
|   Client    |                   |   Server    |
|             |                   |             |
|   Login     |                   |             |
|  Request    |                   |             |
|  ---------> |                   |             |
|             |                   |             |
|   Session   |                   |             |
|   Token     |  --(includes)-->  |             |
|  <--------  |                   |             |
|             |                   |             |
|             |                   | Session     |
|             |                   | Verification|
|             |                   |   & Access  |
|             |                   |   Control   |
|             |                   |             |
+-------------+                   +-------------+
```

#### Example Scenario:

1. **User Login:**
   - User enters credentials and logs in.
   - Server generates a session token (e.g., `abc123`) and sends it in a cookie.

2. **Subsequent Requests:**
   - User navigates to various pages within the application.
   - Client's browser automatically includes the `abc123` cookie in the headers of each request.

3. **Session Verification:**
   - Server reads the `abc123` token from the cookie.
   - Server verifies the token against the stored session data.
   - If valid, the user is allowed to access the requested resources.

4. **User Logout:**
   - User logs out, and the session token is invalidated on the server side.
   - Subsequent requests with the `abc123` token will be denied access.

---

This document provides an overview of session authentication, its functionality, and a sample implementation in a Python Flask application. If you have any further questions or need additional clarification, feel free to reach out. Happy coding!

---
