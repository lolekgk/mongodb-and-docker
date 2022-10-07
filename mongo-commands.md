# Commands

<br/>

### get into container

```
docker exec -it mongodb-and-docker-mongodb-1 bash
```

<br/>

### open mongodb inside container as an admin

```
mongosh -u mongoadmin -p secret
```

<br/>

### switch to the new database

```
use test_db
```

<br/>

### insert documents into posts collection

```
db.posts.insertMany[{data1}, {data2}, {data3}]
```

<br/>

### insert documents into users_data collection

```
db.users_data.insertMany[{data1}, {data2}, {data3}]
```
