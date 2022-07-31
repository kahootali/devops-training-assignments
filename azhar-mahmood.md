How to leverage caching in docker?
Leveraging your cache involves layering your images so that only the bottom layers change often. 
You want your RUN steps that change more frequently towards the bottom of the Dockerfile, while steps that change less often should be ordered towards the top.

What are multi-stage builds?
With multi-stage builds, you use multiple FROM statements in your Dockerfile. Each FROM instruction can use a different base, 
and each of them begins a new stage of the build. You can selectively copy artifacts from one stage to another, 
leaving behind everything you don't want in the final image.

Explain containers vs Image?
Images describe the applications and how they can be run. Containers are the image instances, where multiple containers of the same image can be run, 
each in a different state.

Explain RUN vs CMD vs Entrypoint?
RUN executes commands and creates new image layers.
CMD sets the command and its parameters to be executed by default after the container is started. However CMD can be replaced by docker run command line parameters.
ENTRYPOINT configures the command to run when the container starts, similar to CMD from a functionality perspective.

