# AI Exam Evaluation System

A modern web application for conducting and evaluating exams using AI-powered assessment. The system allows teachers to create exams and students to take them, with automatic evaluation using the Gemini API.

## Features

- Separate portals for students and teachers
- Secure authentication and authorization
- Exam creation with multiple question types (MCQ and Descriptive)
- AI-powered answer evaluation using Gemini API
- Real-time exam timer
- Detailed result analysis
- Filter and search functionality for results
- Responsive and modern UI using Material-UI

## Prerequisites

- Node.js (v14 or higher)
- MongoDB Atlas account
- Gemini API key
- npm or yarn package manager

## Setup

1. Clone the repository:
```bash
git clone <repository-url>
cd exam-evaluation-system
```

2. Install dependencies:
```bash
# Install backend dependencies
npm install

# Install frontend dependencies
cd client
npm install
cd ..
```

3. Configure environment variables:
- Copy the `.env.example` file to `.env`
- Update the following variables:
  - `MONGODB_URI`: Your MongoDB Atlas connection string
  - `JWT_SECRET`: A secure secret key for JWT tokens
  - `GEMINI_API_KEY`: Your Gemini API key

4. Start the development servers:
```bash
# Start backend server (from root directory)
npm run dev

# Start frontend server (from client directory)
cd client
npm start
```

## Usage

### For Teachers

1. Register as a teacher
2. Create new exams with:
   - Multiple choice questions
   - Descriptive questions with AI evaluation criteria
   - Time limits and passing marks
3. View results by:
   - Individual student
   - Section
   - Branch
4. Analyze performance metrics

### For Students

1. Register as a student
2. View available exams
3. Take exams with:
   - Real-time timer
   - Multiple choice and descriptive questions
4. View results with:
   - AI-generated feedback
   - Detailed performance analysis
   - Question-wise breakdown

## API Endpoints

### Authentication
- POST `/api/auth/register` - Register new user
- POST `/api/auth/login` - Login user
- GET `/api/auth/me` - Get current user

### Exams
- GET `/api/exams` - Get all exams
- GET `/api/exams/:id` - Get exam by ID
- POST `/api/exams` - Create new exam
- POST `/api/exams/:id/submit` - Submit exam answers

### Results
- GET `/api/results/student/:id` - Get student results
- GET `/api/results/section/:section` - Get results by section
- GET `/api/results/branch/:branch` - Get results by branch
- GET `/api/results/:id` - Get detailed result

## Technologies Used

- Frontend:
  - React
  - Material-UI
  - React Router
  - Axios

- Backend:
  - Node.js
  - Express
  - MongoDB with Mongoose
  - JWT Authentication
  - Gemini API

## Contributing

1. Fork the repository
2. Create your feature branch
3. Commit your changes
4. Push to the branch
5. Create a new Pull Request

## License

This project is licensed under the MIT License - see the LICENSE file for details. 