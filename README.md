# microservices-note
Microservices Interview Questions 2025 | Top Microservices Interview Questions & Answers | MindMajix
================================================================================
https://www.youtube.com/watch?v=wmawYODmQU0

1. What are microservices?
========================
Microservices are an architectural style where an application is built as a collection of small , independent and loosely coupled services.
Each micro servces have its own independent database.
-Developed, deployed and scale independently.

2. How Microservices differ from Monolithic Architecture ?
============================================
Parameters
--------------
1. Architecture
  Monolithic architecture, a single code base that contains all of the modules, tightly coupled with one executable.
  Microservices are decoupled, all of the modules are seprate entities, they provide modular services and each of them is designed for specific bussiness function and the communication happens through APIs. 
2. Scalability
	Monolithic architecture, it primerly relies on vertical scalling like adding more resources like CPU or memory to a single server.
	In Microservices, Here is horizontal scalling like adding more instances for indivisual services when required.
3. Technology Stack
	Monolithic architecture, it requires a uniform stack for the entire application, limitting the flexibility. So the flexibility aspect is very limited here
	Microservices architecture, it allows diverse stack and this lets team choose the best technology for each services.
4. Deployment
	Monolithic architecture, Everything is deployed as single unit requiring the entire application to be redployed for the changes. So if we want to change in monolithic application, again we have to redeploy like we have to make the changes first and then redeploy the entire application.
	In Microservices, we can independely deploy a perticular microservices. This allows update one services without redeploying the others. 
5. Use Case
	Monolithic architecture, it is very suitable for smaller applications or systems with fewer updated and minimum scaling needs.
	Microservices architecture, it is very suitable for large, complex and rapidly evolving systems requires scalbility and flexibility.
	
3. What are the key fetures of Microservices?
===================================
- Independent Deployment
- Fault Isolation
    Means failures in a service doesnot cause entire application to fail.So it ensure greater resilience and minimizes the downtime.
-Scalbility
  Each service can scale independently based on a specific load and demand and thereby optimizing the resource usages and improving the performance.
  During peak time that indivisula service is scaled wrt to its load.
  Due this it is dynamic scalability and high availability.
  
4. Name the main components of Microservices ?
======================================
Core Characterstics:
--------------------------------
-Service Indendence
- Domain-Driven Design (DDD)
- API Communication
- Technology Diversity

Service Registry and Discovery:
---------------------------------------------
This is the cenralized system that helps the services locate each other dynamically.
Eg: Neflix Eureka console and Kubernets 
- API Gateway
	This acts as a single entry point for clients routing request to appropriate services and handling concerns like authentication, logging and rate limiting.
- Load Balancer
	Load Balancer Basically distributes the incomming traffic accross the instances of a service to ensure high availabilit.
- Data Management
	Each services manages its own database like database per service pattern and this ensure the loose coupling among different services.
- Monitoring and Logging
	Here we have tool like Prometheus, Graphana and ELK stack and thses tools ensure real-time monitoring and debugging.
- CI/CD Pipeline
	CI/CD Pipeline automates testing, deployment and scaling and it ensure faster iterations and minimized downtime.
	
5. Explain the role of API Gateway in microservices?
=============================================
API Gateway serves as a centralized entry point for managing client interactions with microservices.
It simplify the communication by routing the incomming requests to appropriate microservice and handles various operational resposibility as well.
There are 3 primerly responsibilities of API Gateway. 
1.Request Routing: API Gateway directs incomming client request to the micro services based on the operation that is being performed 
2. Load Balanching: API Gateway disctibutes requests evenly accross the multiple instances of a service to ensure optimal resource usages and high availability.
3. Authentication and Authorization: API gatewayb verfies the user credentials and enforces the security policies to ensure that only authorize users can access the specific services.

API Gateway uses Itenary manager for routing.

6. What is Service Discovery in Microservices?
========================================
Service Discovery is a machanism that enables microservices to dynamically locate and communicate with each other within a distributed system.
Adv/Benefits:
----------------
- It Ensures that the services can find and connect other services without hard coded configuration thereby promoting flexibility and Scalability\.
2 Types of Service Discovery
1. Client Side Discovery
	In this approach each service is responsible of keeping track of and managing its own service registry. So the client quires the registry to locate the availability service instances and the chooses the one to interact with.
2. ServerSide Discovery
    Centralized Registry such as Eureka oe console mentains the locations and statues of all the services. So when a client makes a request the server side load balancer queries the registry and routes the request to an appropriate service instance.

7. What is container , why is it used in Microservices?
===========================================
A container is a light weight and standalone unit that bundles an application  along with its dependency including libraries, configurations and runtime, ensure consistency across different environments
-There are 2 important units to using  containers in micro services
1. Consistent deployment, So containers ensure that the application run in the same way in development , testing and production environments. This minimize the compatibility issue 
2. Fatser startup time. Containers are mosre lightweight and have faster initialization times compared to traditional virtual machines thereby enabling the quicker deployments and scalability. We are using docker conatiner.

8. How do Microservices Communicate with each others?
=========================================== 
In a microservices architecture, communication between services is very crusial for acheiving co-ordination and colabration. Since microservices are designed to be independent and loosely coupled, they rely on wel defined communication protocols and mechanisms.

Method of communication
1. Restful API (Representaion State Transfer): Light weight, commonly used protocol. It uses HTTP methods like GET, POST, PUT, DELETE to facilate the synchronous between services. 
2. Through Message Queues: Message Queues enables asynchronous communication between services thereby allowing messages to be sent and received without requiring the services to be active simultanesously. Popular tools Apache Kafka, AWS SQS ad Rabit MQ 
3. GRPC  (G Remote process call): This is a high performance framework developed by Google.It used http2 for communication and the protocol buffers for data serialization and thereby it makes it more efficient than the rest for some usecaes 

9. How would you handle the microservice failure ?
========================================
In a microservices architecture, failures are invertiable, but the goal is to minimize their impact on the overall system.
Since the microservices ofen communicate with eachother, one failure can trigger a chain of reactions thereby leading to cascading failures that effects the entire application. To metigate the issue there are several technique and the best practice for handline the microervices.
Techniques:
1. Circuit Breakers: Circuit Breraker is a design pattern that helps prevent cascading failures by stopping the flow of requests to a service that is likely to fail. So if a microservice detects that another service is not responding or is behaving in a weired way, So the circuit breakrer opens preventing further request to the failing service and it allows to time to recover
2. Retries and Fallbacks: When a service failed to respond a retry mechanism can automatically attempt to resend the request after a short delay. So this is perticularly useful in a scenario where the failure is due to Temporary issues, such as netwoek congestion or breif outages,
3. Cenralized logging: In a microservices environment trobuleshooting and identifying the root cause of failures can be difficult due to distributed nature of the system. So here the cenralized logging aggregates the logs from all of the services into one lacation and it makes it easier to monitor the system and quickly identify and resolve failures.

10. How we can ensure backward compatibility in microservices?
==================================================
Backward compatibility is critical when deploying updates to microervices to avoid breaking client applications.
Using versioning in API and following semantic versioning principles can ensure smooth transitions

Intermediate People experience
11. What is the meaning of OAuth and Why is it Used ?
==============================================
OAuth  stands for Open Authorization.
It i an open standard protocol that allows third-party applications to access a user's resources without exposing their credentails such as usernames and passwords.
OAuth provides a secure and userfriendly way to Grant access to certain parts of applicatons or service without directly sharing the sensitive information.

12. What is CQRS Pattern in microervices ? What problem does it solve?
=========================================================
CQRS stands for Command and Query system in which data operations are separated into two, command which write data into database and Query system which reads data from database or data store. 

Whether it is a read heavy or write heavy operation.
Read Replica and Write Replica in DB.

13. Compare API Gateway and LoadBalancer in microservices.
=================================================
Load Balancer is an old concept which is used to distribute load or traffic across multiple instances.
API Gateway is a Microservice pattern which not only does load balancing but also can be used for lookup and can also simplify client code. We can implements authentication, authorization, security, logging on API Gateway level, instead of implementing in each microservice.

14. What are some common microservices design principles?
===================================================
- High Cohesion: Besically refers to the desihn of  each microervices to be focus around a single wel defined responsibility or business capability. A Cohesive service should be limited for a specific task or a set of related task with minimal dependencies on other services.

- Autonomous: It means microservices should operate independently without depending with one another. So Each microervices should have its own data , bussiness logic and the interface. So this principle emaphasizes loose coupling between the services. So one serfice failure should not affect other services.
- Bussiness Domain Centric: Microservices should be aligned with bussiness domain or capabilities rather than technical layers or function. So each service should be correspond to a specific bussiness function or a capability making the architecture more intuitive and closely tied to business objective.
- Resilience : Microservice should be resilience to failure and designed to gracefully handle distruptions or faults. So this included startergy like redundancy, circuit Breakers and fallbacks to ensure a failure in one service  doesnot lead to systemwide downtime.
-Onservable: Observable basically refers to ability to Monitor and track the health and performance of microervices in real time. So this includes logging, metrics and tracing to capture the insights into how services are performing and interacting with one another.
-Automation: Is the key design , which is refers to the use of automated processes for deployment, scaling and managemet of microervices. It can ensure that microservices can be deployed quickly and reliably the 

15. How do you ensure security in microervices?
=======================================
There few Practices
1.  Secure Communication: It refers to encrypting the data exchange between microservices to prevent the eavesdropping, main in the middle attacks and unauthorized data access. So this is done using the TLS or the transport layer securityor THE SSL Secure socker layer protcol.
2. Authentication and Authorization: It ensure that only verfied authorized users or services can access specific resources in the micro services system. Authentication verfies the identity of the users or services while authorization defines what actions or resources they can access.
3. Service-Level Isolation: This refers to restricting access between microservices to only the necessary communication pathes. This ensure the services interact only with the ones that they are meant to communicate with reducing the risk of an attackter gaining the access to other services

16. What are the few ways to acheive synchronous and asynchronous communication between microervices?
=========================================================================
There are many ways to implement synchronous communication in Microservices architecture like we can use REST API calls, gRPC or GraphQL API to retrieve data from server in synchronous manner and also to upload data to server.

For Asynchronous communication tools like Apache Kafka, Rabit MQ, AWS SQS or Active MQ. These are message brokers allows to sender 
to send and forget and receiver then can process when they are free giving the sender and receiver the freedom to work based on their speed.

17. How Do You Implement Rate Limiting in Microservices?
=============================================
Rate Limiting is very important aspects of managing the load on a system especially in microservices architecture when multiple services interacts and can experince heavy or unexpected traffic.

- Rate limiting ensures fair usage of reseources by controlling how many request client can make within a certain time period. This protects services from being overwhelmed by too many request preventing abuse and helps to maintain the systems stability and performance.

- There 2 technique or 2 ways  to implementing rate limiting in microservices.
 1. Token Bucket Algorithm: - In this metods tokens are replaced in a bucket and each incoming request consumes one token.If the bucket has tokens available the request can be processed further if not the request is denied or cubed. So the tokens are refilled  periodically at a constant rate. Thereby allowing the client to make new request over time.
2. API Gate way for Rate Limitting: - API gate is the entry point for all client request in microervices architecture. So basically it can be configured to handle the rate limiting for all imcomming traffic before it reaches the backend services.

18. What is Event-Driven Architecture in Microservices?
==========================================
Event-Driven architecture is a design pattern where microservices communicate with each other by producing and consuming events rather than making direct API calls.

-in this architecture, service emmits events to signal that something has occurred  and other services listen to these events to trigger actions and process in response.
- So this patterns enables asynchronous communication allowing services to operate independently without needing to be tightly coupled. This architecture helps increase scalability, flexibility and responsiveness in a microservices echo system.

19. What is Idempotency and why it is important in microservices ?
======================================================
Idempotency is a key concept in distributed systems and microservices architecture. It ensures that making the same request multiple times produces the same result, regardless of how many times it is executed.
- This characterstic is crucial for systems that need to handle retries due to transient failures network issues or other interuptions.
- In microservices the communication is often done over unreliable networks, it is common for the request to be retried either by the client or the system itself. So without idempotency retrying the same request could lead to inconsistent or undersirable outcomes such as creating duplicate records or performing the same operation multiple times. 
- So Idempotency basically helps to eliminate these issues by guaranteeing that the repeating a request will not alter the final state of the system

20. What is database Sharding and why it is used in microservices?
===================================================
Database sharding is a technique used in disctributed database systems where large datasets are divided into smaller, more manageable pieces called "shards.".
- Each Shard contains a subset of the data and can be stored on separate database instances or servers.
- In microservices architecture database sharding is particularly useful as it allows each service to handle its own database ensuring that no single database becomes a bottleneck as the system grows.
- So each microservice can operate independently with its own shard which can be scaled as and when needed without affecting the other services.


Advance Questions
----------------------------
21. How do you handle data consistency in Microservices?
==============================================
Microservices follows the consistency model where all the services eventually converge the same data state rather than maintaining the immediate consistency.
There are few technique to handle the data consistency in microservices
1. Saga Pattern
   It has 2 approach
   - Choreography : - In this approach services are communicate through events and each service perform its task and emmits an event for the next service.
   - Orchestration: - A central co-ordinator manages the work flow between the services.
2. Event Sourcing
	Events rather than the final state are stored in microservices and the current state is derived by replaying the events.
	EX: - Payment service store the event like payment initiated and payment completed and these events are often replayed or reconstructed as per the status of the payment.
3. Distributed transactions
   Here we follows the two phases commit or 2 PC or compersating transcations for critical operation.
   Ex: Booking Hotel or a Flight simultanesously required both operations to succeed or roll back entierly.
   
22. What is a Canary Deployment in Microservices?
==========================================
Canary Deployment is a software release startergy where a new version of a service is gradually introduced to a small subset of users before a full rollout to the entire user base.

- This will minimize the risk associated with deploying the new code by allowing for controlled testing and observation in a live environment.

23. How would you monitor the microservices?
===================================
- Monitor is a crusial aspect for ensuring the health, performance and overall stability in a microservices where everying is in disctributed system.
- It provided valuable insights to the behaviour of indivisual services and their interactions.
- There are few steps through which we can monitor the microservices 
Step-1: Distributed Tracing
---------------------------------------
Using Distributed tracing we can track the flow of requests across  multiple services in distributed system. So this helps identify  performance bottleneck, pinpoint the root cause of errors and understand the overall the request journey. 
We have tools like Jagger and Zipkin.

Step-2: Metrics collection:
------------------------------------
-We can collect the key performance indicators or apis such as response time , error rates, throughputs and resource utilization like CPU and memory for each separate micro services.
Tools like Prometheus, Prometheus is an open source monitoring and altering systems that collects metrics including verious sources like applications, OS and cloud infra structure.

Step-3: Visualization and Alerting
------------------------------------------------
We can visualized collected metrics and tracing data using dashboard and create alerts to notfiy the teams of critical issues.
Tools used like Graphana and kibana.

24. What are DDD Principle in microservices?
==================================
DDD -> Domain Driven Design: This is a software development approach that emphasizes on creating software models that align with bussiness domain.
So we applied to Microservices DDD principle can help structure and organize services effectively.

- Bounded Context:
Each microservice should represent a bounded context, encapsulating  a specific bussiness domain or a sub domain.
This promotes  loose coupling and independent development.
- Ubiquitous Language
Here we have vocabulary between bussiness exports and developers and this ensure clear communication and understanding of domains.
So for microservice architecture we have consistent terminology across the teams  and services and this prevents ambiguity and improves the colabration.
-Aggregate
 An Aggregate is a cluster of associateed object that treated as a single unit for data updates.
 -So for a microservices application, Aggregates help maintain data consistency within a bounded context.

Do using the above DDD principle we can develop cohesive and maintainable microervices architecture that aligns with the bussiness domain.

25. How do we design scalability in Microservices?
=========================================
-Scalability ensure that our services can handle increasing traffic and data volumes without experiencing performance degradation.
Different Startergy
Horizontal Scaling (Scaling out)
--------------------------------------------------
Adding more instances to a service to handle the increased load.
-It is very easy to implement and this provides a quick and effective way to handle temporary traffic surges.

Database Partioning and Sharding
-------------------------------------------------
Distributing data across multiple databases to improves read and write performance. So this reduces the load in indivisual database and it also improved the performance for large data sets.

Caching
------------------
- Storing frequently accessed data in memory to reduce the load in underlaying database. Caching significantly improved the response time for frequently access data and it also reduces the load on the databases.

Load Balanching
------------------------
Load Balancing means distributed the incomming traffic to multiple instances of the service. So load balancing prevents the bottlenecks and ensure even resource distribution utilization and service instances.
- It also improves the overall system performance and ability.

Asynchronous Processing
----------------------------------
- in Asynchronous Processing, processing tasks in the background to avoid blocking the main request or response cycle.
- This improved the responsiveness of the main application and it also enables handling timely consuming tasks without impacting the user experience

Service Mesh
-------------------
- This is a dedicated infra structure layer that handles the communication between microservices.

By Implementing these statergy we can ensure that microservices architecture can scale effectivly to meet the demands of our growing bussiness

26. What is Chaos  Engineering and how it is applied in Microservices?
======================================================
 Chaos  Engineering is a displine that involves interntionally introducing controlled failures into a system to test it resilence and ensure fault tolerance.
 - It is a principle that if we can break our system in a controlled environment, we can identify its weakness and improves its ability to withstand unexpected distruptions.
 Principles of Chaos Engineering
 1. Planning for Failure:
 ---------------------------------
 Before introducing Chaos it is crucial to define the scope of experiment, the types of failures to simulate and the expected outcomes.
 This helps us that the Chaos experiments are meaningful and they provided various insights 
 2. Simulating the real world condition
 --------------------------------------------------
 Chaos experiment should aim to simulate real world failure as close as possible. So this included simulating the netwoek latecny, server crashed, disk failure and other common distruptions that can happen in production environment.
 
 3. Learn and Improves
 --------------------------------
 The result of Chaos experiments should be carefully analized and through this we can identify the weakness in our system and this information can  then be used to improved the design of the system and implement the mitigation statergies and enhace the system resilience.
 
 Tools to implement Chaos Engineering like Chaos Monkey, Gremlin and so on.
 
 Ex: Netflix uses Chaos Monkey to randomly terminates the instances in its productions. By simulating the instance failure that have been identifed and addressed numerious weakness of their system, ensuring that their streaming services remains highly available  and resilient to unexpected distruptions.
 
 27. How do we perform logging in a distributed microservices system?
 ==========================================================
 - Logging a Cornerstone of monitoring , debugging, trobuleshooting in disctributed microservices systems. 
 - It provided valuable insights into the behaviour of indivisual service and then particular interactions.
 - Key considerations for effective Logging in Microservices
 Cenralized Logging
------------------------------
  Cenralized Logging aviods the complexity of managing the logs for multiple microservices independently. So here we have cenralized solutions that enable efficient aggregations, analysis  and visualizations of logs across entire system.
Structural Logging
  -------------------------
  Instead of plain text logs, here we used structured format like JSON or Key value pairs
Traces Id
-------------------
Through Trace Ids, each request should assign unique identifier or trace Id that propagate across all involved services.
This allows us to trace the journey of a request through the entire system making it easier to identify and trobuleshooting issues.
Log Levels 
----------------
We utilize different Log level Debug, Info, Warn, Error, fatal tom control the verbosity of Logs.
Security
------------------
Sensitive information like username, password , apikeys are properly masked or redacted from the logs 

28 What is the Purpose of retry Pattern in Microservices?
===========================================
Retry pattern is used to handle the transient failures in a disctributed microservices architecture.
Transient failures are temporary issues like netwoek glitches, temporary service unavilable or database timeouts that usually resolved themself within a short time period.

2 Purpose:
1. It improves the reliability, so by automatically retrying the failed requests the retry pattern enhances the overall reliability of the system. So it helps ensures operations can be successfully completed even when temporary distruptions occurs.
2. Prevents overloading, Implementing expontially backoff is the key over  here. So it increases the delay between retries with each attempt and this also prevents a flood of retry request from overhelming the failing service duriung a temporary outage.

29. What are Sidecars in Microservices?
====================================
Sidecars Pattern is a design pattern in microervices where a lightweight helper container run alongside the min application conatiner within the same deployment unit ( basically a kubernates Pod).

Responsibility and uses cases of Sidecars
------------------------------------------------------
1. Monitoring and Logging 
2. Network Traffic Management
3. Security
4. Feature Delivery

Ex:- in a payment service, a sidecar conatiner could encrypt sensitive data , collect and forward logs and handle network traffic.

30. What are the best practices for deploying microervices in prod environment?
================================================================
To Deploy microservices effectively in a production environment requires careful planning and a roboust approach.
 Containerization
 -------------------------
 We package each microservice into its own container like by using docker and this provided isolation, portability and consistency across different environments.
 Orchestration: here utilizating conatiner orchestration platform like kubernates to manage the deployment scaling and networking of containers.
 CICD(Contineous Intergration and Contineous Deployment)
 ----------------------------------------------------------------------------------
 Automate the build, test and deployment process using the CICD pipelines. This ensure faster and more frequent releases with reduce manual effort.
 Deployment Startergy
 --------------------------------
 We can follow different deployment statergies like Blue-green deployment, Canary releases, ab testing and so on.
 Monitoring and observability
 ----------------------------------------
 Here we implement centralized logging to collect and analyze logs from all of the microservices. So this helps in trobuleshooting issues and identifying the performance bottlenecks.
 Service Discovery
 --------------------------
 This enables services to dynamically discover and locate each other within the network. So this enhances the flexibility and simplifes the service interactions.
 Security
 ---------------
 We concept like Authentication and Authorization, data encryptions, regular security audits and so on.


# API Versioning and REST APIs

API versioning is a standard practice used to manage changes in an API over time without breaking existing client applications. Many different types of APIs, including those designed with the **REST** (Representational State Transfer) architectural style, employ versioning strategies to balance stability and innovation.

### Common REST API Versioning Strategies

When developing a REST API, developers can choose from several methods to implement versioning.

*   **URI Path Versioning**: This involves including the version number directly in the endpoint's URL (e.g., `https://api.example.com/v1/products`). It is straightforward and easy to understand but can lead to URL clutter as the API evolves.
*   **Query Parameter Versioning**: The version is passed as a query parameter (e.g., `https://api.example.com/products?version=1`). This keeps the base URL cleaner but might be less intuitive for consumers.
*   **Custom Header Versioning**: A custom HTTP header, such as `X-API-Version`, is used to specify the desired API version. This keeps the URI clean and aligns well with some REST principles, but requires clients to manage extra headers.
*   **Content Negotiation (Media Type Versioning)**: This advanced method uses the HTTP `Accept` header to indicate the desired representation of the resource, often involving a custom vendor-specific media type that includes the version (e.g., `Accept: application/vnd.example.v1+json`). This is considered by some to be the most "RESTful" approach as it versions the resource's representation rather than its address.

By using versioning, API providers can introduce new features, fix bugs, or change data structures (known as "breaking changes") while allowing existing clients to continue using the older, stable version until they are ready to upgrade.























