# 🚀 MEAN Stack DevOps Automation
A complete CI/CD pipeline for a MEAN (MongoDB, Express, Angular, Node.js) application, demonstrating automated cloud deployment on AWS/Azure using Docker, GitHub Actions, and Nginx.

## 🏗️ Architecture
The application is architected using a microservices-style approach, with each component isolated in its own Docker container:



* **Frontend:** Angular application served on Port 4200.
* **Backend:** Node.js API handling business logic on Port 3000.
* **Database:** MongoDB for persistent data storage.
* **Reverse Proxy:** Nginx installed on the VM host to route traffic from Port 80 to the internal containers.

---

## 🛠️ CI/CD Pipeline Logic
The deployment is fully automated via GitHub Actions. You can view the status of the "robot" in the **Actions** tab.

* **Build & Push:** On every push to `main`, GitHub Actions builds Docker images for both the frontend and backend.
* **Registry:** Images are tagged and pushed to **Docker Hub**.
* **Automated Deploy:** The runner SSHes into the Cloud VM, pulls the latest images, and restarts the containers using `docker-compose`.

---

## 🚀 Setup & Installation

### Local Development
1. Clone the repository:
   ```bash
   git clone [https://github.com/gaureshconnects/Discover-Dollar-DevOps.git](https://github.com/gaureshconnects/Discover-Dollar-DevOps.git)
