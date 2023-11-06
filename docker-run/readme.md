## What happens when you run **docker run**

1. Looks for that image locally in image cache, doesn't find anything
2. Then looks in remote image repository(default to Docker Hub)
3. Downloads the latest version (nginx: latest by default)
4. Creates a new container based on that image and prepares to start
5. Gives it a virtual IP on a private network inside docker engine(virtual network)
6. Opens the specified port, 80 on host and forwards to port 80 in container
7. Start container by using the CMD in the image Dockerfile

Example:

docker run --publish 8080:80 --name webhost -d nginx:1m11 nginx -T

__Change host listening port__
__Change version of image__
__Change CMD run on start__