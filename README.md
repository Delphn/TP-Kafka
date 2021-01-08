

# TP Intergiciel

- Lancer le serveur zookeeper et un broker
```
cd kafka
bin/zookeeper-server-start.sh config/zookeeper.properties
bin/kafka-server-start.sh config/server.properties
```

## Commandes pour créer les topics
1. Topic1
```
bin/kafka-topics.sh --zookeeper localhost:2181 \
--create \
--replication-factor 1 \
--partitions 1 \
--topic Topic1
```
2. Topic2
```
bin/kafka-topics.sh --zookeeper localhost:2181 \
--create \
--replication-factor 1 \
--partitions 1 \
--topic Topic2
```
3. Topic3
```
bin/kafka-topics.sh --zookeeper localhost:2181 \
--create \
--replication-factor 1 \
--partitions 1 \
--topic Topic3
```

## Commande pour creer le user, pswd, database, ...
https://developer.okta.com/blog/2018/12/13/build-basic-app-spring-boot-jpa

- Interaction through the console or a simple web page (not mandatory)

TODO:
1. Producteur kafka pour interroger COVID19 API
2. Consomateur kafka qui recupere les donnees depuis Topic 1
  - Don't modify the json file that you get from the API
  - Store data in JSONB format



Spring Boot with PostgreSQL Example: https://www.javaguides.net/2019/08/spring-boot-spring-data-jpa-postgresql-example.html
```
# switch to the postgres account
sudo -i -u postgres

# switch to postgres command line
psql

# Create a database
create dabase [db-name]

# switch to covid19 database
\c covid19
```

### Connect to database in pgAdmin
password: Pa$$w0rd!  
object => create => server  
- In General fill in name, and in connection give configuration from springboot properties

### Some useful sql commands
```
# 
```