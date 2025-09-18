# AI Academy - Comprehensive Documentation

This document provides a detailed overview of the AI Academy platform, including its architecture, features, deployment, and development guidelines.

## 1. Introduction

AI Academy is an internal education platform designed to build AI literacy across all teams in your organization. It provides a modern, engaging learning experience with specialized tracks for leadership, product, development, and compliance.

### 1.1. Purpose

- **Educate**: Provide comprehensive AI education to all organization employees.
- **Empower**: Equip teams with the knowledge and skills to leverage AI effectively.
- **Standardize**: Ensure a consistent understanding of AI principles and best practices.
- **Innovate**: Foster a culture of AI-driven innovation.

### 1.2. Key Features

- **Modern Learning Experience**: Engaging UI with interactive content and progress tracking.
- **Specialized Learning Tracks**: Tailored content for different roles and expertise levels.
- **Comprehensive Course Library**: 6 courses covering AI strategy, product management, development, and compliance.
- **Analytics Dashboard**: Real-time insights into user engagement, course performance, and learning value.
- **Dynamic Content Management**: Admin interface for real-time content updates without rebuilds.
- **Dockerized Deployment**: Easy setup for local development and production environments.
- **Professional Design**: Modern branding, responsive layout, and professional UI components.

## 2. Architecture

The AI Academy platform is built with a modern full-stack architecture:

- **Frontend**: React, Vite, Tailwind CSS, Recharts
- **Backend**: Flask, Python, SQLAlchemy
- **Database**: SQLite (default), PostgreSQL (optional)
- **Deployment**: Docker, Docker Compose, Nginx

### 2.1. System Components

- **React Frontend**: User interface, authentication, analytics dashboard.
- **Flask Backend**: RESTful API for course content, analytics, and admin functionality.
- **Nginx Reverse Proxy**: Handles SSL, rate limiting, and serves static assets in production.
- **Docker Compose**: Orchestrates the multi-container application.

### 2.2. Data Flow

1. **User Interaction**: User interacts with the React frontend.
2. **API Calls**: Frontend makes API calls to the Flask backend.
3. **Data Processing**: Backend processes requests, interacts with the database, and returns data.
4. **UI Updates**: Frontend updates the UI with the received data.

## 3. Deployment

The platform is designed for easy deployment with Docker.

### 3.1. Prerequisites

- [Docker](https://docs.docker.com/get-docker/)
- [Docker Compose](https://docs.docker.com/compose/install/)

### 3.2. Quick Start

1. **Clone the Repository**

   ```bash
   git clone https://github.com/your-username/ai-academy.git
   cd ai-academy
   ```

2. **Configure Environment**

   ```bash
   cp .env.example .env
   ```

3. **Run the Application**

   - **Development**: `./scripts/deploy.sh dev`
   - **Production**: `./scripts/deploy.sh prod`
   - **Full Production (with Nginx)**: `./scripts/deploy.sh full`

### 3.3. Deployment Script

The `scripts/deploy.sh` script provides a convenient way to manage the application lifecycle.

| Command | Description |
|---|---|
| `dev` | Deploy in development mode (hot reload) |
| `prod` | Deploy in production mode (optimized builds) |
| `full` | Deploy with Nginx reverse proxy (full production) |
| `stop` | Stop all services |
| `logs [service]` | Show logs for all or specific services |
| `status` | Show service status and health checks |
| `help` | Show help message |

## 4. Development

### 4.1. Frontend Development

- **Framework**: React, Vite
- **Styling**: Tailwind CSS
- **Charts**: Recharts
- **Dependencies**: `frontend/package.json`

**To start the frontend development server:**

```bash
cd frontend
npm install
npm run dev
```

### 4.2. Backend Development

- **Framework**: Flask, Python
- **Database ORM**: SQLAlchemy
- **Dependencies**: `backend/requirements.txt`

**To start the backend development server:**

```bash
cd backend
pip install -r requirements.txt
python app.py
```

## 5. Content Management

The platform features a dynamic content management system.

### 5.1. Admin Interface

- **URL**: [http://localhost:5000/admin.html](http://localhost:5000/admin.html)
- **Functionality**: Edit course content, lessons, and metadata in real-time.

### 5.2. Content Structure

- **Format**: JSON
- **Location**: `backend/src/content`
- **Structure**: Each course has a JSON file with its content, lessons, and modules.

## 6. API Reference

The backend provides a RESTful API for data access.

| Endpoint | Method | Description |
|---|---|---|
| `/api/courses` | GET | Get all courses |
| `/api/courses/{id}` | GET | Get a specific course |
| `/api/analytics/overview` | GET | Get analytics overview data |
| `/api/analytics/course-performance` | GET | Get course performance data |
| `/api/analytics/user-engagement` | GET | Get user engagement data |
| `/health` | GET | Health check endpoint |

## 7. Contributing

Contributions are welcome! Please follow the standard GitHub flow:

1. Fork the repository
2. Create a new branch
3. Make your changes
4. Commit your changes
5. Push to the branch
6. Create a new Pull Request

## 8. License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.

