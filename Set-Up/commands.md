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


Here is a list of basic Docker commands related to networks and volumes:

### Docker Network Commands:

1. **List Networks:**
   ```bash
   docker network ls
   ```

2. **Inspect a Network:**
   ```bash
   docker network inspect <network-name>
   ```

3. **Create a Network:**
   ```bash
   docker network create <network-name>
   ```

4. **Remove a Network:**
   ```bash
   docker network rm <network-name>
   ```

### Docker Volume Commands:

1. **List Volumes:**
   ```bash
   docker volume ls
   ```

2. **Inspect a Volume:**
   ```bash
   docker volume inspect <volume-name>
   ```

3. **Create a Volume:**
   ```bash
   docker volume create <volume-name>
   ```

4. **Remove a Volume:**
   ```bash
   docker volume rm <volume-name>
   ```

### Docker Container Commands with Networks and Volumes:

1. **Run a Container with a Specific Network:**
   ```bash
   docker run --network <network-name> <image>
   ```

2. **Run a Container with a Specific Volume:**
   ```bash
   docker run -v <volume-name>:<container-path> <image>
   ```

3. **Run a Container with Multiple Volumes:**
   ```bash
   docker run -v <volume1-name>:<container-path1> -v <volume2-name>:<container-path2> <image>
   ```

4. **Run a Container with a Named Volume:**
   ```bash
   docker run -v <volume-name>:/path/in/container <image>
   ```

5. **Run a Container with a Specific IP Address (on a user-defined bridge network):**
   ```bash
   docker run --network <network-name> --ip <ip-address> <image>
   ```

6. **Run a Container and Mount a Host Directory as a Volume:**
   ```bash
   docker run -v /host/path:/container/path <image>
   ```

7. **Run a Container with Read-Only Volumes:**
   ```bash
   docker run -v <volume-name>:/path/in/container:ro <image>
   ```

These are some basic Docker commands for working with networks and volumes. For more detailed information and options, refer to the official Docker documentation:

- [Docker Network Documentation](https://docs.docker.com/network/)
- [Docker Volume Documentation](https://docs.docker.com/storage/volumes/)
