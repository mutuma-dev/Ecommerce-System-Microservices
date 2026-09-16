# E-Commerce Microservices

A demo e-commerce application built with **Spring Boot** and **Spring Cloud**, demonstrating how to design, communicate, deploy, monitor, and scale a microservices-based system.

The project contains **5 independent microservices**:

- Customer Service
- Product Service
- Order Service
- Payment Service
- Notification Service

## Architecture & Communication

Services communicate using:

- **REST APIs**
- **OpenFeign** for synchronous inter-service communication
- **RabbitMQ / AMQP** for asynchronous messaging

The project demonstrates:

- Service Discovery with **Eureka**
- Load Balancing
- API Gateway with **Spring Cloud Gateway**
- Distributed Tracing with **Zipkin**
- Resilience and health checks
- Centralized observability and monitoring

## Key Features

### Service Discovery

Uses **Eureka Server** to allow microservices to discover and communicate with each other dynamically.

### Inter-Service Communication

Uses **OpenFeign** for declarative REST communication between services.

### Load Balancing

Demonstrates load balancing between service instances and health-check mechanisms.

### API Gateway

**Spring Cloud Gateway** provides:

- Request routing
- Load balancing
- Centralized entry point
- Circuit breaker integration

### Distributed Tracing

Uses **Zipkin** and tracing to track requests across multiple microservices and simplify debugging.

### Asynchronous Messaging

Uses **RabbitMQ / AMQP** for asynchronous communication, particularly for notification events.

### Data Mapping

Uses **MapStruct** for efficient entity-to-DTO mapping.

### Containerization

Uses **Jib** to build container images without requiring a Dockerfile.

The project can also be run locally using **Docker Compose**.

## Kubernetes

The application is deployed to Kubernetes using:

- Deployments
- Services
- StatefulSets
- Persistent Volumes
- Persistent Volume Claims
- Ingress
- Kubernetes Secrets

The Kubernetes deployment includes supporting infrastructure such as:

- PostgreSQL
- RabbitMQ
- Zipkin

Kubernetes also provides service discovery and load balancing between application instances.

## AWS Deployment

The project is deployed to **AWS EKS (Elastic Kubernetes Service)**.

AWS infrastructure includes:

- EKS cluster
- EC2 worker nodes
- Kubernetes workloads
- Amazon RDS for databases
- Autoscaling

## Monitoring & Observability

Application monitoring is implemented using:

- **Spring Boot Actuator**
- **Micrometer**
- **Prometheus**
- **Grafana**
- Distributed tracing

This provides visibility into application health, metrics, performance, and service communication.

## CI/CD

The project uses **GitHub Actions** to automate deployment to AWS EKS.

The pipeline handles:

1. Building and packaging the applications
2. Building and pushing container images
3. Updating Kubernetes manifests
4. Configuring AWS credentials
5. Updating Kubernetes configuration
6. Deploying the services to EKS
7. Managing Kubernetes secrets

## Technologies

- Java
- Spring Boot
- Spring Cloud
- Spring Data JPA
- Spring Web
- Spring Cloud Gateway
- Spring Cloud OpenFeign
- Eureka
- RabbitMQ
- PostgreSQL
- MapStruct
- Docker
- Jib
- Kubernetes
- Minikube
- AWS EKS
- AWS RDS
- GitHub Actions
- Zipkin
- Prometheus
- Grafana
- Spring Boot Actuator
- Micrometer

## Deployment

The application can be deployed locally using **Docker Compose** or **Minikube**, or to **AWS EKS** using Kubernetes manifests and GitHub Actions.

The project demonstrates the complete flow from building individual Spring Boot microservices, connecting them through synchronous and asynchronous communication, containerizing them, deploying them to Kubernetes, and finally running them on AWS EKS with monitoring and CI/CD.
