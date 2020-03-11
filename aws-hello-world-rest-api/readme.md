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


## Deploy to AWS Fargate cluster

* Attached are instructions and screenshots on how to create AWS Fargate cluster with a task definition that defines what container needs to run.In this case we will use the container we deployed to docker hub in the above step.

* We also define a service that specifies how many tasks to run.

* Finally we run the service on our browser using the public IP address available from the deployed service.


* SCREENSHOTS :

![Alt desc](https://github.com/nj11/deploy-spring-microservices-to-aws-ecs-fargate/blob/master/aws-hello-world-rest-api/screenshots/screenshot2.png)


![Alt desc](https://github.com/nj11/deploy-spring-microservices-to-aws-ecs-fargate/blob/master/aws-hello-world-rest-api/screenshots/screenshot3.png)


![Alt desc](https://github.com/nj11/deploy-spring-microservices-to-aws-ecs-fargate/blob/master/aws-hello-world-rest-api/screenshots/screenshot4.png)


![Alt desc](https://github.com/nj11/deploy-spring-microservices-to-aws-ecs-fargate/blob/master/aws-hello-world-rest-api/screenshots/screenshot5.png)


![Alt desc](https://github.com/nj11/deploy-spring-microservices-to-aws-ecs-fargate/blob/master/aws-hello-world-rest-api/screenshots/screenshot6.png)


![Alt desc](https://github.com/nj11/deploy-spring-microservices-to-aws-ecs-fargate/blob/master/aws-hello-world-rest-api/screenshots/screenshot7.png)


![Alt desc](https://github.com/nj11/deploy-spring-microservices-to-aws-ecs-fargate/blob/master/aws-hello-world-rest-api/screenshots/screenshot8.png)


![Alt desc](https://github.com/nj11/deploy-spring-microservices-to-aws-ecs-fargate/blob/master/aws-hello-world-rest-api/screenshots/screenshot9.png)


![Alt desc](https://github.com/nj11/deploy-spring-microservices-to-aws-ecs-fargate/blob/master/aws-hello-world-rest-api/screenshots/screenshot10.png)


![Alt desc](https://github.com/nj11/deploy-spring-microservices-to-aws-ecs-fargate/blob/master/aws-hello-world-rest-api/screenshots/screenshot11.png)


![Alt desc](https://github.com/nj11/deploy-spring-microservices-to-aws-ecs-fargate/blob/master/aws-hello-world-rest-api/screenshots/screenshot12.png)



![Alt desc](https://github.com/nj11/deploy-spring-microservices-to-aws-ecs-fargate/blob/master/aws-hello-world-rest-api/screenshots/screenshot13.png)



![Alt desc](https://github.com/nj11/deploy-spring-microservices-to-aws-ecs-fargate/blob/master/aws-hello-world-rest-api/screenshots/screenshot14.png)


![Alt desc](https://github.com/nj11/deploy-spring-microservices-to-aws-ecs-fargate/blob/master/aws-hello-world-rest-api/screenshots/screenshot15.png)


![Alt desc](https://github.com/nj11/deploy-spring-microservices-to-aws-ecs-fargate/blob/master/aws-hello-world-rest-api/screenshots/screenshot16.png)


![Alt desc](https://github.com/nj11/deploy-spring-microservices-to-aws-ecs-fargate/blob/master/aws-hello-world-rest-api/screenshots/screenshot17.png)


![Alt desc](https://github.com/nj11/deploy-spring-microservices-to-aws-ecs-fargate/blob/master/aws-hello-world-rest-api/screenshots/screenshot18.png)


![Alt desc](https://github.com/nj11/deploy-spring-microservices-to-aws-ecs-fargate/blob/master/aws-hello-world-rest-api/screenshots/screenshot19.png)


![Alt desc](https://github.com/nj11/deploy-spring-microservices-to-aws-ecs-fargate/blob/master/aws-hello-world-rest-api/screenshots/screenshot20.png)


![Alt desc](https://github.com/nj11/deploy-spring-microservices-to-aws-ecs-fargate/blob/master/aws-hello-world-rest-api/screenshots/screenshot21.png)


![Alt desc](https://github.com/nj11/deploy-spring-microservices-to-aws-ecs-fargate/blob/master/aws-hello-world-rest-api/screenshots/screenshot22.png)


![Alt desc](https://github.com/nj11/deploy-spring-microservices-to-aws-ecs-fargate/blob/master/aws-hello-world-rest-api/screenshots/screenshot23.png)


![Alt desc](https://github.com/nj11/deploy-spring-microservices-to-aws-ecs-fargate/blob/master/aws-hello-world-rest-api/screenshots/screenshot24.png)


![Alt desc](https://github.com/nj11/deploy-spring-microservices-to-aws-ecs-fargate/blob/master/aws-hello-world-rest-api/screenshots/screenshot25.png)


![Alt desc](https://github.com/nj11/deploy-spring-microservices-to-aws-ecs-fargate/blob/master/aws-hello-world-rest-api/screenshots/screenshot26.png)

![Alt desc](https://github.com/nj11/deploy-spring-microservices-to-aws-ecs-fargate/blob/master/aws-hello-world-rest-api/screenshots/screenshot27.png)


![Alt desc](https://github.com/nj11/deploy-spring-microservices-to-aws-ecs-fargate/blob/master/aws-hello-world-rest-api/screenshots/screenshot28.png)


![Alt desc](https://github.com/nj11/deploy-spring-microservices-to-aws-ecs-fargate/blob/master/aws-hello-world-rest-api/screenshots/screenshot29.png)


![Alt desc](https://github.com/nj11/deploy-spring-microservices-to-aws-ecs-fargate/blob/master/aws-hello-world-rest-api/screenshots/screenshot30.png)


![Alt desc](https://github.com/nj11/deploy-spring-microservices-to-aws-ecs-fargate/blob/master/aws-hello-world-rest-api/screenshots/screenshot31.png)

![Alt desc](https://github.com/nj11/deploy-spring-microservices-to-aws-ecs-fargate/blob/master/aws-hello-world-rest-api/screenshots/screenshot32.png)


![Alt desc](https://github.com/nj11/deploy-spring-microservices-to-aws-ecs-fargate/blob/master/aws-hello-world-rest-api/screenshots/screenshot33.png)
