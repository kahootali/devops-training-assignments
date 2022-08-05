Q2) Explain Docker Containers vs VMS

Docker Containers is a virtualization technology in which the containers share the OS with the host. In contrast, the virtual machines have a separate OS for every virtual machine. This makes them quite
heavy compared to dockers. Dockers can be quite small as they only isolate a particular process without the OS.

Dockers are very portable within and across different OS. In contrast, the portability of Virtual Machines is lower as the whole virtual machine has to be transported.

Q3) Explain Docker Architecture

Docker uses a Docker is an open platform for developing, shipping, and running applications. Docker enables you to separate your applications from your infrastructure so you can deliver software quickly. 
With Docker, you can manage your infrastructure in the same ways you manage your applications. By taking advantage of Docker’s methodologies for shipping, testing, and deploying code quickly, you can 
significantly reduce the delay between writing code and running it in production.

Q4) Write command to create an nginx container in detached mode with name `assignment-2` running on host port `9090` and container port `80` on a custom network named `assignment-2`

>>> docker network create assignment-2
>>> docker container run -d --name assignment-2 --publish 9090:80 --network assignment-2 nginx 

Q5) Write command to see log of the above container

>>> docker logs assignment-2

Q6) Write commands to Exec into the container and cat the output of the default nginx file at /usr/share/nginx/html/index.html

>>> docker exec -it assigment-2 cat /usr/share/nginx/html/index.html
