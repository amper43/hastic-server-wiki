### Docker

#### Fetch image
```bash
docker pull hastic/server
```

#### Run
```bash
docker run -d \
  --name hastic-server \
  --ipc host \
  -p 80:8000 \
  -e HASTIC_API_KEY=<your_grafana_api_key> \
  -v /some/host/path:/var/www/data \
  hastic/server
```