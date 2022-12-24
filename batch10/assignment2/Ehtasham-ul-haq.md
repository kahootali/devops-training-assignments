1. VMs have the host OS and guest OS inside each VM. A guest OS can be any OS, like Linux or Windows, irrespective of the host OS. In contrast, Docker containers host on a single physical server with a host OS, which shares among them. Sharing the host OS between containers makes them light and increases the boot time.
2. Docker architecture. Docker uses a client-server architecture. The Docker client talks to the Docker daemon, which does the heavy lifting of building, running, and distributing your Docker containers. The Docker client and daemon can run on the same system, or you can connect a Docker client to a remote Docker daemon.
3. $ docker run --name assignment-2 -p 9090:80 -d nginx.
4. docker container logs assignment-2 CONTAINER.
5. docker exec -it assignment-2 bash
   cat /usr/share/nginx/html/index.html.
