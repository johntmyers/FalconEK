# FalconEK

Elastic Search and Kibana with Falcon API Frontend (Soon...)

This just spins up a basic Elastic Search and Kibana 5.0 cluster with no API ingest yet.

# Startup

`$ sudo docker-compose up --build -d`

It may take a few minutes.

Once it is up and running, you can access Kibana at `localhost:5601` in your browser.

Login: `elastic // changeme`

ES and Kibana are only accessible via localhost on the docker host.

## Startup Errors

If ES does not start up properly, try running `docker-compose` without the `-d` option.

If you see something like `max virtual memory areas vm.max_map_count [65530] likely too low, increase to at least [262144]`

Then running `sysctl -w vm.max_map_count=262144` should resolve the issue.

# Shutdown

`$ sudo docker-compose down`

# Storage

ES storage is in a docker volume called esdata, by default docker stores this at `/var/lib/docker/volumes`.

This data will persist across container restarts. It can be modified by changing `docker-compose.yml`
