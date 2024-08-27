# Microservices

https://www.geeksforgeeks.org/top-microservices-interview-questions/
https://www.geeksforgeeks.org/microservices/
https://www.geeksforgeeks.org/how-data-flows-between-systems-in-microservices/?ref=asr1

### What are Microservices?

Microservices architecture is an approach to building software applications as a collection of loosely coupled, independently deployable services. Each service is designed to handle a specific business function and communicate with other services through well-defined APIs.

Microservices are an architectural style used in software development where an application is structured as a collection of small, independent services, each of which handles a specific business function. Unlike traditional monolithic architectures, where all components of an application are tightly integrated into a single codebase, microservices allow each component to be developed, deployed, and scaled independently. Here's a detailed look at microservices:

### Key Characteristics of Microservices

1. **Single Responsibility**: Each microservice is designed to perform a specific, narrowly defined function or business capability, such as user authentication, order processing, or inventory management.

2. **Loose Coupling**: Microservices interact with each other through well-defined APIs and are designed to operate independently. This loose coupling makes it easier to change or update one service without affecting others.

3. **Independent Deployment**: Each microservice can be deployed independently. This means that updates or new features can be rolled out incrementally, reducing the risk of system-wide disruptions.

4. **Decentralized Data Management**: Microservices typically have their own database or data storage. This approach, known as "database per service," allows each microservice to use the data store that best fits its needs and avoids the complexity of a single, monolithic database.

5. **Scalability**: Since each service is independent, they can be scaled individually. If one service experiences high demand, it can be scaled without scaling the entire application, optimizing resource use.

6. **Technology Agnostic**: Different microservices can be implemented using different technologies, programming languages, or frameworks, depending on what best suits the specific needs of each service.

7. **Fault Isolation**: If one microservice fails, it doesn’t necessarily bring down the entire system. This isolation helps improve the overall resilience of the application.

### Benefits of Microservices

- **Flexibility in Development**: Teams can develop, test, and deploy services independently, which speeds up development cycles and allows for more frequent updates.
- **Scalability**: Services can be scaled independently based on demand, allowing more efficient use of resources.

- **Resilience**: Faults in one service do not directly impact other services, enhancing the application's overall stability.

- **Technology Diversity**: Teams can choose the best tools and technologies for each service, leading to potentially better performance and developer satisfaction.

- **Faster Time-to-Market**: Independent development and deployment of services can accelerate the delivery of new features and updates.

### Challenges of Microservices

- **Complexity**: Managing multiple services, each with its own data store, communication mechanisms, and deployment pipeline, adds complexity to system design and maintenance.

- **Inter-Service Communication**: Effective and reliable communication between services is crucial and requires robust mechanisms for handling network calls, retries, and data consistency.

- **Data Consistency**: Ensuring data consistency across services that manage their own data stores can be challenging and often requires implementing patterns such as event sourcing or CQRS (Command Query Responsibility Segregation).

- **Monitoring and Debugging**: Tracking and diagnosing issues across distributed services requires sophisticated monitoring and logging systems.

### Example Use Cases

- **E-commerce Platforms**: Services for user management, product catalog, order processing, and payment can be developed and maintained independently.

- **Streaming Services**: Services for content management, user profiles, recommendations, and analytics can be managed separately.

Microservices represent a shift from traditional monolithic architectures to a more modular and scalable approach, aligning well with the needs of modern, dynamic applications.

### How do Microservices work?

1. **Service Decomposition**: In a microservices architecture, the application is divided into smaller, self-contained services. Each service corresponds to a specific business capability or function, such as user authentication, payment processing, or order management.

2. **Independent Deployment**: Each microservice can be developed, deployed, and scaled independently of the others. This means you can update or scale individual services without affecting the entire application, leading to more agile and flexible development processes.

3. **Communication**: Microservices typically communicate with each other over network protocols. Common methods include RESTful APIs using HTTP/HTTPS, messaging queues (e.g., RabbitMQ, Kafka), or gRPC (a high-performance RPC framework). Each service exposes an API that other services or clients use to interact with it.

4. **Data Management**: Each microservice usually has its own database or data store. This approach, known as database per service, ensures that services are loosely coupled and can operate independently. It also allows each service to choose the most appropriate data storage technology for its needs.

5. **Service Discovery**: In a dynamic environment where services can be added or removed, service discovery mechanisms help locate and communicate with instances of services. Tools like Consul, Eureka, or built-in features in container orchestration platforms (e.g., Kubernetes) manage this process.

6. **Resilience and Fault Tolerance**: Microservices architecture promotes resilience. If one service fails, it doesn’t necessarily bring down the whole system. Techniques like circuit breakers, retries, and timeouts help manage and recover from failures gracefully.

7. **Deployment and Scaling**: Microservices can be deployed in various ways, including on physical servers, virtual machines, or containers (e.g., Docker). Container orchestration platforms like Kubernetes automate deployment, scaling, and management of these containers.

8. **Monitoring and Logging**: Since microservices are distributed, monitoring and logging become crucial. Centralized logging systems (e.g., ELK Stack, Splunk) and monitoring tools (e.g., Prometheus, Grafana) collect and analyze data from various services to ensure system health and performance.

9. **Security**: Security in a microservices architecture involves securing the communication between services, authenticating and authorizing service requests, and managing sensitive data. Implementing security measures such as OAuth, JWT, and SSL/TLS is essential.

10. **Continuous Integration and Continuous Deployment (CI/CD)**: CI/CD pipelines are often used to automate the building, testing, and deployment of microservices, ensuring that changes are delivered quickly and reliably.

Overall, microservices offer benefits like improved scalability, flexibility, and resilience, but they also come with challenges such as increased complexity and the need for robust management and monitoring practices.

### What are the main components of Microservices Architecture?
Microservices architecture comprises several components that work together to create a modular, scalable, and independently deployable system.

The main components of microservices include: 

**Microservices**: These are the individual, self-contained services that encapsulate specific business capabilities. Each microservice focuses on a distinct function or feature.

**API Gateway**: The API Gateway is a central entry point for external clients to interact with the microservices. It manages requests, handles authentication, and routes requests to the appropriate microservices.
Service Registry and Discovery: This component keeps track of the locations and network addresses of all microservices in the system. Service discovery ensures that services can locate and communicate with each other dynamically.

**Load Balancer**: Load balancers distribute incoming network traffic across multiple instances of microservices. This ensures that the workload is evenly distributed, optimizing resource utilization and preventing any single service from becoming a bottleneck.

**Containerization**: Containers, such as Docker, encapsulate microservices and their dependencies. Orchestration tools, like Kubernetes, manage the deployment, scaling, and operation of containers, ensuring efficient resource utilization.

**Event Bus/Message Broker**: An event bus or message broker facilitates communication and coordination between microservices. It allows services to publish and subscribe to events, enabling asynchronous communication and decoupling.

**Centralized Logging and Monitoring**: Centralized logging and monitoring tools help track the performance and health of microservices. They provide insights into system behavior, detect issues, and aid in troubleshooting.

**Database per Microservice**: Each microservice typically has its own database, ensuring data autonomy. This allows services to independently manage and scale their data storage according to their specific requirements.
Caching: Caching mechanisms can be implemented to improve performance by storing frequently accessed data closer to the microservices. This reduces the need to repeatedly fetch the same data from databases.

**Fault Tolerance and Resilience Components**: Implementing components for fault tolerance, such as circuit breakers and retry mechanisms, ensures that the system can gracefully handle failures in microservices and recover without impacting overall functionality.

### What are the Design Patterns of Microservices?
When a problem occurs while working on a system, there are some practices that are to be followed and in microservices, those practices are Design Patterns. Microservices design patterns are such practices which when followed lead to efficient architectural patterns resulting in overcoming challenges such as inefficient administration of these services and also maximizing performance. While working on an application, one must be aware of which design pattern to be used for creating an efficient application.

- Aggregator
  - It invoked services to receive the required information (related data) from different services, apply some logic and produce the result.
  - The data collected can be utilized by the respective services. The steps followed in the aggregator pattern involve the request received by the service, and then the request made to multiple other services combines each result and finally responds to the initial request. 
- API Gateway
  - API Gateway acts as a solution to the request made to microservices.
  - It serves as an entry point to all the microservices and creates fine-grained APIs for different clients.
  - Requests made are passed to the API Gateway and the load balancer helps in checking whether the request is handled and sent to the respective service.
- Event Sourcing
  - This design pattern creates events regarding changes (data) in the application state.
  - Using these events, developers can keep track of records of changes made.
- Strangler
  - Strangler is also known as a Vine pattern since it functions the same way vine strangles a tree around it. For each URI (Uniform Resource Identifier) call, a call goes back and forth and is also broken down into different domains.
  - Here, two separate applications remain side by side in the same URI space, and here one domain will be taken into account at a time. Thus, the new refactored application replaces the original application.
- Decomposition
  - Decomposition design pattern is decomposing an application into smaller microservices, that have their own functionality.
  - Based on the business requirements, you can break an application into sub-components. For example, Amazon has separate services for products, orders, customers, payments, etc.
 
### Microservices vs. Monolithic Architecture?
Below is a tabular comparison between microservices and monolithic architecture across various aspects:

|Aspect|Microservices Architecture|Monolithic Architecture|
| ------ | ------ | ------ |
| **Architecture Style** | Decomposed into small, independent services. | Single, tightly integrated codebase. |
| **Development Team Structure** | Small, cross-functional teams for each microservice. | Larger, centralized development team. |
| **Scalability** | Independent scaling of individual services. | Scaling involves replicating the entire application. |
| **Deployment** | Independent deployment of services. | Whole application is deployed as a single unit. |
| **Resource Utilization** | Efficient use of resources as services can scale independently. | Resources allocated based on the overall application’s needs. |
| **Development Speed** | Faster development and deployment cycles. | Slower development and deployment due to the entire codebase. |
| **Flexibility** | Easier to adopt new technologies for specific services. | Limited flexibility due to a common technology stack. |
| **Maintenance** | Easier maintenance of smaller, focused codebases. | Maintenance can be complex for a large, monolithic codebase. |
| **Testing** | Independent testing of each microservice. | Comprehensive testing of the entire application. |
| **Infrastructure Dependency** | Less dependent on specific infrastructure choices. | Tied to specific infrastructure due to a shared codebase. |

