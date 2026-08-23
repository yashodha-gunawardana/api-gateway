# ServiceHub - API Gateway

## 📌 Overview

The **API Gateway** is the entry point for client requests in the ServiceHub microservice architecture.

It routes requests from the frontend to the appropriate backend microservice.

---

## 👨‍🎓 Student Information

| Information | Details |
|---|---|
| Student Name | Yashoda Gunawardhana |
| Student ID | 241711077 |
| Project | ServiceHub |
| Component | API Gateway |
| GCP Project ID | Not created yet |

---

## 🛠️ Technology Stack

- Java 25
- Spring Boot
- Spring Cloud Gateway
- Spring Cloud Config
- Eureka Client
- Maven

---

## 🏗️ Architecture

```
                    Frontend
                       |
                       v
              API Gateway :8080
                       |
          +------------+------------+
          |            |            |
          v            v            v
    User Service   Request Service   Provider Service
       :8081            :8082             :8083
```

---

## 🔀 Routing

The API Gateway routes requests to backend services.

```
/api/users/**      → User Service
/api/requests/**   → Request Service
/api/providers/**  → Provider Service
```

The exact routes depend on the current gateway configuration.

---

## 🔎 Service Discovery

The Gateway uses Eureka for service discovery.

```
API Gateway
     |
     v
Eureka Server :8761
     |
     +---- User Service
     +---- Request Service
     +---- Provider Service
```

---

## ⚙️ Configuration

The API Gateway uses Spring Cloud Config for centralized configuration.

```
Config Server :8888
        |
        v
API Gateway :8080
```

---

## 🔌 Service Information

| Property | Value |
|---|---|
| Service Name | api-gateway |
| Port | 8080 |
| Eureka Server | 8761 |
| Config Server | 8888 |

---

## 🚀 Running the Gateway

**Windows**

```bash
.\mvnw.cmd spring-boot:run
```

### Build

```bash
.\mvnw.cmd clean package
```

### Run Tests

```bash
.\mvnw.cmd test
```

---

## 🔗 GitHub Repository

https://github.com/yashodha-gunawardana/api-gateway

---

## 📌 Project Status

- Java 25: ✅
- Spring Cloud Gateway: ✅
- Eureka Client: ✅
- Config Client: ✅
- GitHub Repository: ✅
- GCP Deployment: ⏳

---
