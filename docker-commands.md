# Commands

<br/>

### create docker network

```
docker network create mongo-network
```

<br/>

### start mongodb server

```
docker run -dp 27017:27017 \
-e MONGO_INITDB_ROOT_USERNAME=mongoadmin \
-e MONGO_INITDB_ROOT_PASSWORD=secret \
--net mongo-network \
--name mongodb \
-v mongo-data:/data/db \
--restart=always \
mongo
```

<br/>

### start mongo express

```
docker run -dp 8081:8081 \
-e ME_CONFIG_MONGODB_SERVER="mongodb" \
-e ME_CONFIG_MONGODB_ADMINUSERNAME="mongoadmin" \
-e ME_CONFIG_MONGODB_ADMINPASSWORD="secret" \
-e ME_CONFIG_BASICAUTH_USERNAME="root" \
-e ME_CONFIG_BASICAUTH_PASSWORD="secret" \
--name mongo-express \
--network mongo-network \
mongo-express
```
