# "Build your Python image" example

This tiny repo contains the files from the Docker tutorial at https://docs.docker.com/language/python/build-images/

Obviously you will need docker installed to build the container.

You will need Python 3 if you want to test the code, but if not, you can just build it into the container as the Dockerfile will build a Python 3.8 enabled image.

To build the image (the tutorial has more details):

`docker build --tag python-docker .`

I used this command to run the container, because my port 5000 was already in use.

`docker run -p 5005:5000 python-docker`

Or of course, to not run it in the foreground:

`docker run --detach -p 5005:5000 python-docker`

Because these instructions don't name the container, to kill it off, you will probably want to find the Container ID using:

`docker ps -a`

Then you can run:

`docker stop <ContainerID>`
