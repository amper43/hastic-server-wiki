### Docker

#### Run via docker-compose

compose file:
`https://github.com/hastic/hastic-server/blob/master/docker-compose.yml`
`.env` file with default values (should be placed near docker-compose.yml)
`https://github.com/hastic/hastic-server/blob/master/.env`

How to get HASTIC_API_KEY described here: [Get HASTIC_API_KEY](#Get HASTIC_API_KEY)

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

NOTE: if you use grafana and hastic on one host, use real IP instead of localhost (or 127.0.0.1) when open Grafana in browser.

In docker hastic use tcp connection. If you want to increase performance use hastic with host's ipc (production mode, without docker) as described in [Linux](#linux).