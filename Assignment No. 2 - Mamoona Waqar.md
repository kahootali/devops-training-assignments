
**Q1) Share screenshot of the above Branch Protection of `main` branch**
![Screenshot of branch protection rules](https://github.com/mamoonawaqar/devops-training-assignments/blob/68b34347d61bccc346c6f4bbf6d94c79efdc7b41/Branch%20protection%20rule.png)

**Q2) Explain Docker Containers vs VMs**

VM shares physical resources such as hardware. It provides hardware level virtualization. VM takes up more memory in 10s of GBs. It has its own Operating System, applications, binaries, libraries. One machine can host multiple VMs. VMs are isolated but apps are not. They can be slow to boot and have static computation power and static memory. VMs resources usage is high.
Container shares host OS kernel. It provides OS level virtualization. Container takes less memory up to 10s of MBs. It shares host machine hardware and kernel but can have its own OS. Containers are isolated and so are applications. Can be allocated memory and computation power as required thus providing low resource usage.   

**Q3) Explain Docker Architecture**

There are three main components of docker architecture. These are docker client, docker daemon, and registry. Docker client are simple CLI’s to interact with docker daemon. Docket daemon is the main component which create, run and monitor containers, communicate with OS and, build and store images. Third component is registry which stores images and distributes them. 


**Q4) Write command to create an nginx container in detached mode with name `assignment-2` running on host port `9090` and container port `80` on a custom network named `assignment-2`**

sudo docker network create assignment-2

sudo docker container run -d -p 9090:80 --net assignment-2 --name assignment-2 nginx


**Q5) Write command to see logs of the above container**

sudo docker container logs assignment-2

**Q6) Write commands to Exec into the container and cat the output of the default nginx file at /usr/share/nginx/html/index.html**

sudo docker container run -d -p 8080:80 --name nginx-back 

sudo docker container exec -it nginx-back /bin/bash

cat /etc/nginx/nginx.conf>>/usr/share/nginx/html/index.html


