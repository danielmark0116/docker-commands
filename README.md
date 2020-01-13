# docker-commands
## GENERAL

### CONTAINER LIST

```docker ps```

```docker ps -a```

### CONTAINER REMOVE

```docker rm ID or NAME```

### THOROUGH CONTAINER INSPECTION

```
docker inspect NAME/ID
```

### IMAGES LiST

```docker images```
```docker images -a```

### IMAGE DELETE
###### first delete all depended containers

```docker rmi NAME```

### PULLing THE DOKCER IMAGES

```docker pull NAME OF IMAGE```

### RUNNING IMAGE

```docker run NAME``` - if image not present, will be downloaded

### EXECUTING COMMANDs on running containers

```docker exec CONTAINER COMMAND```

### DETACH mode

```docker run -d NAME``` - running in the background

You can also go back to (attach) to the container running in the background by:

```docker attach NAMe or ID of COntainer```

### INTERACTIVE MODE

running in interactive mode - e.g. listening for console inputs
```docker run -i NAME```

with -it flag it also gives the console prompt
```docker run -it NAME```

### PORT MAPPING

```docker -p HOSTYOUWANT:IMAGEPORT NAME```

### VOLUME MAPPING
you can map a given folder on your machine to the file system of the container

```
docker -v PATHinYOURfileSYSTEM:WHATpathINcontainerTOmap NAME
```

### LOGGING

```
docker logs NAME
```

## ENVIRONMENTAL VARIABLES

### RUN WITH GIVEN ENV

```
docker run -e VARNAME=value NAME
```

If you run container with custom ENVs, you can then inspect them with a `docker inspect NAME` command

# DOCKER COMPOSE

Deleting stuff from docker-compose and cleaning
```
docker-compose down -v --rmi all
```

Building from images and running / building form images
```
docker-compose up / build
```

Combining two compose files (eg. overwrite the primary one with the DEVELOPNET ONE
(replace COMMAND with e.g. UP DOWN or BUILD)
```
docker-compose -f docker-compose.yml -f docker-compose.dev.yml COMMAND
```
