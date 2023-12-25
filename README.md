# Containership 
This project is an Container Network Autoconfiguration project designed to provide network abstraction with users who don't know container network system. 

In this projects, our system connects different docker netwokrs using OpenFlow Protocol. to do it, first we mapped docker network with OVS Switch and add flow rule based on IP-address using SDN Controller(ONOS)

users don't have to know container network(=docker network) because of group system(=network abstraction system). they only need to know two information.
1. containers of same group can communicate with each other
2. to connect containers of different group, they just request our system


The diagram below represents the conceptual overview of our project.
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



# Project Design Overview
when designing, we devided our system into three pieces. each one is component of our systems. you can access detailed information through our submodule repository.
1. MainConfigHandler: coordinate switch environment and container environment
2. SwitchConfigHandler: control switch environment. ex) connect container
3. DockerConfigHandler: control docker environment. ex) deploy container

The following is overview of class diagram and sequece diagram corresponding to each use case






# REST API Interface



