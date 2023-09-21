# Base Components Template

<div align="center">
    <img src="https://github.com/romanticlie/base-components/raw/master/docs/images/base-components.jpeg?raw=true" height="100" width="100" >
 </div>

## Include Components
```bash
Nginx,MySQL,Redis,Mongo,Apollo,RabbitMQ,Consul,Etcd,ElasticSearch,Kibana,Grafana,Jaeger,Minio,Kafka,Prometheus
```

## Copy Yml & Environments
```bash
# copy docker-compose.yml file
copy docker-compose.sample.yml docker-compose.yml
# copy .env file
copy .env.example .env
```

## Update Docker Settings 
`vim /etc/docker/daemon.json`
```json
{
    "bip": "172.17.10.1/24",
    "experimental": true,
    "features": {
        "buildkit": true
    }
}
```

## Docker-compose
```bash
# create networks 
docker network create --subnet=172.17.11.0/24 --gateway=172.17.11.1 --opt "com.docker.network.bridge.name"="back" back

# build
docker-compose build

# run
docker-compose up -d
```

