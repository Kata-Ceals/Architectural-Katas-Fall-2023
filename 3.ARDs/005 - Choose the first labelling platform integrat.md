# 005 - Choose the first labelling platform integration

## Status

Accepted

## Context

An integration with at least one labelling platform is needed so users can annotate images/videos from cameras.

## Evaluation Criteria

- Simplicity - how easy is it to implement

## Options

See Analyses of 3rd party tools

## Decision

Integrate with Wildlife Insights as a first labelling platform. The user will have data integrated with the platform but all annotations must be done on Wildlife Inishgts application.

Wildlife Insight was chosen for being a SaaS, which doesn’t increase the complexity of the platform with multiple dimensions.

Note: Comparing Wildlife Insights and TrapTagger have similar features and integration approaches, there is no technical reason for choosing Wildlife Insights over TrapTragger.

## Implications

### Positive

- Easier to implement
- Allows an easier implementation of TrapTagger in the future

### Negative

- GCP integration
