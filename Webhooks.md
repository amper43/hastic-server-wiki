
It's possible to get notifications about detection of patterns / anomalies via [WebHooks](https://en.wikipedia.org/wiki/Webhook)

You need to set variables (whether in `config.json` or as environment variables):
- `HASTIC_WEBHOOK_URL` with your endpoint which expects `POST` requests
- `HASTIC_WEBHOOK_TYPE` which can be:
  - `application/x-www-form-urlencoded` (default) - payload will be sent as form parameters
  - `application/json` - payload will be sent in request body as json


Payload example
```json
{
    analyticUnitName: 'cpu_peaks',
    from: 1544135000,
    to: 1544138330
  };
```
