# Assignment 2

Q1) Share screenshot of the above Branch Protection of `main` branch

Ans: ![scrrenShot](https://user-images.githubusercontent.com/7136590/180639854-cc7016dc-a811-48cf-b56d-cc025038247d.png)


Q2) Explain Docker Containers vs VMs

Ans: Docker containers are considered suitable to run multiple applications over a single OS kernel; whereas, virtual machines are needed if the applications or services required to run on different OS

Q3) Explain Docker Architecture

Ans:  Docker uses a client-server architecture. The Docker client talks to the Docker daemon, which does the heavy lifting of building, running, and distributing your Docker containers. The Docker client and daemon can run on the same system, or you can connect a Docker client to a remote Docker daemon.

Q4) Write command to create an nginx container in detached mode with name `assignment-2` running on host port `9090` and container port `80` on a custom network named `assignment-2`

Ans:sudo docker run --assignment-2 docker-nginx -p 9090 -d nginx

Q5) Write command to see logs of the above container

Ans: docker logs assignment-2

Q6) Write commands to Exec into the container and cat the output of the default nginx file at /usr/share/nginx/html/index.html

Ans: docker exec assignment-2 cat /usr/share/nginx/html/index.html
