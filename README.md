Privnote Docker

https://img.shields.io/badge/Docker-Ready-2496ED?style=for-the-badge&logo=docker
https://img.shields.io/badge/Compose-Ready-2496ED?style=for-the-badge&logo=docker

A streamlined Docker deployment of Privnote - self-destructing encrypted notes service. Optimized for stability and production use.
🚀 Quick Deployment
bash

git clone https://github.com/alexdatur/privnote
cd privnote
docker-compose up -d

Access the application at: http://localhost:3000
📋 Services Overview

This deployment consists of three interconnected containers:

    Frontend (privnote-web): React-based web interface (port 3000)

    Backend (privnote-server): Node.js API server (port 4000)

    Database (privnote-db): PostgreSQL database

⚙️ Configuration

Edit environment variables in docker-compose.yml:
yaml

environment:
  - DATABASE_URL=postgres://user:pass@privnote-db:5432/privnote
  - SMTP_USER=yourmail@gmail.com
  - SMTP_PASS=yourpassword
  # Add other configuration as needed

🐳 Docker Commands
bash

# Start services
docker-compose up -d

# View logs
docker-compose logs

# Stop services
docker-compose down

# Rebuild containers
docker-compose up -d --build

🔧 Customization

The project structure allows easy customization:
text

web/          # Frontend application
server/       # Backend API
docker-compose.yml  # Multi-container configuration

📝 Notes

    Ensure proper SMTP configuration for email notifications

    Default database credentials can be changed for security

    The external network 'privnote' will be created automatically

Based on the original Privnote concept with Docker optimizations and stability improvements.

Note: This is a production-ready Docker implementation of Privnote with separated frontend and backend services.
