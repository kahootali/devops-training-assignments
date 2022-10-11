Q1 Share screenshot of the above Branch Protection of `main` branch
Answer: Upoaded screenshot on dice LMS.
Q2 Explain Docker Containers vs VMs
Answer: Containers and virtual machines are very similar resource virtualization technologies. Virtualization is the process in which a system singular resource like RAM, CPU, Disk, or Networking can be ‘virtualized’ and represented as multiple resources. The key differentiator between containers and virtual machines is that virtual machines virtualize an entire machine down to the hardware layers and containers only virtualize software layers above the operating system level.
Q3 Explain Docker Architecture
Answer Docker uses a client-server architecture. The Docker client talks to the Docker daemon, which does the heavy lifting of building, running, and distributing your Docker containers. The Docker client and daemon can run on the same system, or you can connect a Docker client to a remote Docker daemon.
Q4 Write command to create an nginx container in detached mode with name `assignment-2` running on host port `9090` and container port `80` on a custom network named `assignment-2`
Answer docker run -d -p 9090:80 --name assignment-2 --net assigment-2 ngnix
Q5 Write command to see logs of the above container
Answer docker logs assignment-2
Q6 Write commands to Exec into the container and cat the output of the default nginx file at /usr/share/nginx/html/index.html
Answer docker --exec assigment-2 cat /usr/share/nginx/html/index.html
