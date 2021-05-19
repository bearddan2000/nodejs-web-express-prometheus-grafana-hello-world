# nodejs-web-express-prometheus-grafana-hello-world

## Description
Another way to serve web content.
Uses prometheus to track visitors
and grafana to visualize low level
metrics.

To see a graph of visitors:
- Nav to http://localhost:81
- Classic UI
  - Click Graph tab
    - Search: 'server_visits_count'
    - Duration 1m

For health check:
- Nav to http://localhost:81
- Targetes

To see dashboards:
- Nav to http://localhost:82
- Login with `admin/admin`
- configuration -> datasources
  - Select Prometheus
    - dashboards
      - import and click label

## Tech stack
- nodejs
- prometheus

## Docker stack
- node:latest
- prom/prometheus:latest
- grafana/grafana

## To run
`sudo ./install.sh -u`
- Available http://localhost
- App metrics http://localhost/metrics
- Prometheus console http://localhost:81
- Grafana dashboards http://localhost:82
  - Login with `admin/admin`

## To stop
`sudo ./install.sh -d`

## For help
`sudo ./install.sh -h`

## Credit
- https://dev.to/farnabaz/monitor-your-application-with-prometheus-2886
