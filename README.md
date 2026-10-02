# GenQuery - AI Powered Assistant

> An AI-powered student assistant that enables users to upload documents and ask questions to get relevant, context-aware responses using Retrieval-Augmented Generation (RAG).

## 📌 About the Project

**GenQuery** is a full-stack AI-powered student assistant designed to make document-based information retrieval easier and more interactive.

The application allows students to create an account, manage their profile, upload documents, and interact with an AI assistant through a conversational interface.

GenQuery uses a **Retrieval-Augmented Generation (RAG)** pipeline to process uploaded documents, retrieve relevant information, and generate responses based on the available context.

## ✨ Features

* 🔐 User Registration and Login
* 🔑 JWT Authentication
* 👤 Student Profile Management
* 📄 Document Upload
* 🧠 AI-Powered Question Answering
* 🔎 Retrieval-Augmented Generation (RAG)
* 💬 Conversational AI Interface
* 🗂️ Conversation and Message Management
* 📚 Document-Based Information Retrieval
* 📱 Responsive Web Interface

## 🏗️ How GenQuery Works

```text
                    Student
                       |
                       v
                Angular + Ionic
                   Frontend
                       |
                       v
                Django REST API
                       |
             +---------+---------+
             |                   |
             v                   v
       User & Profile      Document Upload
                                 |
                                 v
                       Document Processing
                                 |
                                 v
                           RAG Pipeline
                                 |
                    +------------+------------+
                    |            |            |
                    v            v            v
               Extraction    Chunking    Embeddings
                                             |
                                             v
                                       Vector Store
                                             |
                                             v
                                    Relevant Context
                                             |
                                             v
                                      AI Generation
                                             |
                                             v
                                       AI Response
                                             |
                                             v
                                          Student
```

## 🧠 RAG Pipeline

The core AI functionality is based on **Retrieval-Augmented Generation**.

The document processing flow consists of:

1. **Document Upload**
   Students upload documents through the application.

2. **Document Extraction**
   The backend extracts usable text from the uploaded content.

3. **Text Chunking**
   The extracted content is divided into smaller sections for efficient retrieval.

4. **Embedding Generation**
   Text chunks are converted into numerical representations for semantic search.

5. **Vector Storage**
   The generated embeddings are stored for efficient retrieval.

6. **Relevant Context Retrieval**
   When a question is asked, relevant information is retrieved from the processed documents.

7. **AI Response Generation**
   The retrieved context is provided to the AI model to generate a relevant response.

## 🛠️ Technology Stack

### Frontend

* Angular
* Ionic
* TypeScript
* HTML
* SCSS

### Backend

* Python
* Django
* Django REST Framework

### Database

* MySQL

### AI

* Google Gemini API
* Retrieval-Augmented Generation (RAG)
* Text Embeddings
* Vector Store
* Document Processing

## 📂 Project Structure

```text
GenQuery/
│
├── studentbeapi/
│   ├── manage.py
│   ├── requirements.txt
│   │
│   ├── studentapi/
│   │   ├── settings.py
│   │   ├── urls.py
│   │   ├── asgi.py
│   │   └── wsgi.py
│   │
│   └── studentapp/
│       ├── models.py
│       ├── serializers.py
│       ├── views.py
│       ├── urls.py
│       ├── migrations/
│       └── rag/
│           ├── chunker.py
│           ├── conversation_pipeline.py
│           ├── embeddings.py
│           ├── extractor.py
│           ├── generator.py
│           ├── ingestion.py
│           ├── rag_pipeline.py
│           ├── schemas.py
│           ├── structured_retriever.py
│           └── vector_store.py
│
└── studentfe/
    └── studentfe/
        ├── src/
        │   ├── app/
        │   │   ├── pages/
        │   │   │   ├── login/
        │   │   │   ├── signup/
        │   │   │   ├── dashboard/
        │   │   │   └── upload-documents/
        │   │   └── services/
        │   ├── assets/
        │   ├── environments/
        │   └── theme/
        │
        ├── package.json
        ├── package-lock.json
        ├── angular.json
        └── ionic.config.json
```

## 🔐 Authentication

GenQuery uses authentication to protect student-specific application data.

The authentication flow includes:

* User registration
* User login
* JWT token-based authentication
* Authenticated API requests
* Student profile access

## 💬 Conversation Management

GenQuery provides a conversational interface for interacting with the AI assistant.

The backend maintains conversation-related information, including:

* Conversations
* Messages
* Student association
* AI-generated responses

This allows users to interact with the assistant through a structured chat experience.

## 🗄️ Database

**MySQL** is used as the primary relational database.

The application stores data related to:

* Users
* Students
* Documents
* Conversations
* Messages

## ⚙️ Installation and Setup

### Prerequisites

Make sure the following are installed:

* Python
* Node.js and npm
* Ionic CLI
* MySQL

### Backend Setup

Navigate to the backend:

```bash
cd studentbeapi
```

Create a Python virtual environment:

```bash
python -m venv env
```

Activate it on Windows PowerShell:

```powershell
.\env\Scripts\Activate.ps1
```

Install Python dependencies:

```bash
pip install -r requirements.txt
```

Apply database migrations:

```bash
python manage.py migrate
```

Start the Django server:

```bash
python manage.py runserver
```

Backend runs at:

```text
http://127.0.0.1:8000/
```

### Frontend Setup

Navigate to the frontend:

```bash
cd studentfe/studentfe
```

Install dependencies:

```bash
npm install
```

Start the Ionic application:

```bash
ionic serve
```

## 🔑 Environment Variables

Sensitive credentials should not be committed to GitHub.

Create a local `.env` file in the backend and configure the required environment variables.

Example:

```env
SECRET_KEY=your-django-secret-key
GEMINI_API_KEY=your-gemini-api-key
```

Configure the MySQL database according to your local environment.

> **Never upload API keys, passwords, or other sensitive credentials to the repository.**

## 📁 Repository Guidelines

The repository intentionally excludes generated or sensitive files such as:

```text
.env
env/
node_modules/
__pycache__/
media/
db.sqlite3
chroma_db/
```

These files are environment-specific, generated during development, or may contain sensitive/personal data.

## 🎯 Project Goals

GenQuery aims to demonstrate how modern full-stack technologies can be combined with AI and RAG to create a practical student-focused application.

The project brings together:

* Full-stack application development
* REST API development
* Database management
* Authentication
* Document processing
* Semantic information retrieval
* Retrieval-Augmented Generation
* AI-powered conversational interaction

## 🚀 Future Enhancements

Possible future improvements include:

* Support for additional document formats
* Improved document management
* Enhanced retrieval accuracy
* More advanced conversation features
* Additional AI model integrations
* Production deployment
* Improved user interface and experience

## 📌 Project Status

**GenQuery - AI Powered Assistant** is an academic full-stack AI project developed for learning, experimentation, and demonstration of AI-integrated web application development.

## 📄 License

This project is developed for educational and academic purposes.
