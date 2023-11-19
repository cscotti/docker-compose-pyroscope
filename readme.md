# Intro
Pyroscope with grafana via docker-compose

## Start docker-compose

```
docker-compose up
```

# Open url
Pyroscope<br>
<http://localhost:4040><br>
Grafana<br>
<http://localhost:3000/>

# Divers

## Force docker restart

```
docker-compose down -v --rmi all --remove-orphans
docker rm $(docker ps -a -q)
docker rmi $(docker images -q)
docker volume rm $(docker volume ls -q)

docker-compose up
```

## Sources
<https://grafana.com/docs/grafana/latest/datasources/grafana-pyroscope/><br>
<https://github.com/grafana/pyroscope/tree/main/examples/python/simple><br>
<https://grafana.com/docs/pyroscope/latest/configure-client/language-sdks/python/><br>
<https://stackoverflow.com/questions/40157756/docker-compose-volumes-not-mounting-to-host-directories><br>
<https://stackoverflow.com/questions/76973441/connect-pyroscope-to-grafana-datasource-using-yaml-config-files-and-docker-comp><br>
<https://pyroscope.io/blog/visualize-flamegraphs-in-grafana/>