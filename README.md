# Elastic Beanstalk

In this hands-on exercise, you will use Elastic Beanstalk to deploy a web application to the cloud.

* By the end of this lab, you will be able to deploy a web application to the cloud using Elastic Beanstalk

Follow the exercise instructions described below:

### Step 1. Access Elastic Beanstalk service from AWS Management Console

From the AWS Management Console page, select the Elastic Beanstalk service.
            
 ![1](https://user-images.githubusercontent.com/94189602/221556080-22ced200-9ba5-4d7d-9769-0dc1925cab5f.PNG)
                        
                        Launch the default Create application wizard

* Use the Create Application wizard to create an application with the following configuration details:

|  Field	              |    Value                                        |
|  ---------------------- |    ------------------                           |
|  Application name       |    Your choice                                  |
|  Platform	              |    Tomcat                                       |
|                         |    Use the default Platform branch and version  | 
|  Application code       |    Sample application                           |

* It will create an environment for a sample application to run

## What is an environment?

An environment is the collection of AWS resources and permissions to allow your web application to run smoothly. The Elastic Beanstalk service manages the environment for us.

![2](https://user-images.githubusercontent.com/94189602/221560651-980942cc-d4e2-4af3-bce7-4c3a4667bb36.PNG)

![3](https://user-images.githubusercontent.com/94189602/221560660-63a52cba-924f-438a-b0e6-a77165397280.PNG)
                       
                       Create a sample web application, that will run on the Tomcat webserver

* Click the **Create application** button.
         
     **Note**: It will take about 10 minutes for your application, and its environment to be created.

* **Important** - Observe the logs shown on your dashboard to understand the resources that are spun up to support your application. While launching the environment and deploying EC2 instances to run your application, the following resources get created automatically:

* Amazon S3 storage bucket

* A target group in the default VPC

* Multiple security groups

* An autoscaling launch configuration and an autoscaling group

* Multiple EC2 instances

* Multiple CloudWatch alarms

* EC2 load balancer You can even see the logs of each event (success and failure) after the creation of the environment. See the snapshots below.

![4](https://user-images.githubusercontent.com/94189602/221562363-8cbed901-ebcc-46a4-bd73-07495266b5d2.PNG)

![5](https://user-images.githubusercontent.com/94189602/221562367-bc52bf31-f573-4170-a7dd-d756f9aa8ee9.PNG)

                        Events logs while creating the environment.
                        
* You can change the log-level to see more detailed information. The standard log-levels in any application are trace, debug, info, warn, error, and fatal.

* Your application is created once you see a green checkmark and the Health of your application as **Ok**.

![6](https://user-images.githubusercontent.com/94189602/221562916-c1b562cd-1583-436a-b019-923e57769269.PNG)
            
                                    A successfully deployed application.

* After the application is deployed successfully, copy the application’s URL that can be found against your application’s name, and paste it in a web browser like Chrome or Safari.

![7](https://user-images.githubusercontent.com/94189602/221562952-6dac7dc5-c75f-439c-ad22-a0d9121ea7be.PNG)

            **Congratulations**! You've deployed a sample application and learned about the resources that spun up automatically.
