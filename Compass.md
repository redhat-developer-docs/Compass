# Compass
Compass is an end-to-end architecture guide for building Cloud Native applications the Red Hat Way.

It includes microservices running in Linux containers, Kubernetes, OpenShift, Ansible and many other technologies.  

There is associated code -- an online store -- to demonstrate the architecture.

The first version of the project will be written in Java. After that, subsequent versions will feature other languages: Node.js, Python, .NET (C#, F# and VB), Go, and another others that are relevant.

## Audience
The target audience for this guide is software architects, developers, and C-level executives (CIO, CTO, etc). For architects, this site is a guide to understanding and designing Cloud Native systems. For developers, this site contains both explanations and working code. You won't be left with theories and edicts; you'll be given source code in your language. Finally, for the CIO and CTO audience, this site will give you an overview of some of the benefits and drawbacks of Cloud Native computing, thing necessary in order to decide if your organization should venture down this path.

## Why this guide?  
Software development is no longer an isolated function. As cloud computing becomes ubiquitous and a commodity, and as systems and teams are becoming more frequently distributed, it becomes crucial that vendor and software selections not only work well, but that they work well together.  

Understanding this, Red Hat has put together this web site in order to help developers down the path of both least resistance and greatest value toward cloud native software success.  

The Red Hat way of development is centered around the concept of cloud computing, and is not limited to any one programming language. While the languages used in this guide are limited (Java for now; node, Go, Python and C# later), the concepts are not. Any developer of any language discipline can profit from this site.

## How This Site Is Organized
This site has two distinct but related sections: The Architectural Blueprint and the Example Application.  

The first section (Architectural Blueprint) describes Red Hat opinionated approach to developing cloud native applications. In this section you will find descriptions and explanations for all things related to cloud native applications, including management considerations, technologies, business needs, etc. Some parts of the section will be language-neutral, while some topics may include language-specific instructions or technologies. Overall, the Architectural Blueprint is the How And Why of cloud native development the Red Hat way.

The second section (Example Application) provides a life-like example of an application that is developed following the guidelines, technologies and disciplines established in the first section. The application, Coolstore, was developed by Red Hat specifically for this purpose, and highlights the best practices and leading technologies for cloud native development. This section is very language-specific; Java is the supported language at this time, with examples coming for Python, Go, Node.js, and the .NET languages (C#, F#, and VB).

## What is Cloud Native Computing?
Cloud Native computing is more than simply running an application on a VM that is hosted off premises. The Cloud Native Computing Foundation describes it thusly:
>Cloud native computing uses an open source stack to be:
>1. Containerized. Each part (applications, processes, etc) is packaged in its own container. This facilitates reproducibility, transparency, and resource isolation.
>2. Dynamically orchestrated. Containers are actively scheduled and managed to optimize resource utilization.
>3. Microservices oriented. Applications are segmented into microservices. This significantly increases oerall agility and maintainability of applications.


## Benefits of Cloud Native Computing
Like any change in the software development landscape, cloud native has both plusses and negatives. Having knowledge of these characteristics can help avoid surprises and disappointments while at the same time helping one position their organization to reap the most benefits from cloud native. Some of the benefits of cloud native computing include:

### Lower Cost  
Cloud native computing can yield cost savings in many ways.
- Simply switching to an open source development model will mean a reduction or elimination of software licensing costs.
- Small microservices mean no more support tickets, eliminating an entire system and the associated administrative costs.

### Speed to deployment
- Small, simple and easy-to-understand microservices, with promises but no coupling, can quickly be changed and deployed.
- Automated (scripted) pipelines reduce human interaction and make things faster. 
- Managed and automated deployments mean you can introduce new code with no downtime and much less risk. These two characterists combine to create a confidence and atmosphere where speed is welcomed and not feared.

### Global scale (e.g. CDNs)
Software that operates on a global scale, or even if merely a continent-sized scale (e.g. it is an online store that operates in the United States), cloud computing benefits by making resources closer to their use, reducing latency. Software running at multiple data centers and Content Delivery Networks (CDNs) allow intelligent routers to find the fastest response, which is most frequently the closest hardware. In those situations where the closest hardware is not the fastest, intelligent routing can find the next fastest solution. Distributed hardware means a better chance of finding the fastest solution.

### Reliability
Systems fail. Networks are fragile. In fact, the eight fallacies of distributed computing lists network unreliability as number one. So how why is reliability a benefit?  

Because we can anticipate and plan for the unreliable parts: networks, latency, and bandwidth. In the last 1980s, when midrange computers ruled the enterprise, the idea was to make hardware that wouldn't fail. When hardware became a commodity in the late 1990s, it ushered in an era of *expecting* and *responding to* failure.

Now, when networks or systems fail, we can quickly detect the event act on it by redirecting traffic, provisioning new VMs or containers, and creating software that provides a service despite being "broken". Monitoring, tracing, auto-scaling, circuit breakers; these technologies (and more) work together to make an unreliable network appear reliable.

## ____ as a Service
Infrastructure, Platform, Software, Database ... these (and more) "as a Service" offerings are all a part of Cloud Native Computing. The benefit of this is that you can select which level of completeness you wish; what starting point suits your needs, desires, or budget.

Infrastructure will provide virtual machines (VMs) and networking. Platform provides an operating environment on top of the infrastructure (e.g. OpenShift). Software is a product that you use, such as Basecamp.

The tradeoffs include cost and customization, but the "as a Service" hierarchy allows you to select your starting point based on your needs.

## Public, Private, Hybrid
Hosting software and data in your on-premises servers, on a hosted solution, or a combination of the two, is a key advantage. The ability to locate computing and storage where you want it is an important benefit of cloud native computing. Security, speed, and even legal issues can be reasons that dictate where you store data and computing. In the best implementations of cloud native computing, not only can applications be moved between private and public servers, it can be moved between -- or spread across -- multiple hosting solutions. The ability to move from, say, Amazon Web Services to Azure, is one of the "holy grails" of cloud native computing.


## The many parts of a microservice
### Small teams
One of the most notable characteristics of a microservice done right is the idea of a small team that owns the application. The "two pizza team" idea from Amazon depicts this idea: A team small enough to be fed with two pizzas. The team _owns_ a microservice, from design to coding to deployments, to support. The team size isn't really the issue here; it's about the team having autonomy and accountability. Autonomy to select their programming language and coding style and standards; accountabililty in that they are responsible for the success of the microservice.

Implemented correctly, this concept of a small (tiny?) team will result in a fast-acting, cohesive unit with an entrepreneurial mindset. If this is not the case, you're doing it wrong.

### Domain Driven Design
Domain Driven Design (DDD) is, in simple terms, the idea that a system design based on the underlying domain, i.e. the real-world "thing" being modeled. For example, an inventory control system is built over the inventory control domain. It does not concern itself with the sales system or the purchasing system. It does provide services that those and other systems can use, but they are not the concern of the inventory system per se. This design methodology results in distinct systems with fewer complexities. This idea of keeping things separated is known as a Bounded Context.

### Bounded Context

### Fault-resilient infrastructure
### API Gateway
### Promises
### Monitoring
### Tracing
### Logging
### Fault tolerance/acceptance
### Continuous Integration
### Continuous Delivery
### Service discovery
### Automation
### Scalability
### Containers
### Load Balancing
### DevOps structure/mentality
### Data

## Where To Start?  
Green field or legacy?
### Adding to a legacy system, AKA the "Strangler" pattern 

### Developing a new ("Green field") application
#### Start with monolith or microservices?

## Our Reference Implementation: Brewery

## Sidecars

