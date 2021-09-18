
URL and help section
```

https://github.com/academiaonline - Sebastian's GitHub

notepad.pw/simplilearndocker
https://www.linkedin.com/in/scolomar/

https://docs.docker.com/
https://docs.docker.com/engine/install/linux-postinstall/
https://docs.docker.com/engine/security/#docker-daemon-attack-surface
https://en.wikipedia.org/wiki/LXChttps://en.wikipedia.org/wiki/Linux_namespacessudo

https://hub.docker.com/
https://hub.docker.com/_/ubuntu

https://github.com/tianon/docker-brew-ubuntu-core/blob/49f002ba206e2cea2024aaa9f6f4ee4e9fb5c084/focal/Dockerfile

https://github.com/academiaonline/simplilearn-dockercoins/blob/2021-09/README.md

```

Commands
```

Login into docker container shell
#################################
docker container exec -it test sh

sudo docker --version 
sudo docker container run --detach --name test1 --tty library/ubuntu:latest 

sudo docker container ls
sudo docker container top test1
sudo docker container exec test1 ps aux
sudo docker container exec test1 apt-get update
sudo docker container exec test1 apt-get install net-tools -y
sudo docker container exec test1 dpkg -L net-tools | grep bin
sudo docker container exec test1 route -n
sudo docker container exec test1 apt-get install net-tools -y
sudo docker container run --rm library/ubuntu:latest route -n
sudo docker container commit test1 library/ubuntu:net-tools
sudo docker container cp test1:/bin/netstat .
sudo docker container diff test1
sudo docker container export --output test1.tar test1
sudo docker container run hello-world

sudo docker events

sudo docker --debug --log-level debug events

sudo docker image import test1.tar library/ubuntu:test1   
sudo docker image history library/ubuntu:test1
sudo docker image history library/ubuntu:latest


sudo tar zcf ubuntu-focal-oci-amd64-root.tar.gz /	sudo docker container exec --tty test1 top	sudo docker image history library/ubuntu:net-tools
sudo docker container exec test1 apt-get install net-tools -y
sudo docker container commit test1 library/ubuntu:net-tools
sudo docker container run --detach --name test1 --tty library/ubuntu:latest 
sudo docker container exec test1 apt-get update
sudo docker container exec test1 apt-get install net-tools -y
sudo docker container commit test1 library/ubuntu:net-tools

sudo docker image build --file Dockerfile.net-tools --tag library/ubuntu:net-tools-dockerfile .
sudo docker container run --rm library/ubuntu:net-tools-dockerfile route -n
sudo docker container run --rm library/ubuntu:latest route -n
sudo docker image history library/ubuntu:net-tools-dockerfile
sudo docker image import test1.tar library/ubuntu:test1
sudo docker system info
sudo tar zcf docker.tar.gz /var/lib/docker
sudo docker container inspect test1
sudo docker image inspect library/ubuntu:latest
sudo docker image inspect library/ubuntu:net-tools-dockerfile
sudo docker image history library/ubuntu:net-tools-dockerfile

sudo docker container run --detach --name test3 --tty library/ubuntu:latest

sudo docker container ls --all --no-trunc
sudo ls /var/lib/docker/containers
sudo find /var/lib/docker/containers
sudo docker container rm test3
sudo docker image rm library/ubuntu:latest
sudo docker container run --name pinger library/alpine:latest ping localhost
sudo docker container pause pinger
sudo docker container unpause pinger

```

DB and Volume
```
https://github.com/academiaonline/postgres

```

Network
```

https://github.com/academiaonline/dca/blob/main/networking.md

To connect container 2 with the same n/w in which container 1 is part of 
########################################################################
docker network connect net1 c2

require 'digest'
require 'sinatra'
require 'socket'
```


Docker Swarm
```
docker swarm init
docker stack deploy --compose-file docker-compose.yaml SIMPLILEARN-DOCKERCOINS
docker service ls
docker stack ls
docker stack ps SIMPLILEARN-DOCKERCOINS --no-trunc
docker stack rm SIMPLILEARN-DOCKERCOINS

watch sudo docker service ls

```

Sample Dockerfile

```
cat Dockerfile.net-tools 
FROM    library/ubuntu:latest
RUN     apt-get update
RUN     apt-get install net-tools -y 
```
