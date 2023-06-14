# NodeJS-Express-Mongodb-CRUD-API

IMPORTANT: 
In the docker-compose.yml file leave in blank in username and password

1.Create this file in VSCode in a separate blank project
docker-compose.yml

```yaml
version: "3.3"

services:
 mongodb:
   image: mongo:latest
   container_name: mongodb
   environment:
    MONGO_INITDB_ROOT_USERNAME: 
    MONGO_INITDB_ROOT_PASSWORD: 
   ports:
    - 27017:27017
   volumes:
    - .dbmongodb:/var/lib/lib/mongodb
```

2.To run the MondDb container run the command: docker-compose up

3.Run MondoDb Compass and connect to the MongoDb docker container
Set the connection string: mongodb://localhost:27017

NOTE: in case we set a username and password for the MondDb container
use this connection string: mongodb://admin:admin@localhost:27017

4.Create a new database and a new collection.

Database name: nodejs
Collection name: home

5.To run the application in the VSCode run the command:

npm run dev 
or
npm run dev -- -p 8081

6.To visualize Swagger paste the URL in the internet web browser:
http://localhost:8081/api-docs

