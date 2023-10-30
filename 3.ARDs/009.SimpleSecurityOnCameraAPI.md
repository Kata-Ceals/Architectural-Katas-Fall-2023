# 009 - Simple security on camera API

## Status

Accepted

## Context

Cameras are considered external resources and don’t have stable and reliable internet connection.

Cameras must have access to the platform, via an API, and it must be validated to have a basic security.

## Evaluation Criteria

- Feasibility - be doable to be done

## Decision

Generate an unique token per camera, that must be set on each camera as a hard-coded value. Each camera’s request must contains the token and messages with invalid token will be ignored.

## Implications

### Positive

- Have a basic security level
- Way to identify cameras in a trustful approach

### Negative

- Cameras with same token will generate invalid/incoherent data