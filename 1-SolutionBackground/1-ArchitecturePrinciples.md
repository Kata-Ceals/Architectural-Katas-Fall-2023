# Architecture principles

Principles that should be applied in the overall architecture of the project.

| Principle              | Reason                                                             | Outcomes                                                            |
| ---------------------- | ------------------------------------------------------------------ | ------------------------------------------------------------------- |
| Availability           | - Cameras can send data at any time                                | - System always up and running                                      |
|                        | - Users from around the globe (access at any time)                 |                                                                     |
| Reliability            | - Multiple users                                                   | - Users will have access only to their resources                    |
| Scalability/Elasticity | - Multiple users in parallel                                       | - System can handle multiple data at the same time                  |
|                        | - Multiple cameras sending data in parallel                        | - Less resources are used when there is no high-traffic             |
| Security               | - Password and integration tokens will be stored in the platform   | - Secured system                                                    |
| Extendability          | - New functionality and integrations can be present in the future  | - Enable future improvements in the system                          |
| Modularity             | - Services and components must be modular                          | - Improvement/changes can be done without touching the whole system |
| Maintainability        | - Support is done by volunteers with different levels of expertise | - System will                                                       |
| Responsiveness         | - Notifications must reach users near real-time                    | - Users will be informed faster                                     |
| Data integrity         | - Data will be erased from SD once is uploaded                     | - Data will be present on the platform once is uploaded             |