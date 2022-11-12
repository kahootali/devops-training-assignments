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
    1st time it took Building 53.1s. and size is 51.8MB.

    I used multistage concept to reduce the size and improve it 
    then it took 8.1s. and size is 5.54MB. updated code is following

    FROM python:3.6-alpine as build

    LABEL name="Python Application" \   
     maintainer="malikahsan <malik.ahsan@outlook.com>" \
     summary="A Sample Python application"

    # Create app directory
    WORKDIR /app

    EXPOSE 8080

    RUN pip install flask

    COPY app.py ./

    CMD [ "python", "./app.py" ]

    FROM alpine

    LABEL name="Python Application" \   
        maintainer="malikahsan <malik.ahsan@outlook.com>" \
        summary="A Sample Python application"

    EXPOSE 8080

    COPY --from=build ./app ./app

    CMD ["python" , "./app.py"]


Q7) Run mysql container using the official image, by persisting data and passing environment variables to set username & password… You can see the information of how to persist and information here
