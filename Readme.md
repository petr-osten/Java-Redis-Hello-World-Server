# Hello world java server with redis

The purpose of this repo is to serve as a jump start with docker and kubernetes deployments for new devops candidates.

## Overview

This application needs redis for its functionality, its a typical enterprise application. Lazy devs did not write much of the documentation so just try to get this application up and running in your kubernetes cluster preferrably without using hints.

## Hints

* <details>
    <summary>Technologies used.</summary>
    Maven, Springboot, Redis
</details>

* <details>
    <summary>Networking.</summary>
    By default application runs on port 8080 and tries to connect to redis on `localhost:6379`
</details>

* <details>
    <summary>Build via docker maven.</summary>

    ```
    docker run -it --rm --name my-maven-project -v "$(pwd)":/usr/src/mymaven -w /usr/src/mymaven maven:3.8.1-jdk-8-slim mvn clean install
    ```
</details>

* <details>
    <summary>How to run application.</summary>

  * Without configuration overload:
    ```
    java -jar target/SpringbootRedisUsingJedis.jar
    ```
  * With configuration overload:
    ```
    java -jar target/SpringbootRedisUsingJedis.jar --spring.config.location=classpath:/application.properties,file:./override.properties
    ```
</details>
