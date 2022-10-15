Q1) Complete all the labs - Done

Q2) How to leverage cache using Dockerfiles 
>> Dockerfile help to avoid downloading image again and again.

Q3) What are multi-stage builds 
>> You can use different container to build a binary and than release that build by simply using the binary in a seprate image whcih does not contain the run time or build time of the language. 

Q4) Explain containers vs Image 
>> Images are the pre build package where as container is a run time of that image. 

Q5) Explain RUN vs CMD vs Entrypoint 
>> First thing that execute is Entrypoint, followied by CMD. RUN is used to execute any command. 

Q6) Improve the Dockerfile for python Application given in slides using the Dockerfile & then improve it and share image size & estimated build time for it
>> Size: 5.54MB and Build Time: 
Q7) Run mysql container using the official image, by persisting data and passing environment variables to set username & password… You can see the information of how to persist and information here
>> Done

https://hub.docker.com/_/mysql

- Create a PR from this branch to your `main` branch
- Now create a PR from your `main` branch to the parent's(kahootali/devops-training-assignment) repo `main` branch
- Link the PR to the issue that you created so that the issue gets closed automatically when PR gets merged
- Handle any comments on the review
- Get this PR merged into the parent repo