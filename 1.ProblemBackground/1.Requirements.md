# Requirements

## Engagement Models

### Users

**Description:** Biologists and nature enthusiasts around the globe.

Receive reports near-real time or identified species in specific locations.

Organize collected in a uniform pattern way across multiple projects.

### Community

**Description:** community members from external communities, like iNaturalist and GBIF.

They can take advantage of discoveries and experiments from Wildlife users.

## Architecturally significant business requirements

### 1. Update camera config by an app

An online system must be present in order to connect mobile app and cameras.

### 2. External integration

Integration with external tools is required, so an integration token (or any other authentication token) must be stored in the system.

### 3. Store big amount of data from users

The system must store a large amount of data.

Data includes:

- Photos and video from cameras
- Labelled photos and videos from 3rd party tools
- Trained models

### 4. Reports near real-time

Cameras should report to users once they identify a species.

## Significant Non-Functional requirements

The system must be built from scratch so it doesn’t need to integrate into an existing solution.