# Docker CLI Cheat Sheet

This cheat sheet covers the most commonly used Docker CLI commands and options.

---

## 🐳 Docker Basics

### Version & Info
```bash
docker --version              # Show Docker version
docker version                # Detailed version info
docker info                   # Display system-wide information
```

### Help
```bash
docker help                   # Help for Docker
docker <command> --help       # Help for a specific command
```

---

## 🏗️ Working with Images

### Pull & List Images
```bash
docker pull <image>[:tag]     # Pull image from Docker Hub
docker images                 # List local images
```

### Build & Tag
```bash
docker build -t <name>:<tag> .    # Build image from Dockerfile
docker tag <image> <repo>:<tag>  # Tag an image
```

### Remove Images
```bash
docker rmi <image>            # Remove an image
```

---

## 🧱 Working with Containers

### Run
```bash
docker run <image>                    # Run container
docker run -it <image>                # Interactive terminal
docker run -d <image>                 # Detached mode
docker run -p <host>:<container> <image>   # Port binding
docker run -v <host>:<container> <image>   # Volume mounting
```

### Start / Stop / Restart / Remove
```bash
docker start <container>       # Start container
docker stop <container>        # Stop container
docker restart <container>     # Restart container
docker rm <container>          # Remove container
docker rm -f <container>       # Force remove container
```

### List & Inspect
```bash
docker ps                      # List running containers
docker ps -a                   # List all containers
docker inspect <container>     # Detailed info (JSON)
docker logs <container>        # Container logs
```

### Execute in Running Container
```bash
docker exec -it <container> <command>   # Run command
```

---

## 📦 Volumes
```bash
docker volume create <name>          # Create a volume
docker volume ls                     # List volumes
docker volume inspect <name>         # Inspect volume
docker volume rm <name>              # Remove volume
```

---

## 🌐 Networks
```bash
docker network ls                    # List networks
docker network create <name>        # Create a network
docker network inspect <name>       # Inspect a network
docker network connect <net> <container>    # Connect container
```

---

## 🧰 Docker Compose
```bash
docker-compose up                    # Start services
docker-compose up -d                 # Detached mode
docker-compose down                  # Stop and remove services
docker-compose ps                    # List services
docker-compose logs                  # View logs
```

---

## 🔧 System Maintenance
```bash
docker system df                     # Show disk usage
docker system prune                  # Remove unused data
docker container prune               # Remove stopped containers
docker image prune                   # Remove unused images
```

---

## 🔒 Login & Push
```bash
docker login                         # Login to Docker Hub
docker push <repo>:<tag>            # Push image
docker logout                        # Logout from Docker Hub
```

---

## 🛠️ Useful Options
- `-e`: Set environment variable
- `--name`: Assign name to container
- `--rm`: Auto-remove container after exit
- `--network`: Specify network
- `--entrypoint`: Override default entrypoint

---

## 🐋 Dockerfile Instructions
```Dockerfile
# Base image
FROM node:18

# Maintainer info
LABEL maintainer="you@example.com"

# Set working directory
WORKDIR /app

# Copy files
COPY . .

# Install dependencies
RUN npm install

# Expose port
EXPOSE 3000

# Environment variable
ENV NODE_ENV=production

# Default command
CMD ["npm", "start"]
```

---

## 🧬 Multi-Stage Builds
```Dockerfile
# First stage: build
FROM node:18 AS builder
WORKDIR /app
COPY . .
RUN npm install && npm run build

# Second stage: production
FROM nginx:alpine
COPY --from=builder /app/dist /usr/share/nginx/html
```
- Reduces final image size by excluding build tools and dependencies

---

## 🧠 Docker Best Practices
- Use `.dockerignore` to exclude unnecessary files
- Keep images minimal (start from `alpine`, `slim`, etc.)
- Combine `RUN` commands to reduce layers
- Use multi-stage builds for production
- Tag images with version info (`v1.0`, `latest`, etc.)
- Clean up after install (`apt-get clean`, `rm -rf /var/lib/apt/lists/*`)
- Scan images for vulnerabilities (`docker scan <image>`)

---

## 🔁 CI/CD Integration Tips
- **Use Docker in CI/CD pipelines** to build, test, and deploy applications consistently.
- **Sample GitHub Actions step** to build and push Docker image:
  ```yaml
  - name: Build Docker image
    run: docker build -t myapp:${{ github.sha }} .
  
  - name: Push to Docker Hub
    run: |
      echo "${{ secrets.DOCKER_PASSWORD }}" | docker login -u "${{ secrets.DOCKER_USERNAME }}" --password-stdin
      docker tag myapp:${{ github.sha }} mydockerhubuser/myapp:latest
      docker push mydockerhubuser/myapp:latest
  ```
- **Use GitLab CI/CD** with a `.gitlab-ci.yml`:
  ```yaml
  build:
    stage: build
    script:
      - docker build -t registry.gitlab.com/mygroup/myapp:latest .
      - docker push registry.gitlab.com/mygroup/myapp:latest
  ```
- **Cache dependencies** between builds to speed up pipelines.
- **Use `docker-compose`** for multi-container apps in CI.
- **Use private registries or GitHub Container Registry (GHCR)** for internal projects.

---

## 📚 References
- [Docker CLI Docs](https://docs.docker.com/engine/reference/commandline/docker/)
- [Docker Compose Docs](https://docs.docker.com/compose/)
- [Dockerfile Reference](https://docs.docker.com/engine/reference/builder/)
- [Best Practices](https://docs.docker.com/develop/dev-best-practices/)
- [GitHub Actions for Docker](https://docs.github.com/en/actions/publishing-packages/publishing-docker-images)
- [GitLab Docker Registry](https://docs.gitlab.com/ee/user/packages/container_registry/)
