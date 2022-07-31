Q1) Share screenshot of the Protection of main branch?

  Here is the screenshot of my main branch:-
![main-protection](https://user-images.githubusercontent.com/42357170/180658875-00b6f11b-1cfe-43e4-a7d5-e47eb2fbd3ee.png)

Q2) Explain Docker Containers vs VMs?
  
  The concept of a virtual machine is simple, really: it’s a virtual server that emulates a hardware server. A virtual machine relies on the system’s physical hardware to emulate the exact same environment on which you install your applications. Depending on your use case, you can use a system virtual machine (that runs an entire OS as a process, allowing you to substitute a real machine for a virtual machine), or process virtual machines that let you execute computer applications alone in the virtual environment.
  Containers sit on top of a physical server and its host OS—typically Linux or Windows. Each container shares the host OS kernel and, usually, the binaries and libraries, too. (See below for definitions if you’re not familiar with these terms.) Shared components are read-only.

Q)3 Explain Docker Architecture?

Docker’s architecture is also client-server based. However, it’s a little more complicated than a virtual machine because of the features involved. It consists of four main parts:

  - Docker Client: This is how you interact with your containers. Call it the user interface for Docker.
  - Docker Objects: These are your main components of Docker: your containers and images. We mentioned already that containers are the placeholders for your software, and can be read and written to. Container images are read-only, and used to create new containers.
  - Docker Daemon: A background process responsible for receiving commands and passing them to the containers via command line.
  - Docker Registry: Commonly known as Docker Hub, this is where your container images are stored and retrieved.

Q4) Write command to create an nginx container in detached mode with name assignment-2 running on host port 9090 and container port 80 on a custom network named assignment-2

docker container run -d --publish 9090:80 --name assignment-2 nginx

Q)5 Write command to see logs of above container?

docker container logs assignment-2

Q6) Write commands to Exec into the container and cat the output of the default nginx file at /usr/share/nginx/html/index.html

docker exec "assignment-2" cat /usr/share/nginx/html/index.html
