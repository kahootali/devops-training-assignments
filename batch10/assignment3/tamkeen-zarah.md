## Q1) Complete all the labs

Done

## Q2) How to leverage cache using Dockerfiles
  
### By placing the files at a lower position in herarchy which has be used more often otherwise they will build each time the build is run.

## Q3) What are multi-stage builds

### Where executables doesnot require build packages

## Q4) Explain containers vs Image

### Image
          - Image is a package 
          - A snapshot of a container
          - changes are made in  images
### Container 
          - is the running state of that package/ image
          - works as a VM but feels like real entity

## Q5) Explain RUN vs CMD vs Entrypoint

### RUN:	
          - a buildtime command
          - creates new layer at run time
### CMD:	
          - a run time command
	        - can be overridden when container starts
	        - passed as an argument to Entrypoint
### ENTRYPOINT:	
          - a run time command
          - first command to run when container starts
      
## Q6) Improve the Dockerfile for python Application given in slides using the Dockerfile & then improve it and share image size & estimated build time for it

## Q7) Run mysql container using the official image, by persisting data and passing environment variables to set username & password… You can see the information of how to persist and information here



