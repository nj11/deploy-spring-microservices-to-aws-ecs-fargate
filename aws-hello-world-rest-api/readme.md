# Hello World Rest API

- Main class RestfulWebServicesApplication 
- You cannot run this app on local as it is configured to run on port 80 . 
- You can run it as a docker container as shown below

## Pre-requisites

* Install maven
* Install docker desktop

![Alt desc](https://github.com/nj11/spring-microservices-on-aws-fargate/aws-hellopworld-rest-api/blob/master/screenshots/screenshot2.png)

* Create docker hub account login
* Create docker hub repository

### Creating Containers

```
   mvn clean package
```

```
  docker login
  docker push @@REPO@@/aws-hello-world-rest-api-1.0.0-RELEASE
```

```
docker run --publish 8200:80 @@REPO@@:aws-hello-world-rest-api-1.0.0-RELEASE
```


## Test URLs

- http://localhost:8200/hello-world

```txt
Hello World
```

- http://localhost:8200/hello-world-bean

```json
{"message":"Hello World - Changed"}
```

- http://localhost:8200/hello-world/path-variable/test

```json
{"message":"Hello World, test"}
```

