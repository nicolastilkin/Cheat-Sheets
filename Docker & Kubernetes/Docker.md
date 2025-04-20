# 🐳 Docker

## 📦 Images & Containers

| Action                      | Command                                                      |
| --------------------------- | ------------------------------------------------------------ |
| Pull an image               | `docker pull <image>:<tag>`                                  |
| List images                 | `docker images`                                              |
| Remove an image             | `docker rmi <image_id>`                                      |
| Build image from Dockerfile | `docker build -t <name>:<tag> .`                             |
| Run container               | `docker run -d -p <host_port>:<container_port> --name <name> <image>` |
| Run interactively           | `docker run -it <image> /bin/bash`                           |
| List running containers     | `docker ps`                                                  |
| List all containers         | `docker ps -a`                                               |
| Stop a container            | `docker stop <container_id>`                                 |
| Start a container           | `docker start <container_id>`                                |
| Remove a container          | `docker rm <container_id>`                                   |
| View container logs         | `docker logs <container_id>`                                 |
| Execute inside container    | `docker exec -it <container_id> /bin/bash`                   |

---

## 🛠️ Docker Compose

| Action                 | Command                     |
| ---------------------- | --------------------------- |
| Start services         | `docker-compose up`         |
| Start in detached mode | `docker-compose up -d`      |
| Stop services          | `docker-compose down`       |
| Rebuild services       | `docker-compose up --build` |
| List services          | `docker-compose ps`         |

---

## 🧠 Volumes & Networks

| Action          | Command                         |
| --------------- | ------------------------------- |
| Create volume   | `docker volume create <name>`   |
| List volumes    | `docker volume ls`              |
| Remove volume   | `docker volume rm <name>`       |
| Create network  | `docker network create <name>`  |
| List networks   | `docker network ls`             |
| Inspect network | `docker network inspect <name>` |

---

## 📂 Useful Flags

| Flag            | Description                            |
| --------------- | -------------------------------------- |
| `-d`            | Detached mode (runs in background)     |
| `-p`            | Port mapping (`host:container`)        |
| `--name`        | Assign a name to the container         |
| `-v`            | Bind mount a volume (`host:container`) |
| `--rm`          | Automatically remove container on exit |
| `--env` or `-e` | Set environment variable               |

---

## 🔍 Inspecting & Debugging

| Action                       | Command                       |
| ---------------------------- | ----------------------------- |
| Inspect container/image      | `docker inspect <name_or_id>` |
| Show container stats         | `docker stats`                |
| Top processes in container   | `docker top <container_id>`   |
| Diff changes in container FS | `docker diff <container_id>`  |

---

## 
