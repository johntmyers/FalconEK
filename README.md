# FalconEK

Elastic Search and Kibana with Falcon API Frontend (Soon...)

This just spins up a basic Elastic Search and Kibana 5.0 cluster with no API ingest yet.

# Startup

`$ sudo docker-compose up --build -d`

It may take a few minutes.

Once it is up and running, you can access Kibana at `localhost:5601` in your browser.

Login: `elastic // changeme`

ES and Kibana are only accessible via localhost on the docker host.

# Shutdown

`$ sudo docker-compose down`

# Storage

ES storage is in a docker volume called esdata, by default docker stores this at `/var/lib/docker/volumes`.

This data will persist across container restarts. It can be modified by changing `docker-compose.yml`
