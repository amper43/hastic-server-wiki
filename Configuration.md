You can configure hastic-server using either *environment variables* or *config file*.

## Config variables priority
Config variables have follow priority, from higher to lower:
- environment variables
- variables from config file

## Environment variables
You can export the following environment variables for hastic-server to use:
- `HASTIC_API_KEY` - (required) API-key of your Grafana instance (e.g. `eyJrIjoiVjZqMHY0dHk4UEE3eEN4MzgzRnd2aURlMWlIdXdHNW4iLCJuIjoiaGFzdGljIiwiaWQiOjF9`), see [Get-HASTIC_API_KEY](https://github.com/hastic/hastic-server/wiki/Get-HASTIC_API_KEY)
- `GRAFANA_URL` - (optional) Grafana URL which can be queried from hastic-server host (e.g. `http://localhost:3000`),
- `HASTIC_PORT` - (optional) port you want to run server on, default: `8000`
- `HASTIC_WEBHOOK_URL` - (optional) use it if you want to get webhooks with new detections (e.g.`http://localhost:8080`),
- `HASTIC_WEBHOOK_TYPE`: (optional) can be either `application/x-www-form-urlencoded` or `application/json`,

e.g.
```bash
export HASTIC_API_KEY=eyJrIjoiVjZqMHY0dHk4UEE3eEN4MzgzRnd2aURlMWlIdXdHNW4iLCJuIjoiaGFzdGljIiwiaWQiOjF9
export HASTIC_PORT=8080
export GRAFANA_URL=http://localhost:3000
```

### docker-compose .env file
You can also set those variables in `.env` file if you're using `docker-compose`
`.env` file example:
```
HASTIC_API_KEY=eyJrIjoiVDRUTUlKSjJ5N3dYTDdsd1JyWWRBNHFkb0VSeDBNTTYiLCJuIjoiaGFzdGljLXNlcnZlciIsImlkIjoxfQ==
GRAFANA_URL=http://localhost:3000
```

This variables will be set as environment variables and will have highest priority.
Note: variable from `.env` file will be applyed only if `docker-compose.yml` have variable name in `services.server.environment` section. Example for `ZMQ_CONNECTION_STRING` from Hastic's [docker-compose.yml](https://github.com/hastic/hastic-server/blob/master/docker-compose.yml):
```
    environment:
      ZMQ_CONNECTION_STRING: ${ZMQ_CONNECTION_STRING:-tcp://analytics:8002}
```

### Config file
You can also rename `config.example.json` to `config.json` and set your values there.
hastic-server config example: https://github.com/hastic/hastic-server/blob/master/config.example.json

### Data base configuration
`HASTIC_DB_CONNECTION_TYPE` set database connection type and can have follow values:
`nedb` - will be used local storage in files and `NeDB` as data base
`mongodb` - will be used remote MongoDB as data base

`HASTIC_DB_CONNECTION_STRING` set string for connection with MongoDB.
Format is follow: `<db_user>:<db_password>@<db_url>/<db_name>`. For example `hastic:password@mongodb.example.com:27017/hastic`:
- username: hastic
- password: password
- mongodb url: mongodb.example.com:27017
- database: hastic
