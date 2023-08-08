# Installation
### Install Required Packages
```
sudo apt install docker.io
```
### Check if docker is installed successfully
```
docker --version
```
**Output**: <br>
`Docker version 20.10.21, build 20.10.21-0ubuntu1~22.10.2`<br>
*This may varry according to version you have installed*


# Post Installation
## Run the helloworld image on docker
*Docker commands, including `docker run` and some others, requires elevated permissions due to the security mechanisms implemented to restrict access to certain resources and functionalities of the Docker daemon.*
```
docker run helloworld
```
**Error**
```
docker: Got permission denied while trying to connect to the Docker daemon socket at unix:///var/run/docker.sock: Post "http://%2Fvar%2Frun%2Fdocker.sock/v1.24/containers/create": dial unix /var/run/docker.sock: connect: permission denied.
```

*The error occurs because the user executing the docker command does not have required permissions to access the Docker daemon socket.*


## Possible Fixes
### Use `sudo` before running docker commands
```
sudo docker run hello-world
```

OR

### Grant Read, Write and Execute permission for running Docker to User
*You will require to execute this command everytime you login into the shell*
```
sudo chmod u+rwx /var/run/docker.sock
```
*Once you execute this command then you can run docker commands without using sudo.*
```
docker run hello-world
```

OR

### Add User to the docker group
```
sudo chmod u+rwx /var/run/docker.sock
```
```
newgrp docker
```
```
docker run hello-world
```

