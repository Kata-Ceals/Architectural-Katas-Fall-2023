# 006 - Choose the first model training integration

## Status

Accepted

## Context

To enable users to use custom machine learning (ML) models for their devices, the platform needs to offer a seamless integration with 3rd party providers. 

## Evaluation Criteria

- Flexibility - anticipate support for different workflows to support business agility
- Simplicity - how easy is it to implement

## Options

See Training tools

## Decision

In order to support business in adjusting their product with enough flexibility, simplicity of usage and variety in configuration options made Edge Impulse the initial model training platform. 
Since model training depends on the labeled datasets and ADR-005 - Choose the first labelling platform integration carries with it a dependency to Google Cloud Platform (GCP), Edge Impulse had the added benefit of consuming datasets from Google Cloud Storage (GCS). 
Additional benefit of this platform is a wide range of target deployments that can be generated for a built model, further supporting flexibility and simplicity during the design of the camera hardware. 

## Implications

### Positive

- Rich set of features for building and managing ML models.
- Versatile data sources enable experimentation during system design.
- Ability to add customer’s deployment targets for custom device architectures
    - Every platform action has accessible API endpoint

### Negative

- Enterprise pricing enabling custom device deployment is on-request and economic feasibility of such platform needs to be confirmed when scaling
