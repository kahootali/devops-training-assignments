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