Q1) Complete all the labs
    Done.
Q2) How to leverage cache using Dockerfiles
    As each instruction executed Docker picks image from its cache it doesn't create new image each time
    that is how Docker manage leverage cache. If you don't want to use cache you can use --no-cache=true option.
Q3) What are multi-stage builds
    In multi-stage build you can use multiple FROM instruction each start with different base. It is useful for production ready applications. In one docker file you can build more than one docker images.
Q4) Explain containers vs Image
    Container is isolated running process and shares kernel of the host Operating System. 
    Container is running form of an application.
    Image is packaged form of an application. 
Q5) Explain RUN vs CMD vs Entrypoint
    RUN is buildtime command if you want to run any command while building image.
    CMD and Entrypint are runtime command which command will run while running the container.
    CMD is parameter to Entrypoint command it means it is passed as an argument to Entrypoint command if it mentioned otherwise it will become first command.
Q6) Improve the Dockerfile for python Application given in slides using the Dockerfile & then improve it and share image size & estimated build time for it

Q7) Run mysql container using the official image, by persisting data and passing environment variables to set username & password… You can see the information of how to persist and information here