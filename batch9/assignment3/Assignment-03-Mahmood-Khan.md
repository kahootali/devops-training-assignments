Mahmood Khan
Dice-DevOps Batch-9
Assignment-03

Question-1:
All Labs completed.

Lab-1: Network:

# Create a Network
sudo docker network create new-network
sudo docker network ls
#Create 2 Containers of Centos
sudo docker container run --net new-network --name centos1 -it centos
# Create another Container on another shell of same VM. As after creating the first container it will log into the shell.
sudo docker container run --net new-network --name centos2 -it centos
# Now ping each container from another container.
# My Ping was successfull. Which eans they are now on same network and can communicate.
# After working, delete the Containers and then delete the network.
sudo docker container rm centos1 centos2
sudo docker network rm new-network

-------------------------------------------------------

Lab-2: Bin Mount:

sudo docker run -it --name web-server -p 8080:80 -v /home/ubuntu/dice_working/lab:/usr/local/apache2/htdocs/ httpd:2.4
# Now in another terminal:
cd /home/ubuntu/dice_working/lab
vi index.html

# Now open the browser and type: localhost:8080/index.html, you will be able to see the page we just created.
# The Cleanup Container:
sudo docker container stop web-server
sudo docker container rm web-server

#Go to the host directory that you mounted and list files, you should
see index.html still there
cd /home/ubuntu/dice_working/lab
ls

-------------------------------------------------------

Lab-3: Volume:
#Create named volume:
sudo docker volume create psql
#List volumes:
sudo docker volume ls

#Run postgres version 13 container:
#sudo docker container run --rm -it --net psql --name postgres1 -e POSTGRES_PASSWORD=testpwd -v psql:/var/lib/postgresql/data postgres:13
sudo docker container run --rm -it --name postgres1 -e POSTGRES_PASSWORD=testpwd -v psql:/var/lib/postgresql/data postgres:13


#Check logs and verify if postgres is configured, now stop & remove the container
sudo docker container stop postgres1
sudo docker container rm postgres1

#Now run postgres version 13.4 container: 
docker container run --rm -it --name postgres2 -e POSTGRES_PASSWORD=testpwd -v psql:/var/lib/postgresql/data postgres:13.4

# This will install the up version of PostGress and a message will also be displayed as below:
PostgreSQL Database directory appears to contain a database; Skipping initialization

sudo docker container stop postgres2
sudo docker container rm postgres2
sudo docker volume rm psql

-------------------------------------------------------

Lab: Docker Hub Accout.

DockerHub account is created and went thorugh the images. Different types of images.
#Below Output:
sudo docker login
Login with your Docker ID to push and pull images from Docker Hub. If you don't have a Docker ID, head over to https://hub.docker.com to create one.
Username: mihmood
Password:
WARNING! Your password will be stored unencrypted in /root/.docker/config.json.
Configure a credential helper to remove this warning. See
https://docs.docker.com/engine/reference/commandline/login/#credentials-store

Login Succeeded

-------------------------------------------------------

Lab: Entrypoint-vs-CMD

# Below is the output of terminal.

ubuntu@ip-172-31-94-39:~/docker-working/docker-samples/entrypoint-vs-cmd$ sudo docker build -t entry-vs-cmd-lab .
Sending build context to Docker daemon  2.048kB
Step 1/3 : FROM ubuntu
latest: Pulling from library/ubuntu
d19f32bd9e41: Pull complete
Digest: sha256:34fea4f31bf187bc915536831fd0afc9d214755bf700b5cdb1336c82516d154e
Status: Downloaded newer image for ubuntu:latest
 ---> df5de72bdb3b
Step 2/3 : ENTRYPOINT ["/bin/echo"]
 ---> Running in eedf5ae67a48
Removing intermediate container eedf5ae67a48
 ---> 40aef4ccbafd
Step 3/3 : CMD ["Hello, How are you? Students of Batch # 9"]
 ---> Running in 09eeefb11ee4
Removing intermediate container 09eeefb11ee4
 ---> 0ff9a5be4a33
Successfully built 0ff9a5be4a33
Successfully tagged entry-vs-cmd-lab:latest
ubuntu@ip-172-31-94-39:~/docker-working/docker-samples/entrypoint-vs-cmd$ sudo docker run -it entry-vs-cmd-lab
Hello, How are you? Students of Batch # 9
ubuntu@ip-172-31-94-39:~/docker-working/docker-samples/entrypoint-vs-cmd$ sudo docker run -it entry-vs-cmd-lab "Hello! This is an overwrite message ..."
Hello! This is an overwrite message ...
ubuntu@ip-172-31-94-39:~/docker-working/docker-samples/entrypoint-vs-cmd$

-------------------------------------------------------

Lab: Arg-vs-Env:

ubuntu@ip-172-31-94-39:~/docker-working/docker-samples/arg-vs-env$ sudo docker build -t arg-env .
Sending build context to Docker daemon  3.072kB
Step 1/5 : FROM ubuntu
 ---> df5de72bdb3b
Step 2/5 : ARG argument="Default Value for Arg"
 ---> Running in b341541b208a
Removing intermediate container b341541b208a
 ---> cea23f956436
Step 3/5 : ENV env_var="Default Value for Env"
 ---> Running in 3cb40fbeec9a
Removing intermediate container 3cb40fbeec9a
 ---> bcd431c7d1fe
Step 4/5 : RUN echo "The value for argument is: ${argument}"
 ---> Running in a337843ba4d5
The value for argument is: Default Value for Arg
Removing intermediate container a337843ba4d5
 ---> 5b719c0af237
Step 5/5 : RUN echo "The value for env var is: ${env_var}"
 ---> Running in 3aa50495350f
The value for env var is: Default Value for Env
Removing intermediate container 3aa50495350f
 ---> e6bf32bd3127
Successfully built e6bf32bd3127
Successfully tagged arg-env:latest


# After passing the arg value:

ubuntu@ip-172-31-94-39:~/docker-working/docker-samples/arg-vs-env$ sudo docker build --build-arg argument="New Valure for Arg" -t arg-env .
Sending build context to Docker daemon  3.072kB
Step 1/5 : FROM ubuntu
 ---> df5de72bdb3b
Step 2/5 : ARG argument="Default Value for Arg"
 ---> Using cache
 ---> cea23f956436
Step 3/5 : ENV env_var="Default Value for Env"
 ---> Using cache
 ---> bcd431c7d1fe
Step 4/5 : RUN echo "The value for argument is: ${argument}"
 ---> Running in 7e314946cbee
The value for argument is: New Valure for Arg
Removing intermediate container 7e314946cbee
 ---> 8f5174259dbb
Step 5/5 : RUN echo "The value for env var is: ${env_var}"
 ---> Running in 8ad17660d487
The value for env var is: Default Value for Env
Removing intermediate container 8ad17660d487
 ---> f430e295450a
Successfully built f430e295450a
Successfully tagged arg-env:latest


-------------------------------------------------------
Lab - Docker Images
#Run container and make changes

docker run -it ubuntu bash

cat <<EOF >> /home/test-file.txt
Name: Mahmood Khan
Container: Diceanalyticslab
EOF

press exit to get out of the container.

sudo docker ps -a
CONTAINER ID   IMAGE              COMMAND                  CREATED             STATUS                         PORTS                 NAMES
96e5b870f005   ubuntu             "bash"                   4 minutes ago       Exited (127) 3 seconds ago                           unruffled_knuth

Build image from a container
sudo docker commit 96e5b870f005 image-from-container
>sha256:a7c71b75e8e75a592b5661913d3cad6a94b575df6881de1e0402d9466008c702

#Now run this command to get Image ID that will be used in next command
sudo docker images
REPOSITORY             TAG       IMAGE ID       CREATED         SIZE
image-from-container   latest    a7c71b75e8e7   6 minutes ago   77.8MB

#Tag newly created image

#docker tag <IMAGE_ID> <yourDockerHubUsername>/<repoName>:<TAG>

sudo docker tag a7c71b75e8e7 mihmood/diceanalytics:v1.0

Login to your Docker Hub account
sudo docker login

Push image to Docker Hub
#docker push <yourDockerHubUsername>/<repoName>:<TAG>
sudo docker push mihmood/diceanalytics:v1.0

>> Final Output>>
ubuntu@ip-172-31-94-39:~$ sudo docker tag a7c71b75e8e7 mihmood/diceanalytics:v1.0
ubuntu@ip-172-31-94-39:~$ sudo docker login
Authenticating with existing credentials...

Login Succeeded

ubuntu@ip-172-31-94-39:~$ sudo docker push mihmood/diceanalytics:v1.0
The push refers to repository [docker.io/mihmood/diceanalytics]
2f158efde395: Pushed
629d9dbab5ed: Mounted from library/ubuntu
v1.0: digest: sha256:82add61ad2ae7f493f6b4050c35adb44373b14830a4ac472bb021fcd6066f6f6 size: 736

ubuntu@ip-172-31-94-39:~$

<<< output ends.

-------------------------------------------------------

All other labs were also done, but file was getting too big, later realized.

-------------------------------------------------------
-------------------------------------------------------

Q2) How to leverage cache using Dockerfiles

The commands that are freuently changed, keep them in the lower part of the Docker file. While the commands that remain same must be kept in the start of the Docker file.
This way, when we build the image, it will use the cache. As the Layers are saved and shared in docker. So it will use the Chache for those same commands.

-------------------------------------------------------
-------------------------------------------------------

Q3) What are multi-stage builds

We can use this to minimize the size of our image. 
With multi-stage builds, we use multiple FROM statements in our Dockerfile.
Each FROM instruction can use a different base, and each of them begins a new stage of the build.
We can selectively copy artifacts from one stage to another, leaving behind everything we don’t want in the final image.

-------------------------------------------------------
-------------------------------------------------------

Q4) Explain containers vs Image
Image are used to Run Containers. Container are running version of Images. 
Images can exist without containers, whereas a container needs to run an image to exist. 
Therefore, containers are dependent on images and use them to construct a run-time environment and run an application.
Multiple containers can share the same image.
Images can be created from 'scratch'. Downloaded from a resgitry (Dockerhub, ECR, etc).

-------------------------------------------------------
-------------------------------------------------------

Q5) Explain RUN vs CMD vs Entrypoint

Run: Run is a build-time command. Run a command in New Container. It will run the steps for example if we need any package to be installed that we need in the newly created container.
CMD:  It is a Run-time command. It is used to pass arguments to the Entrypoint command. CMD can be over-ridden at the start time of container.
Entrypoint: It is a builtime command. Takes Arguments from the CMD command. Cannot be over-ridden at start time of contaner.

-------------------------------------------------------
-------------------------------------------------------

Q6) Improve the Dockerfile for python Application given in slides using the Dockerfile & then improve it and share image size & estimated build time for it

REPOSITORY         TAG       IMAGE ID       CREATED          SIZE
python-app         latest    21638dfc04bd   43 minutes ago   477MB

>> This was taken after building improving the file.
Time for build was not displayed, as was Displayed during the Lecture. I also tried google to see the image build time but was not successfull. Help would be good in this area.

-------------------------------------------------------
-------------------------------------------------------

Q7) Run mysql container using the official image, by persisting data and passing environment variables to set username & password… You can see the information of how to persist and information here


Solution:
Final Command:
sudo docker run --name mahmood-db-mysql-05 -v /home/ubuntu/dice_working/mysql_container_lab/mysql_vol:/var/lib/mysql -e MYSQL_USER=mahmood1 -e MYSQL_PASSWORD -e MYSQL_ROOT_PASSWORD=12345 -d mysql:8.0.30

sudo docker ps -a   # To see your container running
sudo docker logs mahmood-db-mysql-05
sudo docker exec -it mahmood-db-mysql-05 bash

>>> Below is the output after connecting to the MySQL DB.
ubuntu@ip-172-31-94-39:~$ sudo docker exec -it mahmood-db-mysql-05 bash
bash-4.4# mysql -u root -p
Enter password:
Welcome to the MySQL monitor.  Commands end with ; or \g.
Your MySQL connection id is 8
Server version: 8.0.30 MySQL Community Server - GPL

Copyright (c) 2000, 2022, Oracle and/or its affiliates.

Oracle is a registered trademark of Oracle Corporation and/or its
affiliates. Other names may be trademarks of their respective
owners.

Type 'help;' or '\h' for help. Type '\c' to clear the current input statement.

mysql> show databases;
+--------------------+
| Database           |
+--------------------+
| dbtest             |
| information_schema |
| mysql              |
| performance_schema |
| sys                |
+--------------------+
5 rows in set (0.02 sec)

mysql>


<<<output ends<<

This above db was created in another mysql containe, but is visible here as well.


		X------------------------------------  End-of-File ------------------------------------X






 
