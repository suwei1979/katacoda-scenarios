# Step 1 - Running A Container
The first task is to identify the name of the Docker Image which is configured to run Redis. With Docker, all containers are started based on a Docker Image. These images contain everything required to launch the process; the host doesn't require any configuration or dependencies.

Jane can find existing images at registry.hub.docker.com/ or by using the command docker search <name>. For example, to find an image for Redis, you would use `docker search redis`{{execute}}.

# Task
Using the search command, Jane has identified that the Redis Docker Image is called redis and wants to run the latest release. Because Redis is a database, Jane wants to run it as a background service while she continues to work.

To complete this step, launch a container in the background running an instance of Redis based on the official image.

The Docker CLI has a command called run which will start a container based on a Docker Image. The structure is docker run <options> <image-name>.

By default, Docker will run a command in the foreground. To run in the background, the option -d needs to be specified.

`docker run -d redis`{{execute}}

By default, Docker will run the latest version available. If a particular version was required, it could be specified as a tag, for example, version 3.2 would be docker run -d redis:3.2.

As this is the first time Jane is using the Redis image, it will be downloaded onto the Docker Host machine.