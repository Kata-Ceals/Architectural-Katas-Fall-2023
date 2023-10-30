# (suggestion) Second iteration

## Production/platform suggestions**:**

### Expand the system

Focus on integration within the platform. As described in ADR-002 this can be revised and priority can change based on the collected feedback.

### Hardware development

Adapting the cameras to different environments might prove challenging, especially for more extreme locations. Moving from ground-dwelling animals across the animal kingdom might unlock unexpected requirements. Having a way to quickly iterate over the camera design can make a huge difference when bringing a hardware product to market. For that, [CELUS](https://www.celus.io/) engineering platform could be of good use. The platform enables you to design electronics faster, find the best-fitting components, and generate schematics & BOM compatible with the industry’s EDA tools. Through CELUS, Wildlife can benefit from the electronics design platform as soon as it launches in Q1 2024.

### W**isdom of the crowd**

In subsequent iterations of the system, using single annotators per model could result in noisy labels (i.e., improperly identified species). This is a common problem with classification categories that are close to each other (i.e., two similar types of insects). To mitigate this problem, a voting mechanism could be used where the community experts could heave their proposals on platforms like iNaturalist, from which the model labels could be built in a probabilistic fashion. Such labels can better capture uncertainty between model detection and a public forum of domain experts is the perfect place to collect such data.

### Train models inside the platform

Use internal flow to train models instead of using external services. This will become more relevant as the automation opportunities grow in scope when the Wildlife Watcher reaches mass adoption. 

### Remote model deployment

To address the immediate product requirements, the system’s architecture is designed to work with removable SD cards from which the camera devices could load the ML models and store any runtime artifacts. This stems directly from the need to run the camera in remote locations where internet connection would not be reliable or present at all. This worst case scenario took precedence when making architectural decision. To improve the UX of the solution, for those scenarios where the connection is more stable, the model and firmware updates could be sent over the internet. 

This feature is heavily dependent on user research and feedback and until verified should be treated as a product hypothesis. 

### Wildlife analytics

Current architecture proposal anticipates large number animal of observations stored in database optimized for time-series analysis. Through it, there architecture could be further evolved to support advanced analytics capabilities, positioning [Wildlife.ai](http://Wildlife.ai) as the go-to solution for wildlife monitoring.
