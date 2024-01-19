# Local YouTube Dockerized!

------
Local youtube dockerized is based on user234683 [youtube-local](https://github.com/user234683/youtube-local).

This is about the same code but slightly changed to allow it to run in a docker container properly.

## Usage:

To use it you can just use the docker image from docker hub [here](https://hub.docker.com/repository/docker/rytrx0/localyoutube).

Or you can build the image yourself:

### Docker build:

`git clone https://github.com/Rytr-0/local_youtube_docker.git
cd local_youtube_docker
cd youtube-local
docker build -t localyoutube .`

### Docker compose:

#### Running with a volume:

The docker compose file expects a volume mapping in the following directory:

`    volumes:
        - ./LYT_testing:/localYT/`
        
Where **LYT_testing** is a duplicate of the **youtube-local** directory.

You can keep **/localYT/** as it is because it's inside of the docker image itself.

The reason for the volume is that there is a bug that returns *Error 403 forbidden* each time the *save settings* button is pressed.

Therefore, mapping the volume allows to change the setings from the **settings.txt** file inside of youtube-local directory.

Once you provide the duplicate directory or the volume, you can run :
 
`cd local_youtube_docker
docker compose up
`
Now it's started!

#### Running with no volume:

You can just run it as is without any volume but that means you can't change the settings.

To do that just go into the **compose.yml** file and *delete the lines 10-11 with the name 'volumes'*

> Never use Ctrl + C, for stopping the container run:

`docker compose down`

### Website:

If I make anything, it will be on my website [here](Rytr0.com)

## Credit:

Credit for user234683 for the awesome [youtube-local](https://github.com/user234683/youtube-local) 

