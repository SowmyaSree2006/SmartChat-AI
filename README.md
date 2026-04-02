# SmartChat-AI
A full stack AI chat application built with FastAPI, React, PostgreSQL, and Ollama. It enables real time conversations with local language models, supports user authentication, and stores chat history for a seamless user experience.
AI Chat Application

This project is a full stack AI powered chat application built using FastAPI for the backend, React with Vite for the frontend, PostgreSQL for data storage, and Ollama for integrating local large language models. The application allows users to register, log in, and interact with AI models while maintaining persistent chat history.

Features

User authentication with secure login and registration
Real time chat functionality using AI models
Persistent storage of chat history in PostgreSQL
Support for multiple Ollama models
Responsive user interface built with React and Tailwind CSS
RESTful API using FastAPI

Technology Stack

Frontend
React with Vite
Tailwind CSS

Backend
FastAPI
Uvicorn

Database
PostgreSQL

AI Integration
Ollama

Project Structure

Chatbot
backend contains FastAPI application
frontend contains React application
database_setup.sql contains database schema
setup.sh is used for automated setup

Prerequisites

Python version 3.8 or above
Node.js version 16 or above
PostgreSQL installed and running
Ollama installed and running

Setup Instructions

Step 1 Start Ollama

ollama serve
ollama pull gemma3:4b

Step 2 Setup Database

psql -U postgres -c "CREATE DATABASE chatbot;"
psql -U postgres -d chatbot -f database_setup.sql

Step 3 Backend Setup

cd backend
python -m venv venv
source venv/bin/activate
pip install -r requirements.txt
cp .env.example .env

Run Backend

cd backend
python -m uvicorn main:app --reload

Step 4 Frontend Setup

cd frontend
npm install

Run Frontend

cd frontend
npm run dev

Access the Application

http://localhost:5173

Default Login Credentials

Username admin
Password admin123

API Endpoints

Authentication
POST /auth/register
POST /auth/login
GET /auth/me

Chat
POST /chat
GET /chat/history
GET /models

System
GET /health

Environment Variables

OLLAMA_BASE_URL=http://localhost:11434
MODEL_NAME=gemma3:4b
DATABASE_URL=postgresql://postgres:password@localhost:5432/chatbot
SECRET_KEY=your_secret_key

Troubleshooting

If the backend is not starting ensure port 8000 is available
If the frontend is not loading ensure the development server is running
If models are not visible ensure Ollama is running and a model is downloaded
If database connection fails ensure PostgreSQL is running properly

Future Improvements

Add file upload functionality in chat
Implement voice based interaction
Develop an admin dashboard
Deploy the application to cloud platforms
