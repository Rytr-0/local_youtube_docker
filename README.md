# Local YouTube Dockerized!

------
Local youtube dockerized is based on user234683 [youtube-local](https://github.com/user234683/youtube-local).

This is about the same code but slightly changed to allow it to run in a docker container properly.

## Usage:

To use it you can just use the docker image from docker hub [here](https://hub.docker.com/repository/docker/rytrx0/localyoutube).

Or you can build the image yourself:

### Docker build:

```
git clone https://github.com/Rytr-0/local_youtube_docker.git
cd local_youtube_docker
cd youtube-local
docker build -t localyoutube .
```

### Docker compose:

 
```
cd local_youtube_docker
docker compose up
```

Now it's started!

> Never use Ctrl + C, for stopping the container run:

`docker compose down`

### Website:

If I make anything, it will be on my website [here](https://Rytr0.com)

## Credit:

Credit for user234683 for the awesome [youtube-local](https://github.com/user234683/youtube-local) 

