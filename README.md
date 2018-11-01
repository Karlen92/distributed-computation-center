# Distributed Computation Center

Software package intended for research teams, for distributed computations. Software at current version supports computations that has sequental nature. Software supports unlimited number of participants, that can request at anytime. All requests will be placed into queue, and executed in the order they arived. From here can be infered the the what kind of models can be computed by this software package. That is, only models which has state at every given moment, and can be updated at any given step, regardless of requests waiting in queue. Neverthless, this is the default behaviour expected from software, and there is freedom to design the application is a way, so it can be used for parallel and no sequental models. Sequental modeling is available off-the-shelf.

System provides logging available in server, where the software is running. Logging is done by using [ELK](hhttps://www.elastic.co/elk-stack) stack, which means logs are visualized by [Kibana](https://www.elastic.co/products/kibana). To have easy experience with environment we've wrapped the software into [Docker](https://www.docker.com/) containers, which is known enterprise container platform. This gives freedom to operate with any operating system without infrastructure lock-ins. Allis need for application to work as docker container is Docker Community Edition. 

Requirements: [Docker Community Edition](https://www.docker.com/community-edition)

To start the app run: `docker-compose up`.

To start the app in background run: `docker-compose up -d`.

It will then be started on port 3000.

# Endpoints

## Default Behavior

```sh
runing on http://localhost:3000
```

## Default methods when extending from provided main class
```sh
 HTTP:GET /toJson returns json of the model
```
```sh
 HTTP:GET /export returns model as encrypted string
```
```sh
 HTTP:POST /fromJson recovers model from given json
```
```sh
 HTTP:POST /import recovers model from given encrypted string
```
