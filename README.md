# Base Components Template

## Include Components
```bash
Nginx,MySQL,Redis,Mongo,Apollo,RabbitMQ,Consul,Etcd,ElasticSearch,Kibana
```

## Copy Yml & Environments
```bash
# copy docker-compose.yml.example file
copy docker-compose.yml.example docker-compose.yml
# copy .env.example file
copy .env.example .env
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

