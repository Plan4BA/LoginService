# Loginserice
Microservice to authenticate against Campus Dual and return userspecific content
## deployment
### requirements
- Docker (Linux Kernel 3.10 oder Hyper-V Virtualization under Windows)[https://docs.docker.com/install/]
- recommendation: docker-compose[https://docs.docker.com/compose/install/]
### docker run 

``
docker run -d --rm --name loginservice -p 8080:8080 loginservice  
``
### docker compose

```yaml
version: 3
services:
    loginservice:
        container_name: loginservice
        ports:
            - '8080:8080'
        image: loginservice
```
## development
### requirements    
- Docker & Docker compose(see deployment)
- Java(OpenJDK > 11)
- Maven 3
### build
build the executable JAR-Files
```bash
mvn clean package
```
building docker container:
```bash
docker build -t loginservice .
```





