### Example php web server
This is a simple web server based on Flask. This version of code is specific to Ubuntu OS.

#### Build docker image 
`docker build -t phpapp:latest .`

#### List the image
`docker image ls`

#### Run the app in the container in the foreground
`docker container run -p 8000:80 --name myphpapp --rm phpapp:latest`

#### Run the app in the container in the detached and interactive mode
`docker container run -dit -p 8000:80 --name myphpapp --rm phpapp:latest`

#### Get interactive bash terminal into the container
`docker container exec -it myphpapp bash`

#### Run php file present into the container
`docker container exec -it myphpapp php -f /var/www/html/index.php`

#### Attach to the container but you can not do much here. Press Ctl+p Ctl+q to come out without stopping the container
`docker attach myphpapp`

#### check the docker logs
`docker logs myphpapp`

#### run the curl to verify that app is working
`curl http://localhost:8000`
