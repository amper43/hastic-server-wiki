# Linux

**Work in progress: need final example for binary installation**

```bash
wget https://github.com/hastic/hastic-server/releases/latest/download/hastic-server-0.5.0
chmod +x hastic-server-0.5.0
./hastic-server-0.5.0
```

# Docker

Server and analytics processes work in separate docker containers. There are several ways to run them which are listed here.

***
### Important
NOTE: if you have Grafana and Hastic running on the same host, use your host IP (e.g. `http://192.168.0.1:3000` instead of `http://localhost:3000` / `http://127.0.0.1:3000`) when opening Grafana in browser. Otherwise Hastic will try to find Grafana inside Docker container and fail.
***

## Run via docker-compose

You can use [docker-compose](https://docs.docker.com/compose/) setup for more useful and declarative management of containers. For this you need `docker-compose.yml` file that contains services configuration and `.env` file that contains variables default values which are placed here:  
* [docker-compose.yml](https://github.com/hastic/hastic-server/blob/master/docker-compose.yml)  
* [.env](https://github.com/hastic/hastic-server/blob/master/.env)  

These files should be placed in one folder.

How to get `HASTIC_API_KEY` is described [here](https://github.com/hastic/hastic-server/wiki/Get-HASTIC_API_KEY).

Configuration process is described [here](https://github.com/hastic/hastic-server/wiki/Configuration#docker-compose-env-file)

```bash
export HASTIC_API_KEY=<your_grafana_api_key>
# to run Hastic with internal nedb DB
docker-compose up -d
# to run Hastic along with MongoDB
docker-compose up -d -f docker-compose-mongo.yml
```

## Run manually
```bash
docker run -d \
  --name hastic-analytics \
  -p 8002:8002 \
  hastic/analytics

docker run -d \
  --name hastic-server \
  -p 8000:8000 \
  -e HASTIC_API_KEY=<your_grafana_api_key> \
  -e ZMQ_CONNECTION_STRING=tcp://<analytics_ip>:8002\
  -v /some/host/path:/var/www/data \
  hastic/server
```

`ZMQ_CONNECTION_STRING` is the string which is used for connection between server and analytics. For docker-compose by default the value `tcp://analytics:8002` from `.env `file will be used. For manual setup use `tcp://<analytics_ip>:8002` with WAN IP (for example `192.168.0.1`).

Hastic uses TCP connection inside the Docker. If you want to increase performance use IPC in production mode as described in [Installation from source](https://github.com/hastic/hastic-server/wiki/Installation-from-source).

# RPM

## System requirements:
- CentOS 7 / RHEL 7

## Installation 
- `wget https://github.com/hastic/hastic-server/releases/latest/download/hastic-server-0.5.0.rpm`
- `sudo rpm -i hastic-server-0.5.0.rpm`

## Run:
- `sudo hastic-server`