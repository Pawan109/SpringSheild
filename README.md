## **Project Overview**

SpringShield is a **secure authentication and authorization system** built using **Java Spring Boot**, focusing on **token-based authentication (JWT, Refresh Tokens)** and **role-based access control (RBAC)**. It ensures **secure API access** while enabling **real-time event-driven security monitoring** via **Apache Kafka**. The system integrates **Docker for containerization**, ensuring scalability and seamless deployment. A **design-first approach** was used, leveraging sequence diagrams to optimize workflows before development.

---

## **Features**

- **Microservices**: Implements authentication and authorization as independent services, ensuring modularity and scalability.
    
- **RESTful APIs**: Designed for secure login, token management, user roles, and authentication lifecycle.
    
- **Database Integration**: Uses a relational database to store users, roles, tokens, and authentication logs.
    
- **Kafka Messaging**: Publishes authentication events (e.g., login, token refresh) for real-time security monitoring.
    
- **Design-First Approach**: Built **sequence diagrams** before development to streamline the authentication flow and system interactions.
    

---

## **System Workflow**

1. **User Registration & Authentication**: Users sign up or log in via the `AuthController`, triggering role and token creation.
    
2. **Token Generation & Storage**: Upon successful authentication, a JWT access token and refresh token are generated and stored.
    
3. **Event Logging with Kafka**: Authentication events (e.g., successful login, failed login) are published to Kafka for monitoring.
    
4. **Access Control & Role Management**: API requests are validated using JWT tokens and user roles via `SecurityConfig` and `JWT Filter`.
    
5. **Token Refresh Handling**: Expired tokens trigger a refresh flow, verifying validity before generating a new JWT.
    
6. **Authorization Enforcement**: Role-based access controls (RBAC) ensure users can access only permitted resources.
    
7. **Session & Security Monitoring**: Kafka consumers listen for security-related events and trigger alerts when anomalies occur.
    
8. **Database Persistence**: User details, tokens, and authentication logs are stored in a secure database.
    
9. **Scalability & Deployment**: Dockerized services allow seamless deployment and scaling across environments.
    
10. **Security Context Management**: The `SecurityContextHolder` maintains user authentication details throughout the session.
    

---
### **Diagram**
![Image](https://github.com/user-attachments/assets/04c3773d-ad1e-4c5c-b444-10a7b5206d1f)

---
## **Technologies Used**

- **Backend**: Java Spring Boot (Spring Security, JWT, REST APIs)
    
- **Database**: PostgreSQL / MySQL (User and Token Storage)
    
- **Messaging**: Apache Kafka (Event-driven authentication logs)
    
- **Tools**: Postman (API testing), Docker (Containerization), IntelliJ, JIRA
    

---

## **Project Goals**

- **Understand Microservices**: Build modular authentication and authorization services for better scalability.
    
- **Explore Kafka**: Implement event-driven authentication logging and real-time security monitoring.
    
- **Learn Design Skills**: Use **sequence diagrams** to optimize authentication workflows before development.
    
- **Develop Real-World Systems**: Gain hands-on experience in **secure authentication** and **enterprise-grade API security**.
    
- **Optimize Deployment**: Use **Docker** for containerized, scalable deployment across different environments.


