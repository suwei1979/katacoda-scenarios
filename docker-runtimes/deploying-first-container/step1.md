# Step 1 - Running A Container
The first task is to identify the name of the Docker Image which is configured to run Redis. With Docker, all containers are started based on a Docker Image. These images contain everything required to launch the process; the host doesn't require any configuration or dependencies.

Jane can find existing images at registry.hub.docker.com/ or by using the command docker search <name>. For example, to find an image for Redis, you would use `docker search redis`{{execute}}.

# 运行容器

第一个任务是识别配置为运行Redis的Docker映像的名称。对于Docker，所有容器都基于Docker映像启动。这些图像包含启动流程所需的一切；主机不需要任何配置或依赖项。

Jane可以在注册表中找到现有图像。中心码头工人。com/或使用命令docker search<name>。例如，要查找Redis的图像，可以使用:

`docker search redis`{{execute}}

# Task
通过使用search命令，Jane识别出Redis Docker映像名为Redis，并希望运行最新版本。由于Redis是一个数据库，Jane希望在继续工作时将其作为后台服务运行。

要完成此步骤，请在后台启动一个容器，根据官方图像运行Redis实例。

Docker CLI有一个名为run的命令，该命令将基于Docker映像启动容器。结构是docker run<options><image name>。

默认情况下，Docker将在前台运行命令。要在后台运行，需要指定选项-d。

`docker run -d redis`{{execute}}

默认情况下，Docker将运行可用的最新版本。如果需要特定的版本，可以将其指定为标记，例如版本3.2将是 docker run-d redis:3.2。

由于这是Jane第一次使用Redis映像，这个镜像将被从远程仓库下载到当前运行Docker的主机上。