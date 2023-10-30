# 012 - Manual process on cameras

## Status

Accepted

## Context

Once cameras are deployed, it can be very expensive the change it hardware requirements.

Cameras should be able to work without internet given the location where it is set.

Some manual process, like recharging battery, is already manual.

## Evaluation Criteria

- Configurability - ability to each service (camera) have their own configuration

## Decision

Cameras must have a device interface in which a user can connect and change it configurations.

Users  must be able to get data from it (stored in a SD) and load into a different device (like a laptop).

Users must be able to load data from an external device, like a USB sticky. 

## Implications

### Positive

- Cameras can be configured easily

### Negative

- Manual steps of the user
- Any person can change a camera if they have physical access to it