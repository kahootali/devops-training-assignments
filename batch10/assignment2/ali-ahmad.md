# Explain Docker Containers vs VMs.
The key differentiator between containers and virtual machines is that virtual machines virtualize an entire machine down to the hardware layers and containers only virtualize software layers above the operating system level.
# Explain Docker Architecture
Docker uses a client-server architecture. The Docker client talks to the Docker daemon, which does the heavy lifting of building, running, and distributing your Docker containers. The Docker client and daemon can run on the same system, or you can connect a Docker client to a remote Docker daemon.
# Write command to create an nginx container in detached mode with name assignment-2 running on host port 9090 and container port 80 on a custom network named assignment-2
docker container run -d --publish 9090:80 image-name