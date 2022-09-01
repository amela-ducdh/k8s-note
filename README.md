# Install MongoDB

https://www.digitalocean.com/community/tutorials/how-to-install-mongodb-on-ubuntu-20-04

# DB

```
sudo systemctl start mongod.service
npm run mongodb -- --dbpath ./data/db
```

# Docker

```
docker network create knote

docker run \
  --name=mongo \
  --rm \
  --network=knote mongo

docker run \
  --name=knote \
  --rm \
  --network=knote \
  -p 3000:3000 \
  -e MONGO_URL=mongodb://mongo:27017/dev \
  knote  
```

