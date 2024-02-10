Here is a list of some commonly used Docker commands along with examples:

1. **Image Commands:**
   - **Pull an Image:**
     ```bash
     docker pull <image-name>:<tag>
     ```
     Example:
     ```bash
     docker pull ubuntu:20.04
     ```

   - **List Downloaded Images:**
     ```bash
     docker images
     ```

   - **Remove an Image:**
     ```bash
     docker rmi <image-name>:<tag>
     ```
     Example:
     ```bash
     docker rmi ubuntu:20.04
     ```

2. **Container Commands:**
   - **Run a Container:**
     ```bash
     docker run <options> <image-name>:<tag>
     ```
     Example:
     ```bash
     docker run -it ubuntu:20.04 /bin/bash
     ```

   - **List Running Containers:**
     ```bash
     docker ps
     ```

   - **List All Containers (including stopped ones):**
     ```bash
     docker ps -a
     ```

   - **Stop a Running Container:**
     ```bash
     docker stop <container-id or container-name>
     ```

   - **Remove a Container:**
     ```bash
     docker rm <container-id or container-name>
     ```

   - **Execute a Command in a Running Container:**
     ```bash
     docker exec -it <container-id or container-name> <command>
     ```
     Example:
     ```bash
     docker exec -it my-container /bin/bash
     ```

3. **Container Logs:**
   - **View Logs of a Container:**
     ```bash
     docker logs <container-id or container-name>
     ```

4. **Docker Compose Commands:**
   - **Run Services Defined in a Docker Compose File:**
     ```bash
     docker-compose up
     ```

   - **Stop Services Defined in a Docker Compose File:**
     ```bash
     docker-compose down
     ```

5. **Docker Network Commands:**
   - **List Docker Networks:**
     ```bash
     docker network ls
     ```

   - **Inspect a Docker Network:**
     ```bash
     docker network inspect <network-id or network-name>
     ```

6. **Docker Volume Commands:**
   - **List Docker Volumes:**
     ```bash
     docker volume ls
     ```

   - **Inspect a Docker Volume:**
     ```bash
     docker volume inspect <volume-id or volume-name>
     ```

7. **System Commands:**
   - **Show System-wide Information:**
     ```bash
     docker info
     ```

   - **Display Docker Disk Usage:**
     ```bash
     docker system df
     ```

These are just a few examples, and Docker has many more commands and options. You can explore additional commands and options using `docker --help` or refer to the official Docker documentation: [Docker Command-Line Interface (CLI)](https://docs.docker.com/engine/reference/commandline/cli/).
