Backend Ledger

A backend ledger management system built with Node.js, Express.js, and MongoDB. The project provides secure user authentication, account management, financial transactions, and ledger-based transaction records through REST APIs.

Features

- User registration and authentication
- JWT-based authorization
- Secure password handling
- Account creation and management
- Deposit and withdrawal operations
- Account-to-account transfers
- Transaction history
- Ledger-based transaction records
- MongoDB database integration
- Email integration for application notifications
- Input validation and error handling
- Modular backend architecture

Tech Stack

- Runtime: Node.js
- Framework: Express.js
- Database: MongoDB
- ODM: Mongoose
- Authentication: JSON Web Tokens (JWT)
- Password Security: bcrypt
- Email: Nodemailer
- API: REST

Architecture

The application follows a layered backend structure to keep business logic, database operations, and HTTP handling separated.

Client
  │
  ▼
Express Routes
  │
  ▼
Controllers
  │
  ▼
Services / Business Logic
  │
  ▼
Mongoose Models
  │
  ▼
MongoDB

Authentication is handled through JWTs, while protected routes verify the user's identity before allowing account or transaction operations.

Core Transaction Flow

A typical transfer follows this flow:

Client
  │
  ▼
Authenticate User
  │
  ▼
Validate Request
  │
  ▼
Validate Source & Destination Accounts
  │
  ▼
Check Transaction Conditions
  │
  ▼
Update Account / Ledger Records
  │
  ▼
Return Transaction Result

The ledger provides a persistent record of financial activity, allowing transactions to be tracked independently of the current account state.

API Overview

Authentication

Method| Endpoint| Description
POST| "/api/auth/register"| Register a new user
POST| "/api/auth/login"| Authenticate a user

Accounts

Method| Endpoint| Description
POST| "/api/accounts"| Create an account
GET| "/api/accounts"| Get user accounts
GET| "/api/accounts/:id"| Get account details

Transactions

Method| Endpoint| Description
POST| "/api/transactions/deposit"| Deposit funds
POST| "/api/transactions/withdraw"| Withdraw funds
POST| "/api/transactions/transfer"| Transfer funds
GET| "/api/transactions"| Get transaction history

«Note: Update the endpoints above to match the actual routes implemented in the project.»

Authentication

Protected endpoints require a valid JWT.

Authorization: Bearer <JWT_TOKEN>

The server validates the token before allowing access to protected resources.

Database

MongoDB is used for persistent storage.

The main entities include:

User
 └── Accounts
       └── Transactions
             └── Ledger Entries

Mongoose is used to define schemas, validate data, and interact with MongoDB.

Example Request

Transfer

POST /api/transactions/transfer
Authorization: Bearer <JWT_TOKEN>
Content-Type: application/json

{
  "fromAccount": "SOURCE_ACCOUNT_ID",
  "toAccount": "DESTINATION_ACCOUNT_ID",
  "amount": 1000
}

Example response:

{
  "success": true,
  "message": "Transfer completed successfully"
}

«Update the request and response examples to match the actual API implementation.»

Project Structure

backend-ledger/
├── src/
│   ├── controllers/
│   ├── models/
│   ├── routes/
│   ├── services/
│   ├── middleware/
│   ├── utils/
│   └── app.js
│
├── .env.example
├── package.json
└── README.md

The exact structure may vary depending on the current implementation.

Getting Started

Prerequisites

Make sure you have installed:

- Node.js
- npm
- MongoDB

Installation

Clone the repository:

git clone https://github.com/yashwanth-gattu005/backend-ledger.git

Navigate into the project:

cd backend-ledger

Install dependencies:

npm install

Create an environment file:

cp .env.example .env

Configure the required environment variables.

Start the development server:

npm run dev

The API will then be available on the configured server port.

Environment Variables

Example:

PORT=5000
MONGODB_URI=your_mongodb_connection_string
JWT_SECRET=your_jwt_secret
EMAIL_USER=your_email
EMAIL_PASSWORD=your_email_password

Never commit real credentials, API keys, or secrets to the repository.

Error Handling

The API returns appropriate HTTP status codes and structured error responses for cases such as:

- Invalid authentication
- Missing or invalid input
- Unauthorized access
- Invalid account
- Insufficient balance
- Duplicate or invalid transactions
- Server/database errors

Future Improvements

- Automated unit and integration tests
- API documentation with Swagger/OpenAPI
- Rate limiting
- Request logging
- Redis-based caching
- Improved transaction concurrency handling
- Docker support
- CI/CD pipeline
- Production monitoring and observability

Learning Outcomes

This project helped me work with:

- REST API development
- Authentication and authorization
- MongoDB data modeling
- Mongoose
- Backend architecture
- Financial transaction workflows
- Error handling
- Secure handling of credentials
- API design and integration

Author

Yashwanth Gattu

GitHub: "yashwanth-gattu005" (https://github.com/yashwanth-gattu005)
