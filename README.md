# Containership 
This project is an Container Network Autoconfiguration project designed to provide network abstraction with users who don't know container network system. 

In this projects, our system connects different docker netwokrs using OpenFlow Protocol. to do it, first we mapped docker network with OVS Switch and add flow rule based on IP-address using SDN Controller(ONOS)

users don't have to know container network(=docker network) because of group system(=network abstraction system). they only need to know two information.
1. containers of same group can communicate with each other
2. to connect containers of different group, they just request our system


The diagram below represents the conceptual overview of our project.

##### conceptual overview
<img width="960" alt="image" src="https://github.com/parkjumsun/Containership-superRepo/assets/126436201/80678a35-de2d-482a-8f92-8bf6d699d296">


# project environment
This project is implemented using spring MVC framework and RestTemplate library to send Rest API call to SDN Controller 
   - language: JAVA 17
   - framwork: Spring 3.2.1


# Features
simply, our system provide three features. and user can access our system through REST API Call
1. retrieve information: users can retrieve information of switch, group and container
2. connect containers: users just specify container's name that they want to connect, then our system will connect them 
3. deploy containers: it is possible to deploy container through our system. users just specify deployed container's information including container's name that they want to connect.
 
The following is the use case diagram for our project.

##### usecase diagram
<img width="419" alt="image" src="https://github.com/parkjumsun/Containership-superRepo/assets/126436201/3bd2de24-c34b-4ff8-9616-44b620a4129b">





# Project Design Overview
when designing, we devided our system into three pieces. each one is component of our systems. you can access detailed information through our submodule repository.
1. MainConfigHandler: coordinate switch environment and container environment
2. SwitchConfigHandler: control switch environment. ex) connect container
3. DockerConfigHandler: control docker environment. ex) deploy container

The following is component diagram and sequece diagram corresponding to each use case

##### component diagram
<img width="842" alt="image" src="https://github.com/parkjumsun/Containership-superRepo/assets/126436201/172fe630-9eca-4609-85d6-eb52d5ef4f5e">


##### sequence diagram
<img width="696" alt="image" src="https://github.com/parkjumsun/Containership-superRepo/assets/126436201/2b5be7d6-7f2f-4aff-86d8-f7f654362e41">

<img width="680" alt="image" src="https://github.com/parkjumsun/Containership-superRepo/assets/126436201/ff015074-65ca-4425-acf7-fd44b81db94d">

<img width="695" alt="image" src="https://github.com/parkjumsun/Containership-superRepo/assets/126436201/baa5c431-fd6e-4300-8716-5120f5ef26c0">

<img width="913" alt="image" src="https://github.com/parkjumsun/Containership-superRepo/assets/126436201/697efd31-34c8-4ec1-b72f-a5dc18578530">





# How to use REST API Call
1. Retrieve Switch information : get switch information from SDN Controller(ONOS)

<img width="383" alt="image" src="https://github.com/parkjumsun/Containership-superRepo/assets/126436201/58fa1322-9d13-4c04-a70d-5d3fbc2802e5">

Ex)
Request
<img width="383" alt="image" src="https://github.com/parkjumsun/Containership-superRepo/assets/126436201/fc97f257-376f-4887-b974-1a0941010cda">

<img width="397" alt="image" src="https://github.com/parkjumsun/Containership-superRepo/assets/126436201/80ea5b55-9072-4c91-9877-8a8bb4545169">




<img width="383" alt="image" src="https://github.com/parkjumsun/Containership-superRepo/assets/126436201/e194465f-cfa2-4c57-afa2-6ebbb7c85f56">

<img width="410" alt="image" src="https://github.com/parkjumsun/Containership-superRepo/assets/126436201/55564547-ca6a-46e7-8332-c869cd95ca99">

<img width="341" alt="image" src="https://github.com/parkjumsun/Containership-superRepo/assets/126436201/6176d2c5-911c-4914-8e8f-62976fb281eb">


![image](https://github.com/parkjumsun/Containership-superRepo/assets/126436201/a5de7e27-3111-4521-8184-33f0b3bf3347)

<img width="402" alt="image" src="https://github.com/parkjumsun/Containership-superRepo/assets/126436201/c4be5ae5-3787-447a-b36a-19ad2c10709c">

<img width="361" alt="image" src="https://github.com/parkjumsun/Containership-superRepo/assets/126436201/707169ac-f5a9-40cd-a919-71205844a046">


![image](https://github.com/parkjumsun/Containership-superRepo/assets/126436201/7a32b150-4cfa-49bd-ad72-85d8e5eda607)

<img width="405" alt="image" src="https://github.com/parkjumsun/Containership-superRepo/assets/126436201/e5cc8f8a-b6bf-434e-a27b-70796da2ae31">

<img width="388" alt="image" src="https://github.com/parkjumsun/Containership-superRepo/assets/126436201/249016b8-986f-4286-a280-185c10d89462">


![image](https://github.com/parkjumsun/Containership-superRepo/assets/126436201/a98a3587-a5ba-404e-b1df-b6c476ce93d9)

<img width="444" alt="image" src="https://github.com/parkjumsun/Containership-superRepo/assets/126436201/20abee42-3c7c-4d16-8da4-40d61c4a82be">


<img width="417" alt="image" src="https://github.com/parkjumsun/Containership-superRepo/assets/126436201/cb333584-e648-4594-bbdc-598e2307414d">









