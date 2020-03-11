# Hello World Rest API

- Main class RestfulWebServicesApplication 
- You cannot run this app on local as it is configured to run on port 80 . 
- You can run it as a docker container as shown below

## Pre-requisites

* Install maven
* Install docker desktop

* Make sure docker destop is running.

* On docker desktop,navigate to settings => general.Make sure the "Expose daemon on tcp without TLS checkbox is checked as in screensot below"

  ![Alt desc](https://github.com/nj11/deploy-spring-microservices-to-aws-ecs-fargate/blob/master/aws-hello-world-rest-api/screenshots/screenshot1.png)
  
* Restart docker desktop

* Create docker hub account login 
 
    ```https://hub.docker.com/```

* Create docker hub repository

### Creating Containers

* Run the below commands in the same order

```
   cd  aws-hello-world-rest-api
   mvn clean package
```

* @@REPO@@ needs to be substituted with your repository name in docker hub

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

