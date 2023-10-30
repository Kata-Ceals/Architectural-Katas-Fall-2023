# 001 - ADR template

## Status

Accepted

## Context

In order to use ADR, we need to come up with the required fields.

## Evaluation Criteria

- Simplicity - how simple is it to fill the ADR
- Completeness - all necessary points are there

## Options

- Do not follow templates

| Criteria | Score | Rationale |
| --- | --- | --- |
| Simplicity | 5/5 | Not following a template is simple  |
| Completeness | 1/5 | It can lead to missing information |
- [Michael Nygard](https://cognitect.com/blog/2011/11/15/documenting-architecture-decisions)’s template

| Criteria | Score | Rationale |
| --- | --- | --- |
| Simplicity | 4/5 | Very straight-forward fields |
| Completeness | 3/5 | Missing decision making |
- [Jacqui Read](https://github.com/tekiegirl/communicationpatterns/blob/main/assets/ADR-example-decision-making.md)’s template

| Criteria | Score | Rationale |
| --- | --- | --- |
| Simplicity | 3/5 | Very straight-forward fields but with more options then other options |
| Completeness | 5/5 | All expected fields are there |

## Decision

Use Jacqui Read’s template. The template also includes decision-making, when necessary, making it more complete.

The following fields can be present:

- Status: status, it must be one of:  Accepted, Confirmed, Rejected, Superseded, Proposed
- Context: context of the decision
- Evaluation Criteria: which criteria is being used to make the decision
- Options: all options, when applicable
- Decision: the final decision in a text format
- Implications: expected result of it
    - Positive: positive implications
    - Negative: negative implications
- Consultation: people or tools consulted to make the decision

## Implications

### Positive

- Following a template guarantees that all fields will always be filled

### Negative

- Learn the template.