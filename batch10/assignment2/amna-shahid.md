Q2) Explain Docker Containers vs VMs
Ans) Docker Container:  
	1. Vertualizes envirnoment only at app level
	2. faster to load
				
	VMs: 
	1.Vertualizes envirnoment only at OS level
	2. takes more time than Docker container. 

=================================================================


Q3) Explain Docker Architecture
Ans) Docker follows client-server architecture. it has 3 components
	1. Client: client has commands to run. using these commands client communicates with docker deamon (server). Examples of client commands are
docker build
docker pull
docker run
	2. Docker Host: Docker Host is used to provide an environment to execute and run applications. It contains the docker daemon, images, containers, networks, and storage.
	3. Docker Registry: Docker Registry manages and stores the Docker images. 


Q4) Write command to create an nginx container in detached mode with name `assignment-2` running on host port `9090` and container port `80` on a custom network named `assignment-2`
Ans) docker run --name assignment-2 9090:80 -d nginx

=================================================================

Q5) Write command to see logs of the above container
Ans) docker logs –details assignment-2

=================================================================



Q6) Write commands to Exec into the container and cat the output of the default nginx file at /usr/share/nginx/html/index.html

