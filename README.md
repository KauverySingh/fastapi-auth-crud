# FastAPI Auth CRUD API

A beginner-friendly backend project built with FastAPI, PostgreSQL, SQLAlchemy, and JWT Authentication.

This project demonstrates:

- User registration
- User login
- JWT authentication
- Protected routes
- CRUD operations
- PostgreSQL database integration
- Swagger API docs
- Deployment on Render

---

## Live Demo

API Base URL:

https://fastapi-auth-crud-ffkh.onrender.com/

Swagger Docs:

https://fastapi-auth-crud-ffkh.onrender.com/docs

---

## Tech Stack

- FastAPI
- Python
- PostgreSQL
- SQLAlchemy
- JWT Authentication
- Passlib + bcrypt
- Uvicorn
- Render Deployment
- Git + GitHub

---

## Features

### Authentication
- Register new user
- Login user
- Generate JWT token
- Password hashing using bcrypt

### CRUD Operations
- Create user
- Get all users
- Get user by ID
- Update user
- Delete user

### API Docs
- Swagger UI
- OpenAPI schema

---

## Project Structure

```bash
FastAPIProject/
│
├── main.py
├── database.py
├── models.py
├── schemas.py
├── crud.py
├── auth.py
├── requirements.txt
├── Dockerfile
└── README.md
```

---

## Installation

### Clone repository

```bash
git clone https://github.com/KauverySingh/fastapi-auth-crud.git
cd fastapi-auth-crud
```

### Create virtual environment

```bash
python -m venv venv
```

Activate environment:

Windows:

```bash
venv\Scripts\activate
```

Mac/Linux:

```bash
source venv/bin/activate
```

---

## Install dependencies

```bash
pip install -r requirements.txt
```

---

## Setup PostgreSQL

Create database:

```sql
CREATE DATABASE fastapi_db;
```

Update database URL inside `database.py`

```python
DATABASE_URL = "postgresql://username:password@localhost/fastapi_db"
```

For Render deployment:

```python
DATABASE_URL = os.getenv("DATABASE_URL")
```

---

## Run locally

```bash
uvicorn main:app --reload
```

App runs at:

```bash
http://127.0.0.1:8000
```

Swagger docs:

```bash
http://127.0.0.1:8000/docs
```

---

## API Endpoints

### Home

```http
GET /
```

---

### Register

```http
POST /register
```

Request body:

```json
{
  "email": "test@gmail.com",
  "password": "123456"
}
```

---

### Login

```http
POST /login
```

Form data:

```text
username = test@gmail.com
password = 123456
```

Returns JWT token.

---

### Protected Route

```http
GET /users/me
```

Requires Bearer Token.

---

### CRUD

```http
GET /users
GET /users/{id}
PUT /users/{id}
DELETE /users/{id}
```

---

## Deployment

Deployed on Render.

### Steps followed:
- Push code to GitHub
- Connect repo to Render
- Add PostgreSQL database
- Add environment variable:

```text
DATABASE_URL
```

Start command:

```bash
uvicorn main:app --host 0.0.0.0 --port $PORT
```

---

## Future Improvements

- Docker support
- Redis caching
- Role-based authentication
- Email verification
- Password reset
- AI endpoints integration
- Kubernetes deployment

---

## Learning Outcomes

This project helped practice:

- FastAPI fundamentals
- REST API development
- Authentication flow
- JWT tokens
- Database integration
- Cloud deployment
- Backend project structure

---

## Author

Kauvery Singh

GitHub:
https://github.com/KauverySingh

---

## License

This project is open source and available under the MIT License.
