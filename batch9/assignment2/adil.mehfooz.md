Q1) Share screenshot of the above Branch Protection of `main` branch

link --> https://paste.pics/016c96e2bf95703f468b705e9a84cb72

Q2) Explain Docker Containers vs VMs

Containers:

-O/S based virtualization.
-Containers share the kernal of host O/S.
-Containers decouple Applications from O/S.

VMs:
-Hardware based virtualization.
-Each VM needs their on O/S to operate.




Q3) Explain Docker Architecture

Docker is a Container Runtime Interface (CRI). 
It consists of following components.
- Docker CLient: A CLI to communicate with Docker Daemon
- Docker host: Physical or Virtual system with its own O/S and  Docker CRI installed on it
- Docker Daemon: Main component of DOcker. It is responsible for communication with
                host, build and store images as well as create, run and monitor containers.
- Docker Image: Ordered collection of root file system changes
-Docker Registry: It stores and distributes Docker Images. It could be public or private
/////Docker Architecture/////
From CLient we request to pull, run on build an Image. Docker daemon checks for the image on private or public registry. pull the image and run it. 

Q4) Write command to create an nginx container in detached mode with name `assignment-2` running on host port `9090` and container port `80` on a custom network named `assignment-2`

Answer: docker container run --publish 9090:80--name assignment-2 nginx


Q5) Write command to see logs of the above container

Answer: docker logs assignment-2

Q6) Write commands to Exec into the container and cat the output of the default nginx file at /usr/share/nginx/html/index.html

>> docker container exec -it nginx-background /bin/bash
>> cat /usr/share/nginx/html/index.html
