# Marketer app
## Development environment
### Cassandra
To run Cassandra in docker use following commands

* _docker network create app-tier --driver bridge_
* _docker run -d -p 9042:9042 --name cassandra-server --network app-tier bitnami/cassandra:latest_

To access cqlsh use following command:
_docker run -it --rm --network app-tier bitnami/cassandra:latest cqlsh --username cassandra cassandra-server_

To upload sample data:

_insert into client(id, address, age, email, name) values (551, 'Address 1', 10, 'email1@dot.com', 'Client name 1'); <br>
insert into client(id, address, age, email, name) values (552, 'Address 2', 12, 'email22@dot.com', 'Client name 2');_

### Application dev env

Just import maven project intp your IDE  