# docker

- If you have TTY errer use this command
- `alias docker="winpty docker"`
- `hello-world`

### docker commands
`docker pull image-name`
- docker run image-name`
`docker build -t image-name`
- docker push image-name`
- `docker run -d -p 2368:2368 image-name` ghost #this will create a container, if you want to see the logs run the command without `-d`
- How to check running container?
- `docker ps` and docker ps -a`


### Docker container life cycle
- `docker state, stop, start`

- How can we interact with running container?
- docker exec -it container-id bash `docker exec -it 56c356037ecb bash`
- `ls` then `cat config.development.json`

- cd `/usr/share/nginx/html`
-
- Run update `apt update -y`
- Install nano `apt install nano`
- Make changes to html file `nano index.html`
- docker run -d -p 99:80 abumarwa/docker:latest

- to access officiall docker documentation run this comand below
- `docker run -d -p 4000:4000 docs/docker.github.io`

### Docker commit & push
- `docker commit [OPTIONS] CONTAINER [REPOSITORY[:TAG]]`
- `docker push [OPTIONS] NAME[:TAG]`

#### Task
- copy usr/share/nginx/html - default location of nginx index.html using cp command
- Then commit and push
- Copy file from local to docker container `docker cp foo.txt container_id:/foo.txt` in this case `docker cp index.html fc0bc5f674c3:/usr/share/nginx/html/index.html` 
- Commit `docker commit fc0bc5f674c3 abumarwa/nginx_test:latest-v2`
- Push `docker push abumarwa/nginx_test:latest-v2`

#### Summary
- Docker Installation and setup completed
- Hyper V settings
- WSL2 and Linux subsystem enabled
- Docker commands