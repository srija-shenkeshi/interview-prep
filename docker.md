# 1. Create:
Build Image:
Developers create a Docker image using a Dockerfile or pull it from a registry.
Run Container:
Developers run a new container from the Docker image using the docker run command.
# 2. Start:
Start Container:
The container starts, and the process defined in the Docker image begins to execute.
# 3. Run:
Container Running:
The container is now running and executing the defined process.
# 4. Pause (Optional):
Pause Container (Optional):
Developers can pause the execution of a running container using the docker pause command.
# 5. Stop:
Stop Container:
Developers stop a running container using the docker stop command.
Graceful Shutdown:
Docker sends a SIGTERM signal to the main process inside the container, allowing it to shut down gracefully.
# 6. Restart (Optional):
Restart Container (Optional):
Developers can restart a stopped container using the docker start command.
# 7. Unpause (Optional):
Unpause Container (Optional):
Developers can unpause a paused container using the docker unpause command.
# 8. Destroy:
Remove Container:
Developers remove a stopped container using the docker rm command.
Cleanup Resources:
Docker cleans up any resources associated with the container, such as network connections and storage.
# 9. Delete Image (Optional):
Remove Image (Optional):
Developers remove a Docker image using the docker rmi command.
Additional Docker Lifecycle Operations:
Inspect Container:
Developers can inspect the details of a container using the docker inspect command.
View Logs:
Developers can view the logs of a container using the docker logs command.
Attach to Container:
Developers can attach to a running container's process using the docker attach command.
Execute Command in Container:
Developers can execute a command in a running container using the docker exec command.
Example Commands:
bash
Copy code
# Create and run a container from an image
docker run [OPTIONS] IMAGE [COMMAND] [ARG...]

# Pause a running container
docker pause CONTAINER

# Unpause a paused container
docker unpause CONTAINER

# Stop a running container
docker stop CONTAINER

# Restart a stopped container
docker start CONTAINER

# Remove a stopped container
docker rm CONTAINER

# Remove a Docker image
docker rmi IMAGE

# Inspect details of a container
docker inspect CONTAINER

# View logs of a container
docker logs CONTAINER

# Attach to a running container
docker attach CONTAINER

# Execute a command in a running container
docker exec [OPTIONS] CONTAINER COMMAND [ARG...]
