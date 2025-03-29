
# Horizontal & Vertical Scaling

## Explanation

### 1. Top-Down Steps for System Design
- **Identify core functions:** Start by identifying the core functions the system must perform.  
- **Group related functions:** Form collections of related functions into clusters of microservices.  
- **Create architecture diagram:** Visualize the connections between these microservices.  
- **Dive deeper into each microservice:**  
  - Sketch the structure without considering scalability at first.  
  - Identify non-functional requirements, including capacity needs.  
  - Plan how to scale each component.  
  - Design a distributed system for each layer, ensuring redundancy and reliability.  

---

### 2. Reasons to Choose a Distributed System
- **Data Volume:** Essential for handling large data volumes, scaling the database, and caching layers.  
- **High Throughput:** Ensures the system can handle a high number of requests per second.  
- **Response Time:** Quick responses are achieved by parallelizing computations.  
- **Reliability:** Maintains system availability despite failures.  
- **Geolocation:** Reduces latency by using multiple servers across regions.  
- **Hotspots:** Avoids traffic congestion by distributing the data load.  

---

### 3. Vertical Scaling (Scaling Up)
- **Definition:** Adding more resources to a single machine (like increasing CPU, RAM, or storage).  
- **Shared Memory Architecture:** Multiple CPUs access a common memory pool.  
- **Downsides:**  
  - Increased cost with diminishing returns.  
  - Physical limitations when adding more resources.  

---

### 4. Horizontal Scaling (Scaling Out)
- **Definition:** Adding more machines rather than upgrading a single one.  
- **Shared Nothing Architecture:** Each machine works independently without shared memory.  
- **Benefit:** Suitable for distributing the workload across multiple instances.  

---

## Fun Analogy
**Scaling is like hosting a pizza party!**  
- **Vertical Scaling:** Ordering one giant pizza with extra toppings. It’s more expensive and eventually too large to manage.  
- **Horizontal Scaling:** Ordering multiple smaller pizzas and distributing them among guests. Easier to handle and can scale up if more guests arrive.  

---

## Mnemonic
**"Great Cats Always Play Joyfully"**  
- **G - Gather functional requirements:** Identify what the system needs to do.  
- **C - Choose distributed over monolithic:** Enhances scalability and performance.  
- **A - Add resources vertically or horizontally:** Scaling up or scaling out.  
- **P - Prevent hotspots by distributing:** Spread traffic to avoid congestion.  
- **J - Just don’t overdo vertical scaling:** Costs increase, and there are physical limits.  

---

## Interview Questions with Answers

### 1. What are the main steps involved in the top-down system design approach?  
**Answer:**  
1. Gather functional requirements.  
2. Cluster related functions into microservices.  
3. Draw an architecture diagram to visualize connections.  
4. Dive into each microservice to analyze structure, non-functional requirements, and scalability.  

---

### 2. Why would you choose a distributed system over a monolithic one?  
**Answer:**  
Distributed systems enhance scalability, reliability, and performance. They efficiently handle large data volumes, high throughput, low latency (geolocation), and fault tolerance, while monolithic systems may become bottlenecks as they scale.  

---

### 3. What is the difference between vertical and horizontal scaling, and when would you use each?  
**Answer:**  
- **Vertical Scaling:** Adding more power to one machine (CPU, RAM). Suitable for performance upgrades within existing infrastructure.  
- **Horizontal Scaling:** Adding more machines to handle increased load. Ideal for distributed systems needing high availability.  

---

### 4. How do you address hotspots when scaling a distributed system?  
**Answer:**  
Distribute the load evenly across servers or partitions, use caching strategies, and implement data sharding to balance traffic.  

---

### 5. What are the limitations of vertical scaling in a large-scale system?  
**Answer:**  
Vertical scaling has physical and cost limitations. As resources increase, costs rise disproportionately, and there is a point where adding more power does not significantly improve performance.  

---

