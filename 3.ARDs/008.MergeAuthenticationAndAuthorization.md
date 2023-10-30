# 008 - Merge authentication and authorization

## Status

Accepted

## Context

Authentication tells who the user is. Authorization tells what the user can do.

## Evaluation Criteria

- Simplicity - how easy is it to implement

## Decision

Merge authentication and authorization into a single service, once separating it adds unnecessary overhead.

## Implications

### Positive

- Services can consume the same place for authentication and authorization

### Negative

- Increase the coupling between authentication and authorization