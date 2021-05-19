# Estudo sobre node-red

docker run -it -p 1880:1880 -v node_red_data:/data --name mynodered nodered/node-red

http://localhost:1880/

docker attach mynodered
docker start mynodered
docker stop mynodered


# arm
docker run -it -p 1880:1880 -v node_red_data:/data --name mynodered nodered/node-red:1.2.0-10-arm32v6


##

$ docker exec -it mynodered /bin/bash
bash-4.4$ npm install node-red-dashboard
bash-4.4$ exit
$ docker stop mynodered
$ docker start mynodered

# Multiple Instances

docker run -d -p 1880 nodered/node-red

# Linking Containers

docker network create iot
docker run -itd --network iot --name mybroker eclipse-mosquitto mosquitto -c /mosquitto-no-auth.conf

## Links
- https://nodered.org/docs/getting-started/docker
- https://github.com/itirohidaka/NodeRed
