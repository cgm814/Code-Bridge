
# Code Bridge

### Introduction

Code Bridge is a Spring Cloud-based online education platform designed with a distributed architecture. It serves as an excellent system for online learning, experimentation, and code assessment. The platform integrates various technologies to provide robust and scalable services for both students and teachers.

Detailed information about this project can be found on the [Code Bridge website](https://tech-webs.com/code-bridge/).

### Features

- **User Management**: Manage and organize teacher and student users, allowing registration, login, and profile management.
- **Course Management**: Teachers can create courses, manage class activities, and assign tasks.
- **Resource Management**: Share and manage learning resources among users.
- **Real-Time Interaction**: Provides an interactive online classroom for real-time teaching and student engagement.
- **Task Management**: Assign and manage various tasks like exams, assignments, and projects.
- **Code Evaluation**: Automatic code evaluation and feedback for submitted assignments.
- **Performance Tracking**: Track student progress and display performance metrics.

### Prizes

- **First Prize** in the Central South China Competition of the China University Students Computer Design Contest.
- **Third Prize** in the National Competition of the China University Students Computer Design Contest.

### Frameworks

- **Backend**: Java 1.8, Spring 2.3.9.RELEASE, Spring Cloud Alibaba 2.5.5.RELEASE, Spring Cloud Gateway
- **Database**: MyBatis, MySQL 8, Redis 7.0.0
- **Service Discovery**: Nacos 2.1
- **Frontend**: Vue 2, ElementUI

### System Architecture

The system employs a microservices architecture to ensure scalability and maintainability. Key components include:

- **Service Discovery and Configuration**: Nacos
- **API Gateway**: Spring Cloud Gateway
- **Database**: MySQL for persistent storage, Redis for caching
- **Frontend**: Vue.js with ElementUI for a responsive user interface

### Detailed Design and User Subsystems

1. **User Subsystem**: Handles user registration, login, and profile management, including teacher and student roles.
2. **Course Subsystem**: Manages course creation, enrollment, and class activities.
3. **Task Subsystem**: Facilitates assignment creation, resource management, and progress tracking.

### Installation and Usage

#### Prerequisites

- Java JDK/JRE 17.0 or later
- Maven 3.8.0 or later
- MySQL 8.0.0 or later
- Redis 7.0.0 or later

#### Setup

1. **Clone the repository**:
   ```bash
   git clone https://github.com/yourusername/code-bridge.git
   cd code-bridge
   ```

2. **Import SQL files into MySQL**:
   Import the provided SQL files into their respective databases.

3. **Start Redis and Nacos**:
   Ensure Redis is running (password can be empty) and start Nacos in singleton or cluster mode with Nginx as the reverse proxy.

4. **Modify Configuration**:
   Adjust the `application.yml` files in each JAR package to match your environment settings.

5. **Build and Run the Application**:
   Navigate to each JAR directory and execute:
   ```bash
   java -jar gateway-1.0-SNAPSHOT.jar
   java -jar user-service-1.0-SNAPSHOT.jar
   java -jar task-service-1.0-SNAPSHOT.jar
   java -jar course-service-1.0-SNAPSHOT.jar
   java -jar relationship-service-1.0-SNAPSHOT.jar
   ```

### Known Issues

- Occasional freezing bugs in the application.
- Some features may not function optimally in certain environments.

### Future Updates

- Addition of more interactive features and performance optimizations.

## License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.

