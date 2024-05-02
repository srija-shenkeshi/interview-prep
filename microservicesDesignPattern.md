# 1.Circuit Breaker Pattern:
Description: The Circuit Breaker pattern is used to prevent a cascading failure of services. If a service fails, the circuit breaker prevents subsequent calls to the service for a predefined amount of time.


How it works:
The circuit breaker monitors the number of failures when calling a service.
If the number of failures exceeds a predefined threshold, the circuit breaker "trips" and prevents further calls to the service for a specified period.
After the specified period, the circuit breaker allows a limited number of requests to see if the service has recovered.


Benefits:
Prevents cascading failures
Improves system stability and resiliency
