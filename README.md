# DEMO

This demo demostrates a simple python app which can be expose to 'localhost:8080' by a docker container.

## Requriments
- [docker](https://www.docker.com/)

## Inside the app folder:
1. the python app script `devops.py`.
2. templates for HTML files.
3. requirments for additional packages using by python.
4. Dockerfile build the python app as docker image.

## Walkthrough
NOTE: this demo is using the docker-compose structure to build & run the docker container.

To build & run the container on 'localhost:8080'

```
## make sure you are on the root directory.
docker-compose up --build -d

```
To see the size of the image that just created && look for `devops` image name.
```
docker images
```

To test the app please go to your browser on `localhost:8080` 

### cleanup
```
## to disable the running container && remove
docker-compose down

## to delete the image please copy the IMAGE ID and run:
docker rmi <IMAGE ID>
```
