# Introduction to Docker
## Docker Slides
- You can package your code in containers
- Containers makes it easy to "ship" code anywhere as-is
- You can practically run containers on any machine
- Compared to VMs, Containers takes less resources as it doesn't need to virtualize hardware
## Running Docker
- You can run an Ubuntu container with `docker run -it ubuntu bash`, docker will spin up an instance of containerized Ubuntu with Bourne Again Shell (BASH)
- You can run wreck the instance without it affecting your system
- You can spin up containerized instances as many as you'd like
- You can run a python instance in Docker with `docker run -it python:3.x`
- You can run python inside an Ubuntu(?) instance with bash with `docker run -it --entrypoint=bash python:3.x`
## Writing Dockerfile
```
// specifies the image
FROM python:3.x

// executes the command
RUN pip install pandas

// overrides the prompt
ENTRYPOINT ["bash"]
```
- You can build an image with the dockerfile with `docker build -t <name>:<tag> <path>`
- And run it with `docker run -it <name>:<tag>`
```
// specifies the image
FROM python:3.x

// executes the command
RUN pip install pandas

// specifies the working directory
WORKDIR /app

// copies the file in local machine to container
COPY <filename>.py <filename>.py

// overrides the prompt
ENTRYPOINT ["bash"]
```

# Ingesting NY Taxi Data to Postgres
## 
