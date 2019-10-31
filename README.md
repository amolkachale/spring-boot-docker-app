# Spring-Boot-Docker-App

Spring boot application with docker as container engine.



# Step to create docker image and run container:-

 1. Go to project path and build the project using following command
 
   mvn clean install
           
   It create executable jar file in project path/target folder.
    
 2. Then run following command
 
   docker build -t spring-boot-docker-app:1.0.0 .
          
   It create docker image of name spring-boot-docker-app and tag 1.0.0 where tag is
   optional and default value is latest.
    
 3. Then run following command
    
   docker run -d --name spring-boot-docker-app -p 8081:8081 spring-boot-docker-app:1.0.0
          
   It create docker container of name spring-boot-docker-app.
 
 
# Step to test application

1. Call following GET REST API 

     http://localhost:8081/api/v1/test
     
  It will return following response with statusCode as 200 in response header.
     'Welcome to spring boot docker example'

  
