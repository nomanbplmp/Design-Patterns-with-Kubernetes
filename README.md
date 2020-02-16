# Kubernetes Patterns and their application

1. **Side Car Pattern**

    The sidecar pattern is a singlenode pattern made up of two containers. 
    The first is the application container. It contains the core logic for the application. Without this container, 
    the application wouldnot exist. In addition to the application container, there is a sidecar container. The role
    of the sidecar is to augment and improve the application container, often without the
    application container’s knowledge. In its simplest form, a sidecar container can be
    used to add functionality to a container that might otherwise be difficult to improve
    
    Applications of side car pattern:
    
      - Shipping application logs to External logging system
      - Adding Https to a legacy http application
      - Adding Dynamic configuration to Application
      - Creating Platform as a service 

2. **Amabassador Pattern**

   Ambassador container brokers interactions between the application container and the rest of the world.
   The value of the ambassador pattern is twofold. First, as with the other single-node
    patterns, there is inherent value in building modular, reusable containers. The separa‐
    tion of concerns makes the containers easier to build and maintain. Likewise, the
    ambassador container can be reused with a number of different application contain‐
    ers. This reuse speeds up application development because the container’s code can be
    reused in a number of places. Additionally the implementation is both more consis‐
    tent and of a higher quality because it is built once and used in many different con‐
    texts
    
    Application of Ambassador pattern:
      
      - Creating Sharding service
      - System to perform Service Discovery
      - Request Splitting
     
3. **Adapter Pattern**
  In the adapter pattern, the
  adapter container is used to modify the interface of the application container so that it
  conforms to some predefined interface that is expected of all applications. For exam‐
  ple, an adapter might ensure that an application implements a consistent monitoring
  interface. Or it might ensure that log files are always written to stdout or any number
  of other conventions.
     
        
  Application of Adapter pattern:
    - Monitoring
    - Logging
    - Request/Response Converter

