# 010 - Use a queue on Camera Integration Service container (1)

## Status

Accepted

## Context

Before sending messages (push notifications) to users, messages from cameras must be enriched and select which user should receive it based on the user configuration.

The selection of user is a slower then receiving data, and can be a bottleneck in case of huge input.

## Evaluation Criteria

- Scalability/Elasticity - the system must handle many messages in parallel
- Reliability - messages from inside the platform cannot be lost
- Resource usability - resource efficient

## Decision

Use a message queue between the API (producer) and the service (consumer) that enriches and select user. 

## Implications

### Positive

- In case of input bigger than output, is possible to scale the consumer keeping the resource-usage low.
- Messages will be consumed

### Negative

- Having two services instead of one (a producer and consumer)