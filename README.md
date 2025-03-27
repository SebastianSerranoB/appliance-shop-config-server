# Appliance Shop Config Server

The Config Server is a pivotal component of the Appliance Shop Microservices Application, providing centralized configuration management for all microservices. Built with Spring Cloud Config Server, it externalizes configuration properties, allowing dynamic and consistent configuration across environments.

## Features

- **Centralized Configuration Management**: Stores and serves configuration settings for all microservices from a central 
- **Dynamic Configuration Updates**
- **Environment-Specific Configurations**

## Prerequisites

- **Java 21**
- **Git**

## Setup Instructions

1) **Clone the Repository**:

      git clone https://github.com/SebastianSerranoB/appliance-shop-config-server.git

2) **Configure the Configuration Repository:**

   Update the application.yml file to specify the location of your configuration repository. This can be a Git repository or a local file system path.

      spring:
        cloud:
          config:
            server:
              git:
                uri: https://github.com/your-config-repo.git

 3) **Run the Config Server:**
         ./mvnw spring-boot:run
    The server will start on the default port 8888.

## Accessing Configurations

Microservices can retrieve their configurations by making HTTP requests to the Config Server. For example, to fetch configurations for a service named product-service in the development environment:

http://localhost:8888/product-service/development

## Contributing

Contributions are welcome! Please fork the repository and submit a pull request with your enhancements or fixes.

## License
On the way!

This README provides a clear overview of the Config Server's purpose, features, setup instructions, and usage, ensuring that developers can effectively integrate and utilize it within the Appliance Shop Microservices Application.
