# docker-commands

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

