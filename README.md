

# TP Intergiciel

- Lancer le serveur zookeeper et un broker
```
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

## Commande pour creer le user, pswd, database, ... en ligne de commande

```
# create user
create user [name]

# Give the user a password
alter user [name] with encrypted password '<really secure password>'

# switch to the postgres account
sudo -i -u postgres

# switch to postgres command line
psql

# Create a database
create database [db-name]

# switch to covid19 database
\c covid19
```

### Connect to database in pgAdmin
password: Pa$$w0rd!  
object => create => server  
- In General fill in name, and in connection give configuration from springboot properties

### SQL Commands used in the project from JPA repositories
```
@Query(value = "SELECT c FROM Countries c WHERE c.Country = :pays")

@Query("SELECT g.TotalDeaths FROM Global g")

@Query("SELECT g.TotalConfirmed FROM Global g")

@Query("SELECT g FROM Global g WHERE g.id = 1")
# 
```
