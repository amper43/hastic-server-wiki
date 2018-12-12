
It's possible to get notifications about new detection of patterns via [Webhooks](https://en.wikipedia.org/wiki/Webhook)

You need to set variables (whether in `config.json` or as environment variables):
- `HASTIC_WEBHOOK_URL` with your endpoint which expects `POST` requests
***
NOTE: if you have Hastic running in Docker and want to send webhooks to some service on localhost, use your host IP (e.g. `http://192.168.0.1:8000` instead of `http://localhost:8000` / `http://127.0.0.1:8000`). Otherwise Hastic will try to send webhook inside Docker container and fail.
***
- `HASTIC_WEBHOOK_TYPE` which can be:
  - `application/x-www-form-urlencoded` (default) - payload will be sent as form parameters
  - `application/json` - payload will be sent in request body as JSON


JSON Payload example
```json
{
  "analyticUnitName": "cpu_peaks",
  "from": 1544135000,
  "to": 1544138330
}
```

See [Webhooks](https://github.com/hastic/hastic-grafana-graph-panel/wiki/Webhooks) oh hastic-grafana-panel
