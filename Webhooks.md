
It's possible to get notifications about new detection of patterns via [Webhooks](https://en.wikipedia.org/wiki/Webhook)

You need to set variables (whether in `config.json` or as environment variables):
- `HASTIC_WEBHOOK_URL` with your endpoint which expects `POST` requests
***
NOTE: if you have Hastic running in Docker and want to send webhooks to some service on localhost, use your host IP (e.g. `http://192.168.0.1:8000` instead of `http://localhost:8000` / `http://127.0.0.1:8000`). Otherwise Hastic will try to send webhook inside Docker container and fail.
***
- `HASTIC_WEBHOOK_TYPE` which can be:
  - `application/x-www-form-urlencoded` (default) - payload will be sent as form parameters
  - `application/json` - payload will be sent in request body as JSON

#### Webhook image (optional)
Webhooks can contain a panel screenshot with detected segments if you set `HASTIC_ALERT_IMAGE` to `true`. Default value: `false`

#### Timezone configuration (optional)
`TIMEZONE_UTC_OFFSET` configuration variable sets the timezone for getting notifications.
Format: `[-]<h>:<mm>`. For example:
- `"TIMEZONE_UTC_OFFSET": "3:00"` - UTC+3:00
- `"TIMEZONE_UTC_OFFSET": "-2:30"` - UTC-2:30

If `TIMEZONE_UTC_OFFSET` is not set, server will use your local timezone offset.
