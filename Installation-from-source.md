## Build & run from source 

Hastic server requires Grafana's API key (http://<your_grafana_url>/org/apikeys) to query data from Grafana datasources.
API key role requires only `Viewer` access. 

Possible to install on:

* [Linux](#linux)
* [Docker](#docker)

### Linux

#### System prerequisites:

* [git](https://git-scm.com/download/linux)
* [nodejs >= 6.14](https://nodejs.org/en/download/package-manager/#debian-and-ubuntu-based-linux-distributions)
* [python == 3.6.х](https://www.python.org/downloads/) with [pip3](https://packaging.python.org/guides/installing-using-linux-tools/#installing-pip-setuptools-wheel-with-linux-package-managers)

#### Installation
```bash
git clone https://github.com/hastic/hastic-server.git
cd hastic-server
pip3 install -r analytics/requirements.txt
cd server
npm install
npm run build
```

#### Configuration

You can configure hastic-server using either *environment variables* or *config file*.

> NOTE: environment variables have higher priority than config file.

##### Environment variables
You can export the following environment variables for hastic-server to use:
- HASTIC_API_KEY - (required) API-key of your Grafana instance
- HASTIC_PORT - (optional) port you want to run server on, default: 8000

e.g.
```bash
export HASTIC_API_KEY=eyJrIjoiVjZqMHY0dHk4UEE3eEN4MzgzRnd2aURlMWlIdXdHNW4iLCJuIjoiaGFzdGljIiwiaWQiOjF9
export HASTIC_PORT=8080
```

##### Config file
You can also rename `config.example.json` to `config.json` and set your values there.

#### Run
```bash
cd hastic-server/server
npm start
```

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
  -v /tmp:/tmp \
  hastic/server
```