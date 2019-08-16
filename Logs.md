How to get logs:
- Hastic Server:
    - if you've installed it from `.tar.gz` / RPM / source: they can be seen in the terminal where you run `grafana-server`
    - if you've installed it via `docker-compose`: `docker-compose logs` in hastic-server directory

- Grafana logs:
    - if you've installed it from `.tar.gz`: they can be seen in the terminal where you run `grafana-server`
    - if you've installed Grafana via RPM: `journalctl -u grafana-server`
