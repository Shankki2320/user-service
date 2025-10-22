#This document highlights the feature-wise pushes to the repo

1. First feature added is: user-service registers itself as Service Discovery Client
- We need the dependency of eureka-client, sb-starter-web, actuators and spring cloud dependency management
- No need to explicitly mark Main class with @EnableEurekaClient or @EnableDiscoveryClient
- Add configurations in application.properties file for :

eureka.client.service-url.defaultZone=http://localhost:8761/eureka/
eureka.client.register-with-eureka=true
eureka.client.fetch-registry=true
eureka.instance.prefer-ip-address=true

eureka.instance.health-check-url-path= /actuator/health