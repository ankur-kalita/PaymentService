# Payment Processing Service

## Overview
The *Payment Processing Microservice* is a lightweight, modular, and plug-and-play service built with *Spring Boot* to initiate, process, and track payments. It follows object-oriented design principles to ensure maintainability and scalability while providing seamless payment handling.

## Features

### Payment Handling
- Initiate, process, and track payments.
- Default integration with *Razorpay* as the payment gateway.
- Modular architecture to support multiple payment gateways.

### High Availability & Fault Tolerance
- Workflow-based interface to easily switch between payment services.
- Ensures minimal downtime with dynamic gateway selection.

### Design & Architecture
- Follows *MVC architecture* for structured development.
- Uses *Data Transfer Objects (DTOs)* for efficient data handling.
- Implements *object-oriented principles* for maintainability.

## Tech Stack
- *Language:* Java
- *Framework:* Spring Boot
- *Payment Gateway:* Razorpay (default)
- *Database:* PostgreSQL / MySQL
- *Security:* Spring Security & JWT Authentication

## Installation

### Prerequisites
Ensure you have the following installed:
- Java 11+
- Maven
- PostgreSQL or MySQL
- Docker (optional, for containerized deployment)

### Clone the Repository
sh
git clone https://github.com/your-username/payment-microservice.git
cd payment-service


### Environment Configuration
Create a .env file and configure the following:
ini
DB_HOST=localhost
DB_PORT=5432
DB_USER=your_user
DB_PASSWORD=your_password
DB_NAME=payment_db
PAYMENT_GATEWAY=razorpay
RAZORPAY_KEY=your_key
RAZORPAY_SECRET=your_secret


### Install Dependencies
sh
mvn clean install


### Run Database Migrations
sh
mvn flyway:migrate


### Start the Server
sh
mvn spring-boot:run



### Running in Production
sh
SPRING_PROFILES_ACTIVE=prod mvn spring-boot:run


## Contributing
Contributions are welcome! Please follow these steps:
1. Fork the repository.
2. Create a new branch.
3. Commit your changes.
4. Submit a pull request.
