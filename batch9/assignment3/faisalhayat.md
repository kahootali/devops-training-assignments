Q#1 Do you complete all the labs ?
	
	Yes, I have completed all the labs.

Q#2 How to leverage cache using Dockerfiles?
	
	For the most part, the image cache is incredibly helpful and can save you a lot of time while building your images. However, there are times when the caching can bite you if you aren't paying attention, so it's good to know how to selectively bust the cache.

Q#3 What are multi-stage builds

	With multi-stage builds, you use multiple FROM statements in your Dockerfile. Each FROM instruction can use a different base, and each of them begins a new stage of the build. You can selectively copy artifacts from one stage to another, leaving behind everything you don’t want in the final image.

Q#4 Explain containers vs Image
	
	An image is a single file containing all the dependencies and all the configuration required to run a very specific program, for example nginx is the image that you just downloaded (by running command docker run nginx) was supposed to run.
	This is a single file that gets stored on your hard drive and at some point time you can use this image to create something called a container.

	A container is an instance of an image and you can kind of think it as being like a running program with it's own isolated set of hardware resources so it kind of has its own little set or its own little space of memory has its own little space of networking technology and its own little space of hard drive space as well.

Q#5 Explain RUN vs CMD vs Entrypoint

	RUN: The RUN command always gets executed in a new layer. It allows you to install packages and applications on top of an existing image layer and creates a new layer on top of it.

	CMD: Using a CMD command, you will be able to set a default command. This will be executed if you run a particular container without specifying some command. In case you specify a command while running a docker container, the default one will be ignored.

	ENTRYPOINT: It looks similar to a CMD command. However, the difference is that it does not ignore the parameters when you run a container with CLI parameters. You can override the ENTRYPOINT with the predefined tag.

Q#6 Improve the Dockerfile for python Application given in slides using the Dockerfile & then improve it and share image size & estimated build time for it

	Didn't find the file in slides.

Q#7 Run mysql container using the official image, by persisting data and passing environment variables to set username & password… You can see the information of how to persist and information here

	1- docker volume create mysql
	2- docker run --name="mysql_prod_server" -e MYSQL_ROOT_PASSWORD="root123" -e MYSQL_USER="miansarimhameed" -e MYSQL_PASSWORD="msh123" -v mysql:/var/lib/mysql -d mysql:8.0
