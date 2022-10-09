# Q1) Share screenshot of the above Branch Protection of main branch

![Branch Protection of main branch](https://user-images.githubusercontent.com/62700476/194774394-a514f13d-35b8-42e2-90a0-0504059f3fad.png)


# Q2) Explain Docker Containers vs VMs

## Docker Containers

- OS level virtualisation
- light weight
- Fast
- Simply isolated processes 
- Memory efficient

## VMs

- Hardware level virtualisation
- Shared apps
- Dedicated memory

# Q3) Explain Docker Architecture

- Docker is a tool used for containerization
- Sharing of images
- It can create,ship and run containers
- Runs as a single process

# Q4) Write command to create an nginx container in detached mode with name assignment-2 running on host port 9090 and container port 80 on a custom network named assignment-2

docker container run -d --publish 9090:80 assignment-2

# Q5) Write command to see logs of the above container

docker container logs

# Q6) Write commands to Exec into the container and cat the output of the default nginx file at /usr/share/nginx/html/index.html

Create a PR from this branch to your main branch
Now create a PR from your main branch to the parent's(kahootali/devops-training-assignment) repo main branch
Link the PR to the issue that you created so that the issue gets closed automatically when PR gets merged
Handle any comments on the review
Get this PR merged into the parent repo
