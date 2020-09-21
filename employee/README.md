# employee-producer

Docker Steps:
docker image build -t employee-producer .
docker container run --name producer -p 8080:8080 -d employee-producer

Logs
docker container logs producer

URL: localhost:8080/employee


