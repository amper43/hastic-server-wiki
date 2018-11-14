### Docker

Server and analytics processes work in separate docker containers. There are several ways to run them which are listed here.

#### Run via docker-compose

 You can use [docker-compose](https://docs.docker.com/compose/) setup for more useful and declarative management of containers. For this you need `docker-compose.yml` file that contains services configuration and `.env` file that contains variables default values which are placed here:  
* [docker-compose.yml](https://github.com/hastic/hastic-server/blob/master/docker-compose.yml)  
* [.env](https://github.com/hastic/hastic-server/blob/master/.env)  

These files should be placed in one folder.

How to get `HASTIC_API_KEY` is described [here](https://github.com/hastic/hastic-server/wiki/Get-HASTIC_API_KEY).

```bash
export HASTIC_API_KEY=<your_grafana_api_key>
docker-compose up -d
```

#### Run manually
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

NOTE: if you use Grafana and Hastic on one host, use your host IP (e.g. `http://192.168.0.1:3000` instead of `http://localhost:3000` / `http://127.0.0.1:3000`) when opening Grafana in browser. Otherwise Hastic will try to find Grafana inside Docker container and fail.

`ZMQ_CONNECTION_STRING` is the string which is used for connection between server and analytics. For docker-compose by default the value `tcp://analytics:8002` from `.env `file will be used. For manual setup use `tcp://<analytics_ip>:8002` with WAN IP (for example `192.168.0.1`).

In Docker, Hastic uses TCP connection. If you want to increase performance use IPC in production mode as described in [Installation from source](https://github.com/hastic/hastic-server/wiki/Installation-from-source).