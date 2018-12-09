# Nuit info 2018

Ce repository contiens un ensemble de fichier `docker-compose` pour ces deux projets : 
* [Le front end](https://front-lost-nuit-info.netlify.com/), voir le [repo](https://github.com/LesBoa/front_app)
* [Le back end](https://lost-backend-nuit-info.herokuapp.com), voir le [repo](https://github.com/LesBoa/night-back)


Il y a deux setup possible de docker compose : 

* La version "simple"
* La version "complète"

La version simple contiens seulemnet l'app, le server et la base de données.


La version complète viens avec : 
* [Traefik](https://traefik.io/)
* [Grafana](https://grafana.com/)
* [Prometheus](https://prometheus.io/)
* [node-exporter](https://github.com/prometheus/node_exporter)
* [alertmanager](https://github.com/prometheus/alertmanager)
* [cadvisor](https://github.com/google/cadvisor)
* Plus l'application.

## Version simple

Pour la version simple, pour le démarer vous devez faire :

```bash
docker-compose up -d
```

Et vous trouverez sur ces urls les choses suivantes : 
* http://localhost:8090 le client
* http://localhost:3030 le server

## Version complète 

Pour la version complète, pour la démarer, vous devez faire : 

```bash
docker-compose -f docker-compose.prod.yml up -d
```

et vous trouverez sur ces urls les choses suivantes : 

* http://app.lost.docker.localhost le client
* http://api.lost.docker.localhost le server
* http://traefik.docker.localhost le traefik
* http://prometheus.docker.localhost le prometheus
* http://node-exporter.docker.localhost le node-exporter
* http://alertmanager.docker.localhost l'alert manager
* http://cadvisor.docker.localhost le cAdvisor
* http://grafana.docker.localhost le grafana

Pour les logins sur Grafana, les logins de base sont admin/foobar

Pour les logins des sites traefik, prometheus, node-exporter, alert manager et cAvisor, les logins sont admin/foobar.
