What is difference between VM's and Container?
Container shares the host OS kernel, Every VM has its own OS and resources like Ram, Hard Disk. VMs are of few GBs and Containers are lightweight (KBs/MBs).  Ready-made VMs are difficult to find while Pre-built docker containers are easily available. VMs can move to new host easily while Containers are destroyed and re-created rather than moving. Creating VM takes a relatively longer time while Containers can be created in seconds.
What is Docker architecture?
Docker uses a client-server architecture. The Docker client talks to the Docker daemon, which does the heavy lifting of building, running, and distributing your Docker containers. The Docker client and daemon can run on the same system, or you can connect a Docker client to a remote Docker daemon.
Write command to create an nginx container in detached mode with name assignment-2 running on host port 9090 and container port 80?
$ sudo docker run --name assignment-2 -p 9090:80 -d nginx
Write the command to see the logs of the above container?
docker logs assignment-2
Write commands to Exec into the container?
docker exec -it assignment-2 sh
