### Arrancar el influx y el grafana (grafana puede consumir recursos):

`docker-compose up -d influxdb grafana`

### Ejecutar los test con k6
`docker-compose run k6 run /scripts/single-request.js`