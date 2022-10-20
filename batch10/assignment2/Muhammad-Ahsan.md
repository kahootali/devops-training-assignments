Q1) Share screenshot of the above Br

Require a pull request before merging set to check and require approval 1



Q2) Explain Docker Containers vs VMs

Docker Container:

Docker container is basically a running process. It takes less time to load. It utilize less resources. Container is virtualization of  OS Kernal. Less Secure.

VM on the other hand are Virtual machines. Takes time while loading completely isolated. Takes more resources. VM is virtualization of System Resources has its own operating system. More secure.





Q3) Explain Docker Architecture

Docker Basically Consist of 3 things

1) Docker Client CLI through which you can run containers and start and stop.

2) Docker Host in which Deamon that manages containers and images.

3) Docker Registy from which you can pull and push images.


Q4) Write command to create an nginx container in detached mode with name assignment-2 running on host port 9090 and container port 80 on a custom network named assignment-2

docker container run -d publish 9090:80 --name assignment-2 nginx


Q5) Write command to see logs of the above container

docker logs assignment-2


Q6) Write commands to Exec into the container and cat the output of the default nginx file at /usr/share/nginx/html/index.html

docker exec assignment-2 cat /usr/share/nginx/html/index/html
