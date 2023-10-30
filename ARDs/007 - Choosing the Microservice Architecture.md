# 007 - Choosing the Microservice Architecture

## Status

Accepted

## Context

Choosing the right architecture is one of the most important decisions of a system. This decision must be made based on the main architectural characteristics that we’ve chosen for the project. 

## Evaluation Criteria

The most significant architectural characteristics of our system are the following:

- Scalability
- Elasticity
- Evolvability & Extendability
- Responsiveness
- Data Integrity

## Options

|  | Responsiveness | Data Integrity | Scalability | Elasticity | Extendability |
| --- | --- | --- | --- | --- | --- |
| Modular Monolith | Good | Good | Weak | Weak | Weak |
| Microservices | Good | Good | Good | Good | Good |
| Event-driven | Good | Weak | Good | Good | Good |

## Decision

Based on the above analysis, we decided to go with the microservices architecture. 

## Implications

### Positive

- High score on our evaluation criteria

### Negative

- Implementation is a harder because it lacks simplicity. We need to take care of network communication issues between services. Also debugging and testing will be more complex.