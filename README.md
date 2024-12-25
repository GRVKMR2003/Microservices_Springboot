
# Microservices with Spring Boot

## Overview
This project demonstrates the implementation of microservices architecture using Spring Boot. It covers various aspects of microservices such as service discovery, circuit breaker, API gateway, and inter-service communication.

## Features
- **Service Discovery**: Using Netflix Eureka for service registry and discovery.
- **API Gateway**: Using Netflix Zuul as the API Gateway.
- **Circuit Breaker**: Using Netflix Hystrix for fault tolerance.
- **Inter-Service Communication**: Using OpenFeign for declarative REST clients.
- **Centralized Configuration**: Using Spring Cloud Config for external configuration management.
- **Distributed Tracing**: Using Spring Cloud Sleuth for tracing and Zipkin for visualization.
- **Dockerization**: Docker support for containerization of services.

## Prerequisites
- Java 8 or above
- Maven
- Docker (for containerization)
- Git (for version control)

## Getting Started
### Clone the repository
```bash
git clone https://github.com/GRVKMR2003/Microservices_Springboot.git
cd Microservices_Springboot
```

### Build the project
```bash
mvn clean install
```

### Run the services
1. Start Eureka Server:
    ```bash
    cd eureka-server
    mvn spring-boot:run
    ```
2. Start Config Server:
    ```bash
    cd config-server
    mvn spring-boot:run
    ```
3. Start API Gateway:
    ```bash
    cd api-gateway
    mvn spring-boot:run
    ```
4. Start other microservices (e.g., user-service, order-service):
    ```bash
    cd user-service
    mvn spring-boot:run
    
    cd ../order-service
    mvn spring-boot:run
    ```

### Running with Docker
1. Build Docker images:
    ```bash
    docker-compose build
    ```
2. Start all services using Docker Compose:
    ```bash
    docker-compose up
    ```

## Usage
- Access Eureka Dashboard: `http://localhost:8761`
- Access API Gateway: `http://localhost:8080`
- Use the API endpoints exposed by the microservices through the API Gateway.

## Contributing
Contributions are welcome! Please fork the repository and create a pull request with your changes.

## License
This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.

## Acknowledgements
- Spring Boot
- Spring Cloud
- Netflix OSS
