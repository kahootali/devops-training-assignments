Q1) Complete all the labs 
A1) Most of them are done
================================
Q2) How to leverage cache using Dockerfiles
A2) Cache speed up the build time. The place where we add cache command matters all the commands above cache command, if not changed, then they are cached. So the build time is reduced by not building those lines from start but to get them from cache
================================
Q3) What are multi-stage builds
A3) With multi-stage builds, we can use FROM command more than once, which keeps the image size down. With multi-stage builds, we clean up the artifacts which are no longer needed before we move to next layer.

Q4) Explain containers vs Image
A4) IMAGES:
	1. Image is package which comes with commands. 
	2. These images are reusable and can be moved from one machine to an other. 
	3. Images can have multiple containers running.
    CONTAINERS:
	1. Containers is the runtime of an image.
================================
Q5) Explain RUN vs CMD vs Entrypoint
A5) RUN: This command is used when the container is being build.
    CMD: This is executed when a container starts running
    EntryPoint: this is the command called when a container is first time accessed from out side of container


================================
Q7) Run mysql container using the official image, by persisting data and passing environment variables to set username & password
A7) compleed