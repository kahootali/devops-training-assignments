# Dice Analytics DevOps Professional Training
## Batch No. 6 - Assignment No. 3

<br />

:bulb: **Question No. 1: Do you complete all the labs ?**

<br />

Yes, I have completed all the labs which are mentioned in the slides.

---

<br />

:bulb: **Question No. 2: How to leverage cache using Dockerfiles ?**

<br />

You should try and keep the stable parts toward the top and make your additions at the bottom.

If you know you need to install a bunch of OS packages in your image (which is typically one of the slower parts of building an image) put your package installation instructions toward the top of the Dockerfile. Because in the image building process, Docker steps through the instructions in your Dockerfile, executing each in order. At each instruction, Docker searches for an existing image in its cache to use instead of creating a new duplicate image.

---

<br />


:bulb: **Question No. 3: What are multi-stage builds ?**

<br />

With multi-stage builds, you use multiple FROM statements in your Dockerfile. Each FROM instruction can use a different base, and each of them begins a new stage of the build. You can selectively copy artifacts from one stage to another, leaving behind everything you don’t want in the final image.

---

<br />

:bulb: **Question No. 4: Explain Container vs Image ?**

<br />

| Docker Image | Docker Container |
| --- | --- |
| An image is a single file containing all the dependencies and all the configuration required to run a very specific program, for example nginx is the image that you just downloaded (by running command docker run nginx) was supposed to run.<br />This is a single file that gets stored on your hard drive and at some point time you can use this image to create something called a container. | A container is an instance of an image and you can kind of think it as being like a running program with it's own isolated set of hardware resources so it kind of has its own little set or its own little space of memory has its own little space of networking technology and its own little space of hard drive space as well. |

---

<br />

:bulb: **Question No. 5: Explain RUN vs CMD vs ENTRYPOINT ?**

<br />

**RUN:** 
The RUN command always gets executed in a new layer. It allows you to install packages and applications on top of an existing image layer and creates a new layer on top of it.

**CMD**: 
Using a CMD command, you will be able to set a default command. This will be executed if you run a particular container without specifying some command. In case you specify a command while running a docker container, the default one will be ignored.

**ENTRYPOINT:**
It looks similar to a CMD command. However, the difference is that it does not ignore the parameters when you run a container with CLI parameters. You can override the ENTRYPOINT with the predefined tag.

---

<br />

:bulb: **Question No. 6: Improve the Dockerfile for python Application given in slides using the Dockerfile & then improve it and share image size & estimated build time for it.**

I didn't find the exact above mentioned dockerfile from the slides provided my Dice Analytics. Now the time is extreamly short for submitting this assignment. I will provide the answer separately on the direct message. Thanks :relaxed:

---