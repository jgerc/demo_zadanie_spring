_**Case Study: Demo Spring Boot Application**_

*Overview*

This project demonstrates a simple Spring Boot application that includes essential elements like a REST controller, application configuration, and dependency management through Maven. The application is designed for educational purposes and serves as a starting point for building more complex systems.


*Project Structure*

Key Files:

1. **`pom.xml`**:
   - Manages project dependencies and build lifecycle.
   - Includes dependencies for Spring Boot and other required libraries.

2. **Main Application Class** (`DemoZadanieSpringApplication.java`):
   - The entry point of the application.
   - Annotated with `@SpringBootApplication`, enabling auto-configuration, component scanning, and other Spring Boot features.

3. **Controller Class** (`HelloController.java`):
   - Defines a simple REST endpoint.
   - Handles HTTP GET requests and returns a predefined response.

4. **`application.properties`**:
   - Contains configuration settings for the application, such as server port and logging levels.


*Detailed Analysis*

`pom.xml`
The `pom.xml` file specifies the Maven configuration for this project. It includes dependencies such as:
- `spring-boot-starter-web`: Provides the web framework and embedded server.
- `spring-boot-starter-test`: Includes libraries for unit and integration testing.
Main Class (`DemoZadanieSpringApplication.java`)

@SpringBootApplication
public class DemoZadanieSpringApplication {
    public static void main(String[] args) {
        SpringApplication.run(DemoZadanieSpringApplication.class, args);
    }
}

Controller (`HelloController.java`)

@RestController
@RequestMapping("/api")
public class HelloController {

    @GetMapping("/hello")
    public String sayHello() {
        return "Hello, Vistula!";
    }
}

`application.properties`
The configuration file is minimal, containing essential settings:
```properties
server.port=8080
```
This sets the application to run on port 8080.

**Conclusion**

This demo Spring Boot application provides a foundational understanding of building RESTful services with Spring. It is ideal for beginners looking to explore the basics of Spring Boot and REST API development.
