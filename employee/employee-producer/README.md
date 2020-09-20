# dockerdemo
Just a basic docker Springboot application

To run as a Spring boot app, 
1) Maven clean
2) Maven install
3) Run as a Spring Boot App (From STS)

For Docker:
1) Ensure Docker is installed. 
2) Go to project folder 
3) docker build -f DockerFile -t dockerdemo .
4) docker run -p 8080:8080 dockerdemo

To validate: use http://localhost:8080/name
