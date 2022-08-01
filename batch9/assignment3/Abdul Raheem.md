# Assignment 3

Q1) Complete all the labs

Ans All Labs are done

Q2) How to leverage cache using Dockerfiles

Ans As we already know docker file execute from top to bottom. So we put the stable parts on top and the most frequestly changing parts at the bottom.

Q3) What are multi-stage builds

Ans To create a multistage build Dockerfile is to use multiple FROM statements to reference a specific image necessary for that stage. Docker recommends you name each stage to simplify the process of copying results from one stage into the final image with the AS qualifier.

Q4) Explain containers vs Image

Ans Images are read-only templates containing instructions for creating a container. A Docker image creates containers to run on the Docker platform.
A container is an isolated place where an application runs without affecting the rest of the system and without the system impacting the application.

Q5) Explain RUN vs CMD vs Entrypoint

Ans

RUN:
When you use a RUN command in your dockerfile, it always creates a new intermediate image layer on top of the previous ones. That’s why it is always recommended chaining all the RUN commands together.

CMD:
A CMD command is used to set a default command that gets executed once you run the Docker Container. In case you provide a command with the Docker run command, the CMD arguments get ignored from the dockerfile. In the case of multiple CMD commands, only the last one gets executed.

Entrypoint:
An ENTRYPOINT command, unlike CMD, does not ignore additional parameters that you specify in your Docker run command.


Q6) Improve the Dockerfile for python Application given in slides using the Dockerfile & then improve it and share image size & estimated build time for it

Q7) Run mysql container using the official image, by persisting data and passing environment variables to set username & password… You can see the information of how to persist and information here
