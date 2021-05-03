# Microservices approach

Date: 2021-04-29

## Status

Accepted

## Context

We need to decide what the dominating system approach will be. There are several options like: monolith, microservices, 
micro-kernels, modularlized monolith.

### Alternatives

Key map:
- + Promotes
- ++ Strongly promotes
- O Neutral
- - Negative
- -- Strongly negative

| | Monolith | Microservices | Micro-kernel | Modularized Monolith |
|----|----|----|-----|-----|
| Ease of Deployment  | ++ | -  | -  | ++ |
| Availability        | -  | ++ | +  | -  |
| Autonomy            | -- | ++ | ++ | +  |
| Traceability        | ++ | -  | +  | O  |
| Performance         | ++ | ++ | +  | ++ |
| Modifiability       | O  | ++ | +  | +  |
| Maintainability     | -  | ++ | +  | +  |
| Integrity           | ++ | -- | O  | +  |
| Security            | -  | ++ | +  | ++ |
| Scalability         | -- | ++ | -  | +  |

## Decision

Based on alternatives in the context of the business needs, and a development team we think that microservices is 
the best option for now. This will definitely cause some disturbance to business during migration and new process design 
but will pay off in longer term. Further, customer would not need to invest again in Tech stack since we are confident that
new architecture model will resolve the problems.

## Consequences

The main benefits come in the development and deployment area. The team could save a lot or resources setting up 
dev/test/qa/prod environments. The cost of development and cognitive complexity is low level because most of the code base 
has been reused - with minimal changes to the existing sytem.

We believe that with minimal changes to the functional components and some changes to business process will resolve current issues.
