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
1. This should have created a docker image. To check run ```docker images```
