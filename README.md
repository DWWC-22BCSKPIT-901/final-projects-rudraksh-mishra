# MERN Expenses Tracker

## Project Overview

This is a comprehensive Expenses Tracking application built using the MERN (MongoDB, Express, React, Node.js) stack. The application provides a robust solution for personal expense management, allowing users to track, categorize, and analyze their financial transactions.

## Features

### User Management
- User registration and authentication
- Secure login and logout functionality
- User profile management

### Transaction Management
- Add, edit, and delete financial transactions
- Categorize transactions
- View transaction history

### Category Management
- Create custom expense categories
- Organize and classify transactions
- Manage category-based financial insights

## Technology Stack

### Backend
- **Node.js**: Runtime environment
- **Express.js**: Web application framework
- **MongoDB**: NoSQL database
- **Mongoose**: ODM (Object Document Mapper)

### Frontend
- **React**: JavaScript library for building user interfaces
- **Vite**: Next-generation frontend tooling
- **Tailwind CSS**: Utility-first CSS framework
- **Redux**: State management

### Authentication
- JWT (JSON Web Tokens) for secure authentication
- Middleware-based route protection

## Project Structure

```
Mern-Expenses-Project/
│
├── backend/
│   ├── controllers/     # Business logic
│   │   ├── categoryCtrl.js
│   │   ├── transactionCtrl.js
│   │   └── usersCtrl.js
│   │
│   ├── middlewares/     # Request interceptors
│   │   ├── errorHandlerMiddleware.js
│   │   └── isAuth.js
│   │
│   ├── models/          # Database schemas
│   │   ├── Category.js
│   │   ├── Transaction.js
│   │   └── User.js
│   │
│   └── routes/          # API endpoint definitions
│       ├── categoryRouter.js
│       ├── transactionRouter.js
│       └── userRouter.js
│
└── frontend/
    ├── src/
    │   ├── components/  # Reusable UI components
    │   ├── redux/       # State management
    │   ├── services/    # API interaction logic
    │   └── utils/       # Utility functions
    │
    └── Templates/       # Page and component templates
```

## Getting Started

### Prerequisites
- Node.js (v14 or later)
- MongoDB
- npm or yarn

### Installation

1. Clone the repository
   ```bash
   git clone https://github.com/yourusername/mern-expenses-tracker.git
   cd mern-expenses-tracker
   ```

2. Install Backend Dependencies
   ```bash
   cd backend
   npm install
   ```

3. Install Frontend Dependencies
   ```bash
   cd ../frontend
   npm install
   ```

4. Set Up Environment Variables
   - Create a `.env` file in the backend directory
   - Add necessary configurations:
     ```
     MONGO_URI=your_mongodb_connection_string
     JWT_SECRET=your_jwt_secret
     PORT=5000
     ```

### Running the Application

1. Start Backend Server
   ```bash
   cd backend
   npm start
   ```

2. Start Frontend Development Server
   ```bash
   cd frontend
   npm run dev
   ```

## API Endpoints

### Authentication
- `POST /api/users/register`: User registration
- `POST /api/users/login`: User login
- `GET /api/users/profile`: Get user profile

### Transactions
- `GET /api/transactions`: List all transactions
- `POST /api/transactions`: Create new transaction
- `PUT /api/transactions/:id`: Update transaction
- `DELETE /api/transactions/:id`: Delete transaction

### Categories
- `GET /api/categories`: List all categories
- `POST /api/categories`: Create new category
- `PUT /api/categories/:id`: Update category
- `DELETE /api/categories/:id`: Delete category

## Security Features
- Password hashing
- JWT-based authentication
- Protected routes
- Error handling middleware
- Input validation
