<div align="center">
  <img src="https://img.shields.io/github/stars/alexdatur/privnote.svg?style=for-the-badge&logo=github&color=black" alt="Stars" />
  <img src="https://img.shields.io/github/forks/alexdatur/privnote.svg?style=for-the-badge&logo=github&color=black" alt="Forks" />
  <img src="https://img.shields.io/github/issues/alexdatur/privnote.svg?style=for-the-badge&logo=github&color=black" alt="Issues" />
  <img src="https://img.shields.io/github/contributors/alexdatur/privnote.svg?style=for-the-badge&logo=github&color=black" alt="Contributors" />
</div>

<br />

<div align="center">
  <a href="https://github.com/alexdatur/privnote">
    <img src="web/static/privnote-logo.svg" alt="Logo" width="220" height="88">
  </a>

  <h1 align="center">Privnote-docker</h1>

  <p align="center">
    A fast, secure, and open-source service for sharing self-destructing notes.
    <br />
    <i>This is an optimized and enhanced fork of the original project.</i>
    <br />
    <br />
    <a href="https://github.com/alexdatur/privnote/issues/new?assignees=&labels=bug&template=bug_report.md&title=">Report a Bug</a>
    ·
    <a href="https://github.com/alexdatur/privnote/issues/new?assignees=&labels=enhancement&template=feature_request.md&title=">Request a Feature</a>
  </p>
</div>

---

### About The Project

**Privnote** is a secure, open-source note-sharing service inspired by PrivNote. Create a note, share the link, and it will self-destruct after being read.

This fork enhances the original project by providing a streamlined Docker setup, optimizations, and various fixes to ensure a smooth and reliable self-hosting experience. The backend is built with Rust (Axum) for maximum performance, while the SvelteKit frontend is configured to emit **zero JavaScript**, making it incredibly lightweight and fast.

### ✨ Key Features

* **🔒 Secure & Private**: Notes are encrypted and self-destruct after the first view.
* **🚀 Blazing Fast**: Built with Rust and a zero-JS frontend for instant loading times.
* **📦 Easy to Self-Host**: Get up and running in minutes with Docker Compose.
* **💎 Minimalist**: A clean, focused interface for creating and sharing notes.
* **🌐 Open Source**: Free to use, modify, and contribute to.

---

### 🛠️ Tech Stack

This project is built with a modern and efficient technology stack:

<p align="center">
  <img src="https://img.shields.io/badge/rust-%23000000.svg?style=for-the-badge&logo=rust&logoColor=white" alt="Rust" />
  <img src="https://img.shields.io/badge/svelte-%23FF3E00.svg?style=for-the-badge&logo=svelte&logoColor=white" alt="Svelte" />
  <img src="https://img.shields.io/badge/Docker-2496ED?style=for-the-badge&logo=docker&logoColor=white" alt="Docker" />
  <img src="https://img.shields.io/badge/PostgreSQL-316192?style=for-the-badge&logo=postgresql&logoColor=white" alt="PostgreSQL" />
  <img src="https://img.shields.io/badge/tailwindcss-%2338B2AC.svg?style=for-the-badge&logo=tailwind-css&logoColor=white" alt="TailwindCSS" />
  <img src="https://img.shields.io/badge/typescript-%23007ACC.svg?style=for-the-badge&logo=typescript&logoColor=white" alt="TypeScript" />
</p>

---

### 🚀 Getting Started

Deploying your own instance of Privnote is incredibly simple with Docker.

#### Prerequisites

* [Docker](https://www.docker.com/get-started)
* [Docker Compose](https://docs.docker.com/compose/install/)

#### Installation with Docker (Recommended)

1.  **Clone the repository:**
    ```sh
    git clone [https://github.com/alexdatur/privnote.git](https://github.com/alexdatur/privnote.git)
    cd privnote
    ```

2.  **Configure your environment:**
    Copy the example environment file and customize the variables inside, especially the `DATABASE_URL` and `SECRET_KEY`.
    ```sh
    cp env.example .env
    ```

3.  **Launch the application:**
    ```sh
    docker-compose up -d
    ```

Your Privnote instance is now running! By default, it will be accessible at `http://localhost:8787`.

<br>

<details>
  <summary><b>Manual Installation (for Development)</b></summary>
  
  #### Prerequisites
  - [Rust](https://www.rust-lang.org/tools/install)
  - [Node.js](https://nodejs.org/) (v18 or higher)
  
  #### Backend (Server)
  1. Navigate to the server directory:
     ```sh
     cd server
     ```
  2. Run the server:
     ```sh
     cargo run
     ```

  #### Frontend (Web)
  1. In a new terminal, navigate to the web directory:
     ```sh
     cd web
     ```
  2. Install dependencies:
     ```sh
     npm install
     ```
  3. Start the development server:
     ```sh
     npm run dev
     ```
</details>

---

### 🤝 Contributing

Contributions are welcome and greatly appreciated! If you have an idea for an improvement, please feel free to fork the repository and create a pull request.

1.  **Fork** the Project
2.  Create your Feature Branch (`git checkout -b feature/AmazingFeature`)
3.  Commit your Changes (`git commit -m 'Add some AmazingFeature'`)
4.  Push to the Branch (`git push origin feature/AmazingFeature`)
5.  Open a **Pull Request**

Don't forget to give the project a star if you find it useful!

### 🙏 Acknowledgments

* A big thanks to the original creator ([0-don](https://github.com/0-don)) for the initial project.
* All the frameworks and libraries that made this project possible.

---
<p align="center">
  <a href="https://github.com/alexdatur/privnote">https://github.com/alexdatur/privnote</a>
</p>
