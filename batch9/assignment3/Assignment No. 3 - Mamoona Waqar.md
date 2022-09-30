Q1) Complete all the labs. 70% to 80% completed.

Q2) How to leverage cache using Dockerfiles?

A build cache maintains the previous state of image build and uses already built commands if there is no change in those particular commands. Hence placing statements in such order that those statements are put first which are if once executed will not change frequently in future and thus no need to build them every time will greatly enhance build time. Properly planned image file can result in less resource consumption especially in terms of time and memory due to build cache.

Q3) What are multi-stage builds

Multistage builds refer to building image in multiple stages. For example if you need to build golang code. You can build the code in one FORM command using the golang builder which produce the artifact and the exe for your code. And in the next stage use only the exe produced from the previous FROM command and use another FROM command including only the required applications or OS on which you need to run the exe. Multistage builds include multiple FROM commands and the code from the last FROM command remains after the image is built. All the previous FROM commands are discarded after they are executed while building the image.

Q4) Explain containers vs Image

An image is simply a runnable component with filesystem. Docker image is a file composed of multiple layer, used to execute code in docker container. An image basically is a packaged form of an application. A container is a running form of an image, created when we start an image with ‘run’ command. When a container is created a thin read/write layer is put on top of image, Any changes made to the container is put on this read/write layer during the lifetime of the container. We can start multiple containers of same image and each container runs in complete isolation which means each container maintains its own data safely on the top of the Docker Images as each has its own read/write layer

Q5) Explain RUN vs CMD vs Entrypoint

RUN is a build time command, if you want to run any command during the build time of an image. CMD and Entrypoint are run time commands which can be used while running the container if any commands need to be executed. Entrypoint is the first command that is executed while running the container. If Entrypoint is not defined then CMD becomes first command. If Entrypoint is defined in image file then CMD is passed as argument to Entrypoint.

Q6) Improve the Dockerfile for python Application given in slides using the Dockerfile & then improve it and share image size & estimated build time for it

FROM python:3.10-alpine

RUN pip3 install --upgrade pip ADD app.py ./

CMD [ "python3", "./app.py" ]

Image size: 65.8MB Time: 6sec

Q7) Run mysql container using the official image, by persisting data and passing environment variables to set username & password… You can see the information of how to persist and information here

https://hub.docker.com/_/mysql

Answer: ubuntu@ubuntu-asus:~/docker-samples$ sudo docker run --name mysql-new -v ~/docker-samples/mysql/persist-data:/var/lib/mysql -e MYSQL_ROOT_PASSWORD=1234 -e MYSQL_USER=mamoona -e MYSQL_PASSWORD=0000 -d mysql
