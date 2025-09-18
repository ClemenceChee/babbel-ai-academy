# B____ AI Academy - Internal AI Education Platform

![B____ AI Academy Banner](https://i.imgur.com/your-banner-image.png)

**B____ AI Academy** is a comprehensive internal education platform designed to build AI literacy across all teams at B____. It provides a modern, engaging learning experience with specialized tracks for leadership, product, development, and compliance.

This repository contains the complete source code and Docker deployment configuration for the B____ AI Academy platform, making it easy for anyone to run, develop, and deploy the application.

---

## ✨ Key Features

- **Modern Learning Experience**: Engaging UI with interactive content and progress tracking.
- **Specialized Learning Tracks**: Tailored content for different roles and expertise levels.
- **Comprehensive Course Library**: 6 courses covering AI strategy, product management, development, and compliance.
- **Analytics Dashboard**: Real-time insights into user engagement, course performance, and learning value.
- **Dynamic Content Management**: Admin interface for real-time content updates without rebuilds.
- **Dockerized Deployment**: Easy setup for local development and production environments.
- **Professional Design**: B____ branding, responsive layout, and modern UI components.

## 🚀 Quick Start

Get the B____ AI Academy platform up and running in minutes with Docker.

### Prerequisites

- [Docker](https://docs.docker.com/get-docker/)
- [Docker Compose](https://docs.docker.com/compose/install/)

### 1. Clone the Repository

```bash
git clone https://github.com/your-username/babbel-ai-academy.git
cd babbel-ai-academy
```

### 2. Configure Environment

Copy the example environment file and customize it for your setup:

```bash
cp .env.example .env
```

### 3. Run the Application

Use the deployment script to start the application in your desired mode:

**Development Mode (with hot reload):**

```bash
./scripts/deploy.sh dev
```

**Production Mode:**

```bash
./scripts/deploy.sh prod
```

**Full Production with Nginx:**

```bash
./scripts/deploy.sh full
```

### 4. Access the Application

- **Frontend**: [http://localhost:3000](http://localhost:3000)
- **Backend API**: [http://localhost:5000](http://localhost:5000)
- **Admin Panel**: [http://localhost:5000/admin.html](http://localhost:5000/admin.html)

**Demo Credentials:**
- **Email**: `demo@company.com`
- **Password**: `demo123`

## 🔧 Deployment Script

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

## 🏗️ Architecture

The B____ AI Academy platform is built with a modern full-stack architecture:

- **Frontend**: React, Vite, Tailwind CSS, Recharts
- **Backend**: Flask, Python, SQLAlchemy
- **Database**: SQLite (default), PostgreSQL (optional)
- **Deployment**: Docker, Docker Compose, Nginx

### System Components

- **React Frontend**: User interface, authentication, analytics dashboard.
- **Flask Backend**: RESTful API for course content, analytics, and admin functionality.
- **Nginx Reverse Proxy**: Handles SSL, rate limiting, and serves static assets in production.
- **Docker Compose**: Orchestrates the multi-container application.

## 📚 Course Library

The platform includes 6 comprehensive courses:

1. **AI Strategy for Leadership**
2. **GDPR Compliance for AI Systems**
3. **AI Product Management**
4. **Machine Learning for Developers**
5. **Safe AI Usage Guidelines**
6. **MLOps and Production AI**

## 🎨 Design & Branding

The platform features a professional design with B____ branding:

- **Color Scheme**: B____ orange for the frontend, blue for the admin backend.
- **Typography**: Inter font for a clean, modern look.
- **UI Components**: Cards, charts, navigation, forms, and interactive elements.
- **Responsive Design**: Optimized for all screen sizes.

## 🤝 Contributing

Contributions are welcome! Please follow the standard GitHub flow:

1. Fork the repository
2. Create a new branch (`git checkout -b feature/your-feature`)
3. Make your changes
4. Commit your changes (`git commit -m "Add your feature"`)
5. Push to the branch (`git push origin feature/your-feature`)
6. Create a new Pull Request

## 📄 License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.

---

*This project was created with the help of Manus AI.*
