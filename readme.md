***Sprintboot RHPAM Simple Process Example***

This is a small example to show a simple business process running on Springboot. 

The shell of the project was created here: <https://start.jbpm.org>

Relevant documentation and blog links :
* [Good blog by Duncan Doyle](https://developers.redhat.com/blog/2018/11/01/spring-boot-enabled-business-process-automation-with-red-hat-process-automation-manager/)

* [Official Documents](https://access.redhat.com/documentation/en-us/red_hat_process_automation_manager/7.2/html-single/creating_red_hat_process_automation_manager_business_applications_with_spring_boot/index)


##Getting Started
1. Git clone this repo
1. Navigate to the springboot-business-application-service folder
1. For docker run: ```./launch.sh clean install -Pdocker,h2```
1. This should have created a docker image. To check run the following command ```docker images```. You should see an entry named ```apps/springboot-business-application-service```.
1. Check a container is not already running using ```docker ps```
1. To start a container run the following command ```docker run <IMAGE ID>```
1. It should start up successfully and to check attempt to access the following url ```http://localhost:8090/rest/server/containers```. Hopefully you should a success response.
1. To create a new process instance you can use the following curl command ```curl -X POST \
  http://localhost:8090/rest/server/containers/springboot-business-application-kjar-1_0-SNAPSHOT/processes/org.demo.SampleCaseProcess/instances \
  -H 'Accept-Encoding: application/json' \
  -H 'Authorization: Basic a2llc2VydmVyOmtpZXNlcnZlcjEh' \
  -H 'Content-Type: application/json' \
  -H 'Postman-Token: 9a4edc30-bfaf-4108-86f6-724950fcb6cb' \
  -H 'cache-control: no-cache'```
