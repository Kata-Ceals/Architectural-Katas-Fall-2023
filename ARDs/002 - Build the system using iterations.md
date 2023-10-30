# 002 - Build the system using iterations

## Status

Accepted

## Context

After analyzing requirements was possible to find the critical parts - especially the ones that are hard to change - like the camera’s hardware.

Building a platform that will deliver all expected features in an automated way is a huge and ambitious project that can take months or years to be finished.

## Evaluation Criteria

- Solving the problem - start solving real-world problems as soon as possible
- Collect feedback - understand how users and the system work better, in order to improve it earlier
- User experience - how good is the experience of the user while using the platform

## Decision

The decision is to deliver the system in smaller chunks (iterations).

The first iteration must focus on parts that are harder to change in the future (hardware) and are based on other parts. The next iterations must be focused on making the user experience as smooth as possible.

The overall architecture must be revisited from time to time (also during iterations) in order to adjust for possible new inputs, requirements or decisions.

## Implications

### Positive

- Delivery value faster for the user
- Get feedback (user and usage) earlier

### Negative

- Bad user experience in the beginning