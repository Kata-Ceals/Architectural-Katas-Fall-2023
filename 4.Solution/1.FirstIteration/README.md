# First iteration

## Goal

1. Deliver a minimum viable product (MVP) that touches all requirements.
2. Address the short-term business requirements.

The first iteration is focused on delivering a system in which the user can:

- Register cameras
- See cameras’ config and status (like battery and notifications)
- Update camera config
- Store datasets
- Label datasets
- Train ML models based on dataset

(*) The mentioned data is:

- Videos and photos
- Labelled photos and videos
- Trained models

## Requirements and solutions

| Requirement | Solution |
| --- | --- |
| Users should be able to communicate with the camera using a mobile app (to set the cameras on/off and adjust settings without opening the cameras) | Mobile App |
| Users should be able to analyse the videos using common camera trap labelling platforms (https://wildlifeinsights.org/, https://wildeyeconservation.org/traptagger or https://gitlab.com/oscf/trapper-project) | Trigger integration using WebApp |
| Users should be able to publish frames from the videos to https://www.inaturalist.org/ for experts to help with the identification of the species | Trigger integration using WebApp |
| Users should be able to easily train edge models. using their own labelled videos, and upload the models to the cameras (using third-party services like https://roboflow.com/, https://edgeimpulse.com/ or https://www.tensorflow.org/lite) | Trigger integration using WebApp |
| Users should be able to publish the species occurrences to https://www.gbif.org/ the https://camtrap-dp.tdwg.org/ | Trigger integration using WebApp |
| Cameras should be able to process the footage on the device and send a small alert message to the users via LoraWan, 3G or satellite. | Push notifications |

## Assumptions

Related ADRs:

- ADR-009
- ADR-012

Some assumptions are made for the iteration:

- The first camera setup must be done manually and the user must add some data, like a security token
- Cameras can be configured manually via a device interface - like a USB
    - The process of taking pictures of the camera (SD or any other storage) are made exclusive by the user, and the user is responsible for updating this data in the platform.
    - The process of updating the model of the camera is made exclusive by the user via any camera device interface.

## C4 Models

The C4 models are described under C4 models folder.

### Main tasks:

Related ARDs:

- ADR-003
- ADR-004
- ADR-005
- ADR-006
- ADR-007
- ADR-012
- ADR-013
- ADR-014

**Task list:**

- Mobile app to interact with cameras
    - Users can register themselves
    - List cameras and their details
    - Add new camera
    - Change camera config
    - Receive push notifications
- WebApp in which:
    - Users can upload or download dataset (raw dataset, labelled, or ML models)
    - The user can trigger integrations (Wildlife Insights, Edge Impulse, iNaturalist, GBIF)
- Created described services list on C4 models
