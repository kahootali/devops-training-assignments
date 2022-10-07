Q1) Share screenshot of the above Branch Protection of `main` branch
Ans: Done and uploaded on the assignement 2 at Dice LMS Portal

Q2) Explain Docker Containers vs VMs
Ans: 
- VM has Hardware Level Virtualization where as Containers have OS Level Virtualization
- VM share hardware but has own OS, where as Container share hardware as well as OS Kernel, but it has its own OS. 
- VM takes more space as compare to Containers.

Q3) Explain Docker Architecture
Ans: In Docker, each container shares the same OS Kernel.Kubernettes is used to do clustering. 


Q4) Write command to create an nginx container in detached mode with name `assignment-2` running on host port `9090` and container port `80` on a custom network named `assignment-2`
Ans: docker container run -d --publish 9090:80 --name assignment-2 nginx

Q5) Write command to see logs of the above container
Ans: docker container logs assignment-2

Q6) Write commands to Exec into the container and cat the output of the default nginx file at /usr/share/nginx/html/index.html
Ans: docker container exec assignment-2
     docker contain 
     
- Create a PR from this branch to your `main` branch
- Now create a PR from your `main` branch to the parent's(kahootali/devops-training-assignment) repo `main` branch
- Link the PR to the issue that you created so that the issue gets closed automatically when PR gets merged
- Handle any comments on the review
- Get this PR merged into the parent repo