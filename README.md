# SmartChat AI

SmartChat AI is a full stack AI-powered chat application built using FastAPI, React, PostgreSQL, and Ollama. The system enables real time interaction with locally hosted large language models while ensuring secure authentication and persistent chat storage.

---

## Overview

This application provides a scalable platform for conversational AI by combining a high performance backend with a modern frontend interface. It allows users to register, log in, and communicate with AI models while maintaining conversation history for future reference.

---

## Features

- User authentication with secure login and registration  
- Real time chat powered by local AI models  
- Persistent storage of chat history using PostgreSQL  
- Support for multiple Ollama models  
- Responsive and modern user interface  
- RESTful API design using FastAPI  

---

## Technology Stack

### Frontend
- React with Vite  
- Tailwind CSS  

### Backend
- FastAPI  
- Uvicorn  

### Database
- PostgreSQL  

### AI Integration
- Ollama  

---

## Project Structure

Chatbot/
├── backend
├── frontend
├── database_setup.sql
├── setup.sh
└── README.md

---

## Prerequisites

- Python 3.8 or higher  
- Node.js 16 or higher  
- PostgreSQL installed and running  
- Ollama installed and running  

---

## Setup Instructions

### Step 1: Start Ollama

ollama serve  
ollama pull gemma3:4b  

---

### Step 2: Setup Database

psql -U postgres -c "CREATE DATABASE chatbot;"  
psql -U postgres -d chatbot -f database_setup.sql  

---

### Step 3: Backend Setup

cd backend  
python -m venv venv  
source venv/bin/activate  
pip install -r requirements.txt  
cp .env.example .env  

### Run Backend

cd backend  
python -m uvicorn main:app --reload  

---

### Step 4: Frontend Setup

cd frontend  
npm install  

### Run Frontend

cd frontend  
npm run dev  

---

## Application Access

Open the application in a browser

---

## Default Credentials

- Username: admin  
- Password: admin123  

---

## API Endpoints

### Authentication
- POST /auth/register  
- POST /auth/login  
- GET /auth/me  

### Chat
- POST /chat  
- GET /chat/history  
- GET /models  

### System
- GET /health  

---

## Future Enhancements

- File upload support in chat  
- Voice-based interaction  
- Admin dashboard for user management  
- Deployment to cloud platforms  


