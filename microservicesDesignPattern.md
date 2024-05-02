# 1.Circuit Breaker Pattern:
Description: The Circuit Breaker pattern is used to prevent a cascading failure of services. If a service fails, the circuit breaker prevents subsequent calls to the service for a predefined amount of time.<br/>

How it works:<br/>
The circuit breaker monitors the number of failures when calling a service.<br/>
If the number of failures exceeds a predefined threshold, the circuit breaker "trips" and prevents further calls to the service for a specified period.<br/>
After the specified period, the circuit breaker allows a limited number of requests to see if the service has recovered.<br/>


Benefits:<br/>
Prevents cascading failures<br/>
Improves system stability and resiliency<br/>


# 2. API Gateway Pattern:
Description: The API Gateway pattern provides a single entry point for clients to access various microservices. It is responsible for routing requests, handling authentication, and enforcing policies such as rate limiting and caching.<br/>
How it works:<br/>
Clients send requests to the API Gateway, which forwards them to the appropriate microservice.<br/>
The API Gateway may also aggregate multiple requests into a single request, reducing the number of round trips between the client and server.<br/>
Benefits:<br/>
Simplifies client access to microservices<br/>
Centralized management of cross-cutting concerns like authentication and rate limiting<br/>
Can improve performance by reducing the number of client-server round trips<br/>

# 3.Service Registry Pattern:
Description: In a microservices architecture, services are dynamically created and destroyed. The Service Registry pattern involves using a service registry (such as Netflix Eureka, Consul, or Zookeeper) to keep track of the location and availability of services.<br/>
How it works:<br/>
When a service starts up, it registers itself with the service registry.<br/>
Clients looking to use a service query the service registry to discover available instances of the service.<br/>
The client can then communicate with the discovered service instance directly.<br/>
Benefits:<br/>
Dynamic service discovery<br/>
Load balancing<br/>
Fault tolerance<br/>
# 4. Service Discovery Pattern:<br/>
Description: The Service Discovery pattern allows services to find and communicate with each other without needing to know the network location of the other services.<br/>
How it works:<br/>
Services register with a service discovery tool, which maintains a dynamic directory of available services.<br/>
When a service needs to communicate with another service, it queries the service discovery tool to find the network location of the required service.<br/>
The client can then communicate with the discovered service.<br/>
Benefits:<br/>
Decouples service communication from network locations<br/>
Simplifies service deployment and scaling<br/>
