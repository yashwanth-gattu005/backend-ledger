# Backend Ledger

A backend ledger management system built using **Node.js, Express.js, and MongoDB**.

## Features

- User registration and login
- JWT authentication
- Password hashing with bcrypt
- Account management
- Transactions and ledger records
- Email integration
- Protected routes
- MongoDB database

## Tech Stack

- Node.js
- Express.js
- MongoDB
- Mongoose
- JWT
- bcrypt
- Nodemailer

## Project Structure

```text
backend-ledger/
├── src/
│   ├── config/
│   ├── controllers/
│   ├── middleware/
│   ├── models/
│   ├── routes/
│   └── services/
├── server.js
├── package.json
└── README.md
```

## Setup

### Clone the Repository

```bash
git clone https://github.com/yashwanth-gattu005/backend-ledger.git
cd backend-ledger
```

### Install Dependencies

```bash
npm install
```

### Environment Variables

Create a `.env` file in the root directory:

```env
PORT=5000
MONGODB_URI=your_mongodb_uri
JWT_SECRET=your_jwt_secret
```

Add the required email configuration for the email functionality.

### Run the Application

```bash
npm run dev
```

## Author

**Yashwanth Gattu**

GitHub: https://github.com/yashwanth-gattu005
