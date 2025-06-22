# SpringBootTest
Testing Spring Boot Deployment to EBS

Ensure that the default route has content
HelloWorldController.java
@Controller
public class HelloWorldController {
    @RequestMapping(value = "/", method=RequestMethod.GET)
    @ResponseBody
    public String helloWorld(){
        return "Hello World !!";
    }
    
}


application.properties
Set server.port=5000 as thats the port EBS expects


IAM Role for EBS
https://us-east-1.console.aws.amazon.com/iam/home?region=us-east-1#/roles
Create role with AWSElasticBeanstalkCustomPlatformforEC2Role policy


Also be sure the VPC you deploy into has an internet gateway setup in the routing
table of the subnet you select.