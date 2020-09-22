## employee

### producer url
localhost:8080/employee

### create docker network 
docker network create consumer-producer

### start the employee producer container on the newly created network.
docker container run --network consumer-producer --name producer -p 8080:8080 -d employee-producer

### start the employee consumer container on the newly created network.
docker container run --network consumer-producer --name consumer -d employee-consumer

## Other docker commands

### build 
docker image build -t employee-producer .
### run 
docker container run --name producer -p 8080:8080 -d employee-producer
### To stop
docker container stop producer
### To remove
docker container rm producer
### Logs
docker container logs producer
### list network
docker network ls

## docker-compose
### start all services using docker-compose
Go to consumer an run this: 
docker-compose up
1. If network employee-producer does not exist, it creates it. 
2. Starts container using image employee-producer  
3. Starts container using image employee-consumer


