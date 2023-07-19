# Base Components Template

## Copy Environments
```bash
# copy .env.example files
copy .env.example .env
```

## Docker-compose
```bash
# build
docker-compose build

# networks
docker network create --subnet=172.17.11.0/24 --gateway=172.17.11.1 --opt "com.docker.network.bridge.name"="back" back

# run
docker-compose up -d
```

