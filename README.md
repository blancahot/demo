# Demo

This demo demonstrates 2 simple python apps which one of them can be expose to 'localhost:8081' by a docker container and the other trigged by a specific workflow.

## Requriments
- [docker](https://www.docker.com/)

## Inside app folder:
1. The python app script `devops.py`.
2. Templates for HTML files.
3. Requirments for additional packages using by python.
4. Dockerfile build the python app as docker image.

## Inside app2 folder:
1. A simple python script with print command.

## Walkthrough
### Run Locally:
NOTE: This demo is using the docker-compose structure to build & run the docker container.

To build & run the container on 'localhost:8081'

```
## make sure you are on the root directory.
docker-compose up --build -d

```
To see the size of the image that just created && look for `devops` image name.
```
docker images
```

To test the app please go to your browser on `localhost:8081` 

### cleanup
```
## to disable the running container && remove
docker-compose down

## to delete the image devops please copy the IMAGE ID and run:
docker rmi <IMAGE ID>
```

### Run by github-actions workflow:
This demo also trigged by an github-action [workflow](.github/workflows/python.yaml) which can be trigged by a merged pull request to 'main' branch. 

The workflow will excute [app2](app2/main.py).

