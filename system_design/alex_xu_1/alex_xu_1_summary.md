# Tech Summary of Alex Xu's System Design Volumen 1

## Chapter 1: 

### web: 

* frontend/mobile, backend, RESTful API

* data type: HTML, json

### Network Infra:

* DNS, https, IP address; RESTful API

* loadbalancer, public ip, private ip

* geoDNS-routed

### DB:

* SQL DB

* Non SQL DB: key-value stores, graph stores, column stores, and document stores

* Database replication

* Database scaling: Vertical Scaling vs Horizontal Scaling (Sharding)

### Micro Services Components:

* Message Queue: Asynchronous Communication

### Vertical scaling vs horizontal scaling

* Vertical Scaling

* Horizontal Scaling: LoadBalancer

* web, data, and cache tiers

* Stateless web tier

### Logging, metrics, automation

### Issues 

* availability: failover 

### Failures 

* SPOF: A single point of failure (SPOF) 
