
# Authentication and Base64 Encoding

Welcome to the official documentation for Authentication and Base64 Encoding! 🚀

This README provides a user-friendly guide to understanding authentication, Base64 encoding, Basic Authentication, and how to send the Authorization header using Python.

## What is Authentication?

**Definition:** Authentication is the process of proving your identity to access something, like logging into an account with a username and password.

**Example:** Logging into an email account by entering your email and password.

## What is Base64 Encoding?

**Definition:** Base64 encoding is a way to convert data (text, binary, etc.) into a safe format for transmission, often used in web applications.

**Example:** Converting the word "hello" to Base64 results in "aGVsbG8=".

## How to Encode a String in Base64:

In Python, you can encode a string to Base64 like this:

```python
import base64
encoded_message = base64.b64encode("hello".encode())
print(encoded_message.decode())  # Output: "aGVsbG8="
```

## What is Basic Authentication?

**Definition:** Basic Authentication is a method to access restricted resources by sending your username and password in an encoded form.

**Example:** Sending a request with your username and password encoded in Base64 in the Authorization header:

```
Authorization: Basic YWxhZGRpbjpvcGVuc2VzYW1l
```

## How to Send the Authorization Header in Python:

In Python, you can send the Authorization header using the `requests` library:

```python
import requests
url = "https://api.example.com/data"
headers = {"Authorization": "Basic YWxhZGRpbjpvcGVuc2VzYW1l"}
response = requests.get(url, headers=headers)
```

This sends a GET request to `https://api.example.com/data` with the Basic Authentication header attache this README to explain authentication, Base64 encoding, and Basic Authentication in your projects. Happy coding! 🎉

# Simple API

Simple HTTP API for playing with `User` model.


## Files

### `models/`

- `base.py`: base of all models of the API - handle serialization to file
- `user.py`: user model

### `api/v1`

- `app.py`: entry point of the API
- `views/index.py`: basic endpoints of the API: `/status` and `/stats`
- `views/users.py`: all users endpoints


## Setup

```
$ pip3 install -r requirements.txt
```


## Run

```
$ API_HOST=0.0.0.0 API_PORT=5000 python3 -m api.v1.app
```


## Routes

- `GET /api/v1/status`: returns the status of the API
- `GET /api/v1/stats`: returns some stats of the API
- `GET /api/v1/users`: returns the list of users
- `GET /api/v1/users/:id`: returns an user based on the ID
- `DELETE /api/v1/users/:id`: deletes an user based on the ID
- `POST /api/v1/users`: creates a new user (JSON parameters: `email`, `password`, `last_name` (optional) and `first_name` (optional))
- `PUT /api/v1/users/:id`: updates an user based on the ID (JSON parameters: `last_name` and `first_name`)
