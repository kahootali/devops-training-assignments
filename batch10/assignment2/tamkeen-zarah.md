# Q1) Share screenshot of the above Branch Protection of main branch

![Branch Protection of main branch](https://user-images.githubusercontent.com/62700476/194774394-a514f13d-35b8-42e2-90a0-0504059f3fad.png)


# Q2) Explain Docker Containers vs VMs

## Docker Containers

- OS level virtualisation
- light weight
- Fast
- Simply isolated processes 
- Memory efficient

## VMs

- Hardware level virtualisation
- Shared apps
- Dedicated memory

# Q3) Explain Docker Architecture

- Docker is a tool used for containerization
## Client
● A CLI fro interaction with Daemon

## Daemon
● Main component running and communicating with OS
● Build and store Images
● It can create,ship and run containers

## Registry
● Sharing of images
● DockerHub, private registries

# Q4) Write command to create an nginx container in detached mode with name assignment-2 running on host port 9090 and container port 80 on a custom network named assignment-2

sudo docker network create network1

sudo docker container run --net 9090:80 assignment-2 

sudo docker container run -d --publish 9090:80 --name assignment-2 nginx

# Q5) Write command to see logs of the above container

sudo docker logs assignment-2

sudo docker ps

# Q6) Write commands to Exec into the container and cat the output of the default nginx file at /usr/share/nginx/html/index.html

step-1 sudo docker container exec -it assignment-2 /bin/bash 
step-2  cat /usr/share/nginx/html/index.html

