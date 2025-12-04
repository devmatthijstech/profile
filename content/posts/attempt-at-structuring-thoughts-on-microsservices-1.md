---
title: "Attempt at Structuring Thoughts on Microsservices: part 1"
date: 2025-12-04T21:52:18+01:00
draft: true
tags: ["microservices", "architecture"]
---

{{<lead>}}
What happens if you deploy a Microservice with downtime. And other Microservices with high traffic call this Microservice via HTTP? And how could you solve it?
{{</lead>}}

## Services calling services
{{<mermaid>}}
graph LR;
    A["Api Gateway"]-->|HTTP|B["Microservice A"];
    B-->|HTTP|C["Microservice B"]
{{</mermaid>}}

So in this hypothetical case we have an API Gateway that routes requests to Microservice A. Microservice A in turn calls Microservice B via HTTP. And clients go through the API gateway.

Let's assume:
- For the API gateway it is perfectly fine when we deploy Microservice A, since that is able to do a deployment with zero downtime. Requests simply are slowly migrated via a load balancer to the new version of A.
- We only have this load balancer at the edge of our system, since adding load balancers between all microservices would add a lot of complexity. We're not ready to introduce Kubernetes with a full fledged service mesh, we currently don't have the knowledge and capacity in our company.
- Microservice B has to do a release where zero downtime is not possible.

The effect for http request in flight from 

## Thoughts In Progress
- Mark Richards on Service Granularity and forces that might motivate you to merge or split up services.
 https://www.youtube.com/watch?v=cFooOjUNRXc&t=1110s
- Horrible scenario of services-calling-services.
- Udi Dahan - benefits of messaging and doing request response not through http. HTTP is for clients only.
- https://learn.microsoft.com/en-us/dotnet/architecture/microservices/architect-microservice-container-applications/communication-in-microservice-architecture#asynchronous-microservice-integration-enforces-microservices-autonomy
  - the downsides of using http between microservices

![helpful](images/posts/architectural-modularity-mark-richards.png)
![helpful 2](images/posts/architectural-modularity-mark-richards.png)