Q1) Share screenshot of the above Branch Protection of `main` branch
--------------------------------------------------------------------
![image](https://user-images.githubusercontent.com/95872967/195485904-17672566-06eb-4e69-9fbf-86e4b9c4d695.png)




Q2) Explain Docker Containers vs VMs
--------------------------------------
The key differentiator between containers and virtual machines is that virtual machines virtualize an entire machine down to the hardware layers and containers only virtualize software layers above the operating system level

Containers are lightweight software packages that contain all the dependencies required to execute the contained software application whereas Virtual machines are heavy software packages that provide complete emulation of low level hardware devices like CPU, Disk and Networking devices.




Q3) Explain Docker Architecture
---------------------------------
Docker uses a client-server architecture. The Docker client talks to the Docker daemon, which does the heavy lifting of building, running, and distributing your Docker containers. The Docker client and daemon can run on the same system, or you can connect a Docker client to a remote Docker daemon. 

The Docker client and daemon communicate using a REST API, over UNIX sockets or a network interface. Another Docker client is Docker Compose, that lets you work with applications consisting of a set of containers.




Q4) Write command to create an nginx container in detached mode with name `assignment-2` running on host port `9090` and container port `80` on a custom network named `assignment-2`
----------------------------------------------------------------------------------------------------

docker run --name assignment-2 -p 9090:80 -d nginx 

docker network create assignment-2 // Creates a custom network named assignment-2


![image](https://user-images.githubusercontent.com/95872967/195509686-ae508e20-3a08-4bcd-9856-b824edd2b713.png)




Q5) Write command to see logs of the above container
------------------------------------------------------
docker logs assignment-2                                    

![image](https://user-images.githubusercontent.com/95872967/195509584-0420e6a2-fb33-4516-8a20-ed56c5e1c15b.png)




Q6) Write commands to Exec into the container and cat the output of the default nginx file at /usr/share/nginx/html/index.html
-----------------------------------------------------------------------------------------------------
docker exec -it assignment-2 bin/bash/

![image](https://user-images.githubusercontent.com/95872967/195509358-eaf16b44-a534-40a2-b539-99ae570deb38.png)
