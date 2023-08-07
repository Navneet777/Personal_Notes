
Docker Basics Comands
---------------------
FROM <image>	Defines a base for your image.
RUN <command>	Executes any commands in a new layer on top of the current image and commits the result. RUN also has a shell form for running commands.
WORKDIR <directory>	Sets the working directory for any RUN, CMD, ENTRYPOINT, COPY, and ADD instructions that follow it in the Dockerfile.
COPY <src> <dest>	Copies new files or directories from <src> and adds them to the filesystem of the container at the path <dest>.
CMD <command>	Lets you define the default program that is run once you start the container based on this image. Each Dockerfile only has one CMD, and only the last CMD instance is respected when multiple exist.

**Build Docker Command:**
docker build -t test:latest .    
note:- here test is image name and latest is tag (it's optional) and (.) means it's represent current directory.

**Docker RUN Command**
docker run -p 8000:8000 test:latest

**List of Containers**
docker ps (list of active container)
docker ps -a (list of active and inactive container)

**Login Inside Container**
docker exec -it <container id> bash or sh

**Restart Docker Container**
docker restart <container id>

**Start Docker Container**
docker start <container id>

**Stop Docker Container**
docker stop <container id>

**Check Docker Logs**
docker logs -f <container id>
