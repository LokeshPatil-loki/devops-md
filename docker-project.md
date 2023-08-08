## Install Node.js LTS (v18.x):
```
curl -fsSL https://deb.nodesource.com/setup_lts.x | sudo -E bash - &&\
sudo apt-get install -y nodejs
```
## Dockerize Application
### Docker Login
```
docker login -u <username>
```

*Replace `<username>` with your docker username*


**Example**

`docker login -u lokilokesh`


*After executing above command you'll be propmted to enter the pasword of your dockerhub account.*

**Output:**
```
Password: 
WARNING! Your password will be stored unencrypted in /home/master/.docker/config.json.
Configure a credential helper to remove this warning. See
https://docs.docker.com/engine/reference/commandline/login/#credentials-store

Login Succeeded
```

