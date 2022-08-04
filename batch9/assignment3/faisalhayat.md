Q#1 Do you complete all the labs ?
	
	Yes, I have completed all the labs.

Q#2 How to leverage cache using Dockerfiles?
	
	For the most part, the image cache is incredibly helpful and can save you a lot of time while building your images. However, there are times when the caching can bite you if you aren't paying attention, so it's good to know how to selectively bust the cache.

Q#3 What are multi-stage builds

	With multi-stage builds, you use multiple FROM statements in your Dockerfile. Each FROM instruction can use a different base, and each of them begins a new stage of the build. You can selectively copy artifacts from one stage to another, leaving behind everything you don’t want in the final image.