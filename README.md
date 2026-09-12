Backend Ledger

A backend ledger management system built using Node.js, Express.js, and MongoDB.

Features

- User registration and login
- JWT authentication
- Password hashing with bcrypt
- Account management
- Transactions and ledger records
- Email integration
- Protected routes
- MongoDB database

Tech Stack

- Node.js
- Express.js
- MongoDB
- Mongoose
- JWT
- bcrypt
- Nodemailer

Project Structure

backend-ledger/
├── config/
├── controllers/
├── middleware/
├── models/
├── routes/
├── services/
├── server.js
└── package.json

Setup

git clone https://github.com/yashwanth-gattu005/backend-ledger.git
cd backend-ledger
npm install

Create a ".env" file with the required environment variables and start the server:

npm run dev

Environment Variables

PORT=5000
MONGODB_URI=your_mongodb_uri
JWT_SECRET=your_jwt_secret

Add the required email configuration if using the email functionality.

Author

Yashwanth Gattu

"GitHub" (https://github.com/yashwanth-gattu005)
