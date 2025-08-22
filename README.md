<a name="readme-top"></a>

<div align="center">
   <img src="https://img.shields.io/github/contributors/alexdatur/privnote.svg?style=for-the-badge" />
   <img src="https://img.shields.io/github/forks/alexdatur/privnote.svg?style=for-the-badge" />
   <img src="https://img.shields.io/github/stars/alexdatur/privnote.svg?style=for-the-badge" />
   <img src="https://img.shields.io/github/issues/alexdatur/privnote.svg?style=for-the-badge" />
   <img src="https://img.shields.io/badge/Docker-Ready-blue?style=for-the-badge&logo=docker" />
</div>

<!-- PROJECT LOGO -->
<br />
<div align="center">
  <a href="https://github.com/alexdatur/privnote">
    <img src="web/static/privnote-logo.svg" alt="Logo" width="200" height="80">
  </a>

  <h1 align="center">Privnote (Dockerized)</h1>

  <p align="center">
    A secure, open source and zero javascript note sharing service inspired by PrivNote
    <br />
    <strong>Forked from <a href="https://github.com/0-don/privnote">0-don/privnote</a> with Docker support</strong>
    <br />
    <a href="https://github.com/alexdatur/privnote/issues">Report Bug</a>
    ·
    <a href="https://github.com/alexdatur/privnote/issues">Request Feature</a>
  </p>
</div>

<!-- TABLE OF CONTENTS -->
<details>
  <summary>Table of Contents</summary>
  <ol>
    <li>
      <a href="#about-the-project">About The Project</a>
      <ul>
        <li><a href="#built-with">Built With</a></li>
      </ul>
    </li>
    <li>
      <a href="#getting-started">Getting Started</a>
      <ul>
        <li><a href="#prerequisites">Prerequisites</a></li>
        <li><a href="#installation">Installation</a></li>
        <li><a href="#docker-deployment">Docker Deployment</a></li>
      </ul>
    </li>
    <li><a href="#nginx-configuration">Nginx Configuration</a></li>
    <li><a href="#usage">Usage</a></li>
    <li><a href="#roadmap">Roadmap</a></li>
    <li><a href="#contributing">Contributing</a></li>
    <li><a href="#license">License</a></li>
    <li><a href="#contact">Contact</a></li>
    <li><a href="#acknowledgments">Acknowledgments</a></li>
  </ol>
</details>

<!-- ABOUT THE PROJECT -->

## About The Project

[Privnote](https://github.com/alexdatur/privnote) is a secure, open-source note sharing service inspired by PrivNote. This project is unique because it's built with Svelte but emits zero JavaScript, ensuring a lightweight and fast user experience. The backend is powered by Axum, a highly performant web application framework.

This fork enhances the original project by adding Docker support for easy deployment.

Here's why you should consider using or contributing to Privnote:

- It's secure: Your notes are safe and can be shared confidently.
- It's efficient: With zero JavaScript emission from Svelte and a performant backend in Axum, Privnote is built for speed.
- It's open-source: This means you can contribute to its development, suggest changes, and help improve it.
- It's Docker-ready: Easy to deploy in any environment with Docker.

Privnote is not just another note sharing service. It's designed to be secure, efficient, and user-friendly.

### Built With

The major frameworks/libraries used to bootstrap this project include:

- [Rust](https://www.rust-lang.org/): A language empowering everyone to build reliable and efficient software.
- [SvelteKit](https://kit.svelte.dev/): A framework for building extremely high-performance web apps.
- [SeaORM](https://www.sea-orm.org/): An async, dynamic and lightweight ORM for Rust.
- [Axum](https://github.com/tokio-rs/axum): A web application framework that ensures high performance.
- [Svelte](https://svelte.dev/): A JavaScript framework for building user interfaces. In this project, it's configured to emit zero JavaScript.
- [PostgreSQL](https://www.postgresql.org/): A powerful, open source object-relational database system.
- [Tailwind CSS](https://tailwindcss.com/): A utility-first CSS framework for rapidly building custom designs.
- [TypeScript](https://www.typescriptlang.org/): A typed superset of JavaScript that compiles to plain JavaScript.
- [Docker](https://www.docker.com/): For containerization and easy deployment.

<p align="right">(<a href="#readme-top">back to top</a>)</p>

<!-- GETTING STARTED -->

## Getting Started

To get a local copy of Privnote up and running, follow these steps:

### Prerequisites

- You need to have Rust installed. If you don't have it, you can install it from [here](https://www.rust-lang.org/tools/install).
- You need Node.js and npm installed. If you don't have them, you can install Node.js from [here](https://nodejs.org/en/download/) which includes npm.

### Installation

1. Clone the repo
   ```sh
   git clone https://github.com/alexdatur/privnote.git

    Change directory to the cloned repo
    sh

cd privnote

Open a new terminal and start the server
sh

cd server && cargo run

Open a new terminal and start the Web App
sh

    yarn
    yarn dev

Docker Deployment

This project is Dockerized for easy deployment. Ensure you have Docker and Docker Compose installed.

    Clone the repository
    sh

git clone https://github.com/alexdatur/privnote.git
cd privnote

Build and run using Docker Compose
sh

    docker-compose up -d

    The application will be available at http://localhost:3000 by default.

For production deployment, ensure to set the necessary environment variables in docker-compose.yml or using an environment file.
<p align="right">(<a href="#readme-top">back to top</a>)</p>
Nginx Configuration

For production deployment, it's recommended to use Nginx as a reverse proxy. Below is a sample configuration:
nginx

server {
    listen 443 ssl http2;
    server_name yourdomain.xyz;

    ssl_certificate /yourpath/fullchain.pem;
    ssl_certificate_key /yourpath/privkey.pem;
    
    add_header X-Frame-Options "SAMEORIGIN" always;
    add_header X-Robots-Tag noindex;
    add_header X-Content-Type-Options "nosniff" always;
    add_header Strict-Transport-Security "max-age=31536000; includeSubDomains" always;
    

    location / {
        proxy_set_header Upgrade $http_upgrade;
        proxy_set_header Connection "Upgrade";
        proxy_set_header Host $host;
        proxy_set_header X-Real-IP $remote_addr;
        proxy_set_header X-Forwarded-For $proxy_add_x_forwarded_for;
        proxy_set_header X-Forwarded-Proto $scheme;
        proxy_pass http://localhost:3000/;
    }
}

Replace yourdomain.xyz with your domain and adjust the paths to your SSL certificates.
<p align="right">(<a href="#readme-top">back to top</a>)</p><!-- USAGE EXAMPLES -->
Usage

Privnote is a secure, open-source note sharing service. You can use it to share notes securely with others. Simply write your note, generate a link, and share it. The note will self-destruct after being read.
Roadmap

See the open issues for a list of proposed features and known issues.
Contributing

Contributions are what make the open-source community such an amazing place to learn, inspire, and create. Any contributions you make are greatly appreciated.

    Fork the Project

    Create your Feature Branch (git checkout -b feature/AmazingFeature)

    Commit your Changes (git commit -m 'Add some AmazingFeature')

    Push to the Branch (git push origin feature/AmazingFeature)

    Open a Pull Request

License

Distributed under the MIT License. See LICENSE for more information.
Contact

Project Link: https://github.com/alexdatur/privnote
Acknowledgments

    Svelte

    Axum

    SeaORM

    Rust

    Docker

    PostgreSQL

    SvelteKit

    Tailwind CSS

    TypeScript

    ESLint

    Prettier

<p align="right">(<a href="#readme-top">back to top</a>)</p> ```
