# SpringBootTest
Testing Spring Boot Features & Deployment to EBS


application.properties
Set server.port=5000 as thats the port EBS expects


IAM Role for EBS
https://us-east-1.console.aws.amazon.com/iam/home?region=us-east-1#/roles
Create role with AWSElasticBeanstalkCustomPlatformforEC2Role policy


Also be sure the VPC you deploy into has an internet gateway setup in the routing
table of the subnet you select.