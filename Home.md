# About

Hastic is a software for detecting patterns and anomalies. It helps to improve monitoring systems in fields like manufacturing, energy, cyber-security, telecommunications, and financial trading. Hastic integrates with many monitoring platforms and its functionality can be extended.

Use case: In telecommunication field, improvement of equipment monitoring system helps operators to react faster and more precisely.

## Technology
Hastic is open source and licenced under Apache 2.0 [License](https://github.com/hastic/hastic-server/blob/master/LICENSE), with source code available on GitHub. For backend ([hastic-server](https://github.com/hastic/hastic-server)) used Python and Node.js. Hastic application for [Grafana](https://grafana.com/): ([hastic-grafana-app](https://github.com/hastic/hastic-grafana-app)) for interacting with the backend application. Hastic could be used without Grafana via API.

Hastic queries Grafana to get data from datasoures: InfluxDB, Prometheus, Graphite, ElasticSearch, postgreSQL. Hastic has its own database for storing detections. Deployment is possible on Mac, Linux, and Windows. Go to downloads for more info.

# Getting started

Hastic consist of two main parts: server and client applications, you should install both parts.

## Install server
  * [Binary](https://github.com/hastic/hastic-server/wiki/Installation-from-binary)
  * [Linux](https://github.com/hastic/hastic-server/wiki/Installation-in-Linux)
  * [Docker](https://github.com/hastic/hastic-server/wiki/Docker)
  * [RPM](https://github.com/hastic/hastic-server/wiki/Installation-from-RPM)
## Install client
  * [Install hastic-grafana-app](https://github.com/hastic/hastic-grafana-app/wiki/Installation)
  * [Connect hastic-grafana-app to hastic-server](https://github.com/hastic/hastic-grafana-app/wiki/Getting-started)
  * [Setup hastic-server config to connect to Grafana](https://github.com/hastic/hastic-server/wiki/Configuration)


### See also:
* [FAQ](https://github.com/hastic/hastic-server/wiki/FAQ)
* [hastic-grafana-graph-panel wiki](https://github.com/hastic/hastic-grafana-graph-panel/wiki) if you use [Grafana](https://grafana.com/)