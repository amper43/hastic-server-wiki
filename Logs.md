How to see logs of:
- Hastic Server:
    - if it's installed from `.tar.gz` / RPM / source: logs can be seen in the terminal where you run `grafana-server`
    - if it's installed via `docker-compose`: `docker-compose logs` in hastic-server directory

- Grafana:
    - if it's installed from `.tar.gz`: logs can be seen in the terminal where you run `grafana-server`
    - if it's installed Grafana via RPM: `journalctl -u grafana-server`
