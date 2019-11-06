## Configuration

Hastic can send alerts to [Prometheus Alertmanager](https://prometheus.io/docs/alerting/alertmanager/).
You need to set 2 variables in [config.json](https://github.com/hastic/hastic-server/wiki/Configuration):
- `HASTIC_ALERT_TYPE=alertmanager`
- `HASTIC_ALERTMANAGER_URL=<alertmanager_url>`

For example:
```js
// config.json
{
  //...
  "HASTIC_ALERT_TYPE": "alertmanager",
  "HASTIC_ALERTMANAGER_URL": "http://localhost:9093"
}
```

P.S. to configure your Alertmanager to send alerts to Telegram [see alertmanager-bot](https://github.com/metalmatze/alertmanager-bot#alertmanager-configuration).