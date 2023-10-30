# 011 - Integration containers database

## Status

Accepted

## Context

Integration container must contain a Database to store API token and any other needed information from external tools.

## Evaluation Criteria

- Extendability - how easy is to add new integrations

## Decision

Use a Document database, like MongoDB.  

## Implications

### Positive

- For being schemaless document databases don’t need to have rely on schema migrations