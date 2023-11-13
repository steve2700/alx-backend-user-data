# 0x03 User Authentication Service

## Overview

This project is a powerful User Authentication Service built using Flask, a lightweight and flexible Python web framework. The authentication process is enhanced with the use of bcrypt for secure password hashing, ensuring the protection of user credentials.

## Features

- **Flask Backend**: The backend is developed using Flask, a web framework that simplifies the process of building robust web applications.

- **Secure Password Hashing**: User passwords are securely hashed using bcrypt, a key derivation function designed for secure password hashing.

## Getting Started

### Installation

To install the required dependencies, run the following command:

```bash
pip install -r requirements.txt
```

### Running the Application

```bash
python app.py
```

The application will start, and you can access it by navigating to [http://localhost:5000](http://localhost:5000) in your web browser.

## Project Structure

The project directory structure is organized for clarity and maintainability:

- **`app.py`**: Main entry point for the Flask application.
  
- **`user.py`**: Defines the SQLAlchemy model for the `users` table.

- **`requirements.txt`**: Contains the necessary dependencies. Install them using `pip install -r requirements.txt`.

## SQLAlchemy Model

The `User` model is defined with the following attributes:

- `id` (Integer, Primary Key)
- `email` (String, Non-nullable)
- `hashed_password` (String, Non-nullable)
- `session_id` (String, Nullable)
- `reset_token` (String, Nullable)

## Usage

The User Authentication Service provides a solid foundation for building secure user authentication features in your web applications. Use the provided SQLAlchemy model as a basis for managing user data securely.

## Contributing

Feel free to contribute to the project by submitting issues or pull requests. Your feedback and contributions are highly appreciated.

## License

This project is licensed under the [MIT License](LICENSE). Feel free to use, modify, and distribute the code for your projects.

---

Thank you for using the 0x03 User Authentication Service! If you have any questions or need assistance, please don't hesitate to reach out.
