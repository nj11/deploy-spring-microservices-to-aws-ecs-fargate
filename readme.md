## Deployment of spring boot microservices to AWS fargate.



ECS ( Elastic Container Service ) was the first container orchestration tool offering by AWS. It essentially consists of EC2 instances which have docker already installed, and run a Docker container which talks with AWS backend


![Alt desc](https://github.com/nj11/deploy-spring-microservices-to-aws-ecs-fargate/blob/master/screenshots/screenshot1.png)

Fargate was the second service offering to come, and is intended to abstract all everything bellow the container (EC2 instances where they run) from you. In other words, a pure Container-as-a-Service, where you do not care where that container runs.

![Alt desc](https://github.com/nj11/deploy-spring-microservices-to-aws-ecs-fargate/blob/master/screenshots/screenshot2.png)
