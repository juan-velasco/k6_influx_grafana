### Descargar el repo de git:

`git clone https://gitlab.iti.upv.es/acs/acs-devops/k6_influx_grafana.git`

### Arrancar el influx y el grafana (grafana puede consumir recursos):
Ir a la ruta donde se ha bajado el proyecto git.

`docker-compose up -d influxdb grafana`

### Acceder a grafana

http://localhost:3000

### Ejecutar los test con k6
`docker-compose run k6 run /scripts/single-request.js`

### Lanzar smoke test (un usuario / una iteración)
Si indicamos los VUs y el número de iteraciones se sobreescriben las opciones por defecto. 
También podemos utilizar un fichero de configuración (recomendado).

`docker-compose run k6 run /scripts/single-request.js --vus 1 --iterations 1`

`docker-compose run k6 run /scripts/single-request.js --config "/scripts/configs/smoke_test.json"`


