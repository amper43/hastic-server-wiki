
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
  "analyticUnitName": "Anomaly_unit",
  "URL": "url_string",
  "Image": "image_url_string",
  "from": "Mon Oct 07 2019 16:51:00 UTC+03:00",
  "to": "Mon Oct 07 2019 16:53:00 UTC+03:00",
  "ID": "ID_string",
  "Message": "21 out of bound",
}
```
#### Timezone configuration (optional)
`TIMEZONE_UTC_OFFSET` set timezone for getting notifications. You need to set variables (whether in `config.json` or as environment variables):
Format: `<h>/<-h>:<mm>`. For example:
- `"TIMEZONE_UTC_OFFSET": "3:00"` - UTC+3:00
- `"TIMEZONE_UTC_OFFSET": "-2:30"` - UTC-2:30

If there is no field, server will be used default value equals your local timezone offset.


See [Webhooks](https://github.com/hastic/hastic-grafana-graph-panel/wiki/Webhooks) oh hastic-grafana-panel
