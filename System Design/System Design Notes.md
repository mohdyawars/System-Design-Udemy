## Todos 

- [x] Learn Scalability 
- [x] Make Notes on Scalability 
- [ ] Learn More About Obsidian

## Scalability

#### Motivation 🤓

Traffic on the system never remains same. In search engine some time there is a high spike of traffic some time it is low. So we need to scale our system so that it can increase/decrease its resources according to the requests.

#### Types of Scalability

-  Vertical Scaling
-  Horizontal Scaling

**Vertical Scaling** - *Increasing the system resources like increasing the space, better processor, more RAM*

- Pros
   - Any app can benefit from it.
   - Code changes are not required
   - We can migrate to bigger machine when there is more traffic, we can also migrate to smaller machine when the traffic is less.

- Cons
  - There is a limit to upgrade in vertical scaling that limit is reached very quickly
  - We are locked to single system in case of vertical scaling which cannot provide
   - Fault Tolerance
   - High Availability

**Horizontal Scaling** - *Making a multiple instances of system in this way the system does not get overloaded*

- Pros
   - No limit on scalability
   - We can quickly add/remove machines based on the traffic load
   - If we design correctly system can have Fault Tolerance, High Availability

- Cons
  - Code changes may be required
  - Increased complexity

![[Pasted image 20240630211325.png]]
[[System Design - II]]