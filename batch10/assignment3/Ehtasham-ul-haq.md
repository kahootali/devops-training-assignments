Q2) How to leverage cache using Dockerfiles
	
	Leveraging your cache involves layering your images so that only the bottom layers change often.
	You want your RUN steps that change more frequently towards the bottom of the Dockerfile, 
	while steps that change less often should be ordered towards the top

Q3) What are multi-stage builds

	With multi-stage builds, you use multiple FROM statements in your Dockerfile.
	Each FROM instruction can use a different base, and each of them begins a new stage of the build.
	You can selectively copy artifacts from one stage to another, leaving behind everything you don't
	want in the final image.

	FROM golang:1.16 AS builder
	WORKDIR /go/src/github.com/alexellis/href-counter/
	RUN go get -d -v golang.org/x/net/html  
	COPY app.go ./
	RUN CGO_ENABLED=0 go build -a -installsuffix cgo -o app .

	FROM alpine:latest  
	RUN apk --no-cache add ca-certificates
	WORKDIR /root/
	COPY --from=builder /go/src/github.com/alexellis/href-counter/app ./
	CMD ["./app"] 

Q4) Explain containers vs Image

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
	
	FROM python:3.6-alpine

	RUN pip install --upgrade pip ADD app.py ./

	CMD [ "python", "./app.py" ]

## Q7) Run mysql container using the official image, by persisting data and passing environment variables to set username & password… You can see the information of how to persist and information here
	1- docker volume create mysql
	2- docker run --name="mysql_prod_server" -e MYSQL_ROOT_PASSWORD="root123" -e MYSQL_USER="mainehtashamulhaq" -e MYSQL_PASSWORD="test@123" -v mysql:/var/lib/mysql -d mysql:8.0
