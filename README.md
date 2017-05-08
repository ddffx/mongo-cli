# Mongoshell, mongodump mongorestore

## Start the container
```
docker-compose up
```

### 
Start mongo shell
```
docker exec -it mongocli_app_1 mongo
```

### Export a database

```
docker exec -it mongocli_app_1 mongodump --host [x.x.x.x] --port [port] -d [db_name] -u [db_user] --out=/dbTmp/ --gzip
```
### Import it
```

docker exec -it mongocli_app_1 mongorestore --host [x.x.x.x] --port 27017 -d [db_name]  -u [db_user] --drop  --dir=/dbTmp/[db_name]  --gzip
```