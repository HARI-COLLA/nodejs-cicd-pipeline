# 🚀 Node.js CI/CD Pipeline using GitHub Actions & Docker

This project demonstrates a complete CI/CD pipeline setup for a simple Node.js application using GitHub Actions and DockerHub. The pipeline automatically builds the application, creates a Docker image, and pushes it to DockerHub on every code push to the `main` branch.

---

## 📦 Tech Stack

- **Node.js** — Backend JavaScript runtime
- **Express.js** — Lightweight web server framework
- **Docker** — Containerization platform
- **GitHub Actions** — CI/CD automation tool
- **DockerHub** — Container registry

---

## 📁 Project Structure
nodejs-cicd-pipeline/
├── .github/workflows/main.yml # GitHub Actions workflow
├── Dockerfile # Docker build file
├── index.js # Main server file
├── package.json # Project metadata and dependencies
└── package-lock.json # Exact dependency versions




---

## ⚙️ CI/CD Workflow

The GitHub Actions workflow is defined in `.github/workflows/main.yml` and performs the following steps automatically:

1. **Triggered on push to `main`**
2. **Checks out code**
3. **Sets up Node.js environment**
4. **Installs dependencies**
5. **Builds the Docker image**
6. **Logs in to DockerHub using GitHub Secrets**
7. **Pushes image to DockerHub**

---

## 🔐 GitHub Secrets Used

You must add the following **repository secrets** to enable DockerHub authentication:

| Name              | Description                          |
|-------------------|--------------------------------------|
| `DOCKER_USERNAME` | Your DockerHub username              |
| `DOCKER_PASSWORD` | DockerHub password or access token   |

---

## 🐳 Docker Image

The Docker image is automatically published to DockerHub.

> 🔗 **Image URL:**  
> [https://hub.docker.com/r/hari727/nodejs-cicd-pipeline](https://hub.docker.com/r/hari727/nodejs-cicd-pipeline)

---

## 🧪 Run Locally (Optional)

You can test the app locally using Docker:

```bash
docker pull hari727/nodejs-cicd-pipeline
docker run -p 3000:3000 hari727/nodejs-cicd-pipeline

