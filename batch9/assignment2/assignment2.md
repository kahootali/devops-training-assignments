# Assignment 2

Q1) Share screenshot of the above Branch Protection of `main` branch

Q2) Explain Docker Containers vs VMs
Answer: Docker containers are considered suitable to run multiple applications over a single OS kernel; whereas, virtual machines are needed if the applications or services required to run on different OS.

Q3) Explain Docker Architecture
Answer: Docker follows Client-Server architecture, which includes the three main components that are Docker Client, Docker Host, and Docker Registry.
    Docker Client:
        Docker Client uses Command Line Interface (CLI) to run the following commands -

                docker build

                docker pull

                docker run
    Docker Host:
        Docker Host is used to provide an environment to execute and run applications. It contains the docker daemon, images, containers, networks, and storage.
    Docker Registry:
        Docker Registry manages and stores the Docker images.There are two types of registries in the Docker -
            Pubic Registry:
                 Public Registry is also called as Docker hub.
            Private Registry:
                It is used to share images within the enterprise.
Q4) Write command to create an nginx container in detached mode with name `assignment-2` running on host port `9090` and container port `80` on a custom network named `assignment-2`

Q5) Write command to see logs of the above container

Q6) Write commands to Exec into the container and cat the output of the default nginx file at /usr/share/nginx/html/index.html


