# Considerations and Data Criticality

Overview of data criticality and project considerations.

## Considerations

- Cameras don’t need to stream or send photos/videos over the internet - this data will be stored on an SD and requires manual step
- Uploading the model through the internet can be not doable given the lack of internet.
- The camera already has manual steps, like getting data from SD and charging batteries.
- Cameras will have access to the internet, when available.

## Data criticality

| Data type | Criticality  | Observation |
| --- | --- | --- |
| Video and photos on camera | Critical | Must be always available |
| Videos and Photos on platform | Critical | Must be always available |
| Labelled data | Critical | Must be always available |
| Trained models | Critical | Must be always available |
| Notifications from cameras | Low | can be not available because of the internet in the wild |