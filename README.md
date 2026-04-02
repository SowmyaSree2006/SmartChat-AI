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
```
Chatbot
├── backend
├── frontend
├── database_setup.sql
├── setup.sh
└── README.md
```
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
```bash
cd backend  
```
```bash
python -m venv venv  
```
```bash
source venv/bin/activate  
```
```bash
pip install -r requirements.txt  
```


### Run Backend

```bash
cd backend  
```
```bash
python -m uvicorn main:app --reload  
```

---

### Step 4: Frontend Setup

```bash
cd backend  
```
```bash
npm install
```

### Run Frontend

```bash
cd backend  
```
```bash
npm run dev 
```

---

## Application Access

Open the application in a browser

---

## Default Credentials

- Username: admin  
- Password: admin123  

---


## Future Enhancements

- File upload support in chat  
- Voice-based interaction  
- Admin dashboard for user management  
- Deployment to cloud platforms  
