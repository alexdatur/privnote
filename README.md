<a name="readme-top"></a><div align="center">
   <img src="https://img.shields.io/github/contributors/alexdatur/privnote.svg?style=for-the-badge" />
   <img src="https://img.shields.io/github/forks/alexdatur/privnote.svg?style=for-the-badge" />
   <img src="https://img.shields.io/github/stars/alexdatur/privnote.svg?style=for-the-badge" />
   <img src="https://img.shields.io/github/issues/alexdatur/privnote.svg?style=for-the-badge" />
</div>

<br />

<div align="center">
  <a href="https://github.com/alexdatur/privnote">
    <img src="web/static/privnote-logo.svg" alt="Logo" width="200" height="80">
  </a>

  <h1 align="center">Privnote (Docker Edition)</h1>

  <p align="center">
    <a href="https://github.com/alexdatur/privnote">View Project</a>
    ·
    <a href="https://github.com/alexdatur/privnote/issues">Report Bug</a>
    ·
    <a href="https://github.com/alexdatur/privnote/issues">Request Feature</a>
    <br />
    A Docker-optimized fork of <a href="https://github.com/0-don/privnote">Privnote</a>, a secure, open-source, zero-JavaScript note-sharing service built with Rust and Svelte.
  </p>
</div>

<!-- TABLE OF CONTENTS -->
<details>
  <summary>Table of Contents</summary>
  <ol>
    <li><a href="#about-the-project">About The Project</a></li>
    <li><a href="#built-with">Built With</a></li>
    <li><a href="#getting-started">Getting Started</a>
      <ul>
        <li><a href="#prerequisites">Prerequisites</a></li>
        <li><a href="#installation">Installation</a></li>
        <li><a href="#nginx-reverse-proxy">Nginx Reverse Proxy</a></li>
      </ul>
    </li>
    <li><a href="#usage">Usage</a></li>
    <li><a href="#contributing">Contributing</a></li>
    <li><a href="#contact">Contact</a></li>
    <li><a href="#acknowledgments">Acknowledgments</a></li>
  </ol>
</details>

About The ProjectThis is a Docker-optimized fork of Privnote, a secure and lightweight note-sharing service inspired by PrivNote. It leverages Rust for a performant backend with Axum and Svelte for a zero-JavaScript frontend, ensuring speed and security. This fork simplifies deployment using Docker, making it ideal for containerized environments.Key Features:Secure Note Sharing: Notes are encrypted and self-destruct after being read.
Zero JavaScript: Svelte frontend emits no JavaScript for a fast, lightweight experience.
Docker-Optimized: Streamlined setup for containerized deployments.
High Performance: Powered by Axum and Rust for efficient backend operations.

<p align="right">(<a href="#readme-top">back to top</a>)</p>

Built WithRust - Reliable and efficient backend.
SvelteKit - High-performance, zero-JS frontend framework.
Axum - Performant web application framework.
SeaORM - Lightweight, async ORM for Rust.
PostgreSQL - Robust database system.
Tailwind CSS - Utility-first CSS framework.
TypeScript - Typed JavaScript for enhanced development.
Docker - Containerized deployment.

<p align="right">(<a href="#readme-top">back to top</a>)</p>

Getting StartedFollow these steps to set up and run the project in a Docker environment.PrerequisitesDocker - Ensure Docker is installed.
Docker Compose - For orchestrating containers.
Git - For cloning the repository.

InstallationClone the Repositorybash

