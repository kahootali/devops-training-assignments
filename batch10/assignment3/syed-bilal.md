2- Using dockerfiles, you donot have to download the image everytime. Once downloaded it ca nbe used multiple times.

3- With multi-stage builds, you use multiple FROM statements in your Dockerfile. Each FROM instruction can use a different base, and each of them begins a new stage of the build.

4- Image is a template and container runs that template

5- Entry point is the first command that runs. CMD sets the command and its parameters to be executed by default. RUN executes commands and creates new image layers.

6- Size: 6.12MB

7- Done