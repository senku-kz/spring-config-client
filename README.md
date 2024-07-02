# Getting Started

##

## usefull links:

https://howtodoinjava.com/spring-cloud/spring-cloud-config-server-git/

https://docs.spring.io/spring-cloud-config/docs/current/reference/html/#_environment_repository

https://habr.com/ru/companies/otus/articles/590761/
Information about /actuator/refresh

### The HTTP service has resources in the following form:

/{application}/{profile}[/{label}]

/{application}-{profile}.yml

/{label}/{application}-{profile}.yml

/{application}-{profile}.properties

/{label}/{application}-{profile}.properties


### For example:

curl localhost:8888/foo/development

curl localhost:8888/foo/development/master

curl localhost:8888/foo/development,db/master

curl localhost:8888/foo-development.yml

curl localhost:8888/foo-db.properties

curl localhost:8888/master/foo-db.properties


where application is injected as the spring.config.name in the SpringApplication (what is normally application in a regular Spring Boot app), profile is an active profile (or comma-separated list of properties), and label is an optional git label (defaults to master.)
