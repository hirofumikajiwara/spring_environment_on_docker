# spring_environment_on_docker

## Objective

* Be able to develop spring boot web with localhost postgresql on docker on windows 11.
* Be able to access with vscode remote development.

## Procedure

1. install WSL on windows.
2. install ubuntu on WSL.
3. install docker on ubuntu.
4. install vscode on windows.
5. install remote-WSL on vscode on windows.
6. install remote development extension on vscode on windows.
7. install docker extension on vscode on ubuntu.
8. git pull this files to a directory on ubuntu.
9. make directory project and postgres.
10. add authority all to project directory.
11. compose up docker-compose.yml on ubuntu.
12. spring-boot-docker-postgres_1 container created.
13. show containers on docker extension on vscode on ubuntu.
14. attach vscode to the container.
15. install some like following extensions on this container.
  * Extension Pack for Java
  * Lombok Annotations Support for VS Code
  * Maven for Java
  * Gradle for Java
  * Spling Boot Extension Pack
16. create project with spring initializer.
17. set postgres to application.properties.
18. build and run this project.
19. show http://localhost:8080

### application.properties

```
spring.jpa.database=POSTGRESQL
spring.datasource.url=jdbc:postgresql://postgres:5432/postgres
spring.datasource.username=postgres
spring.datasource.password=postgres
```

## Misc

### run docker on ubuntu

```
sudo service docker start
```

### backup database on ubuntu

```
docker run -it --rm --network spring-boot-docker_default postgres pg_dump -h spring-boot-docker_postgres_1 -U postgres> postgresql.dump
```
