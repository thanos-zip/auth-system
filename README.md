# Auth System

> A complete authentication system with register, login, JWT tokens and password hashing.

## What You Will Learn
- How authentication actually works under the hood
- How to hash passwords securely with bcrypt
- How to create and verify JWT tokens
- How to protect routes with middleware

## Tech Stack
- Node.js
- Express
- PostgreSQL
- bcrypt
- JSON Web Tokens (JWT)
- Railway (deployment)

## Getting Started

### Prerequisites
- Node.js 18+ installed
- PostgreSQL installed locally or a free Railway database
- A free Railway account

### Installation
```bash
git clone https://github.com/thanos.zip/auth-system
cd auth-system
npm install
cp .env.example .env
# Fill in your database URL and JWT secret in .env
npm run dev
```

## Project Structure
```
auth-system/
├── src/
│   ├── index.js                  # Server entry point
│   ├── routes/
│   │   └── auth.js               # Register and login routes here
│   ├── controllers/
│   │   └── authController.js     # Business logic here
│   ├── middleware/
│   │   └── verifyToken.js        # JWT verification middleware here
│   ├── models/
│   │   └── user.js               # Database queries here
│   └── db/
│       └── index.js              # Database connection here
├── .env.example
├── package.json
└── README.md
```

## What To Build
- Create a users table in PostgreSQL with id, email, password, created_at
- POST /register — validate input, hash password, save user, return JWT
- POST /login — find user, compare password hash, return JWT
- GET /profile — protected route, verify JWT middleware, return user data
- Handle errors properly — duplicate email, wrong password, expired token
- Deploy on Railway

## Stretch Goals
- Add refresh tokens so users stay logged in longer
- Add email verification on register
- Add OAuth — let users sign in with Google

## Resources
- https://jwt.io/introduction
- https://www.npmjs.com/package/bcrypt
- https://railway.app/docs

---
Built for [@thanos.zip](https://instagram.com/thanos.zip) followers.
