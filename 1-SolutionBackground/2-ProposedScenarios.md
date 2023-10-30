# Proposed Scenarios

## User

### Login

User login flow to access the platform.

```mermaid
flowchart TD
    First[User has account]
    Login(User login)

    First --> |yes| Login
    First --> |no| Registry
    Registry --> Login
```

### Update camera config

Update camera configuration if existing or register a new camera if missing.

```mermaid
flowchart TD
    App(Initial page)
    All(See all cameras)
    Single(Single camera)
    Register(Register camera)

    App --> All
    All --> Single
    App --> Register
```

### Upload data

Data can be uploaded automatically via a desktop application or manually.

The user will go into the wilderness to get their SD card and either bring an alternative SD card with a new configuration or read it on the spot with a laptop.

The dataset can be retrieved from the SD card using generic file-system readers. 

Users can upload the dataset and/or the occurrences log to Wildlife Watcher platform for downstream tasks.

```mermaid
flowchart TD
    GetPhysicalData(Get physical camera)
    UploadToPlatform(Upload to Wildlife Watcher platform)
    ImportImages(Import animal detection clips to platform's datasets)
		ImportDetections(Import animal detection logs to platform's observations)

    GetPhysicalData --> UploadToPlatform
		UploadToPlatform --> |capture mode enabled| ImportImages
		UploadToPlatform --> |detection mode enabled| ImportDetections
		

```

### Label data

Once the user uploads their data into the Wildlife Watcher platform, they can link those files to the data annotation tool. After the annotation is done, the output labels are imported back into the platform. 

```mermaid
flowchart TD
    SelectDataset(Select dataset)
    SelectTargettool(Select target tool)
    CheckToolConfig(Check tool configuration)
    AskCredential(Ask credentials)
    SendData(Send/sync data)
    RedirectUser(Redirect the user to the website)
    CollectData(Collect/sync data)
    
    SelectDataset --> SelectTargettool
    SelectTargettool --> CheckToolConfig
    CheckToolConfig --> |credential doesn't exist| AskCredential
    AskCredential --> SendData
    CheckToolConfig --> |credential exist| SendData

    SendData --> RedirectUser
    RedirectUser --> |check in background| CollectData
```

### Model training

After the image data has been annotated (labeled), it is loaded into a model training platform. 

An exported model can be downloaded to user’s computer and placed on the SD card. The camera device can then read the model and use it for detection on next system boot. 

```mermaid
flowchart TD
	Start[Select annotated dataset]
	Link[Link the annotated dataset to the model training platform]
	TrainBranch[Was a model already trained?]
	Train[Train a model with a new architecture]
	FineTune[Fine-tune an existing model]
	Evaluate[Evaluate the new model on test dataset]
	Export[Export the model in the format for target platform]

	
	Start --> Link
	Link --> TrainBranch
	TrainBranch --> |No| Train
	TrainBranch --> |Yes| FineTune
	Train --> Evaluate
	FineTune --> Evaluate
	Evaluate --> Export

```

### Deploy camera

Once the model has been trained and exported from the platform, the user needs to place it in the SD card before loading it onto the camera. 

```mermaid
flowchart TD
	Connect[Connect the Wildlife Watcher camera to computer]
	Dowload[Download exported model to user's computer]
	Place[Place the model onto the SD card for next]
	UpgradeIf[Does the camera firmware need an upgrade?]
	Upgrade[Upgrade the firmware of the camera]
	Deploy[Apply changes to the camera and place it in wilderness again]

	Connect --> Dowload
	Dowload --> Place
	Place --> UpgradeIf
	UpgradeIf --> |Yes| Upgrade
	UpgradeIf --> |No| Deploy
	Upgrade --> Deploy
```

### iNaturalist User Authorisation

How users are authorised via iNaturalist

```mermaid
flowchart
    Start --> U(Redirect user to iNaturalist)
    U --> Auth{User authorizes our app?}
    Auth --> |No| Reject(Show failure page)
    Auth --> |Yes| Redirect(Redirect to app with a 'code')
    Redirect --> GetToken(Get 'access token' from 'code')
    GetToken --> AuthEnd[Authorisation completed]
```

### Publish to GBIF

How user can publish their frames to GBIF

```mermaid
flowchart
    Start --> U(User sends a 'publish to GBIF' request)
    U --> AskCredentials(App asks user to provide their GBIF credentials)
    AskCredentials --> Creds{User provided the credentials?}
    Creds --> |No| Reject[Reject user's request]
    Creds --> |Yes| Publish[App publishes the frames to GBIF on behalf of the user]
```

## Camera

### Check for updates

The next cycle waiting time is defined on the camera

```mermaid
flowchart TD
    CheckUpdate[Check for update]
    ApplyChanges(Apply changes)
    EndCycle(End of cycle)

    Start --> CheckUpdate

		CheckUpdate --> |new update| ApplyChanges
		CheckUpdate --> |no updates or no internet| EndCycle
    ApplyChanges --> EndCycle
    EndCycle --> |wait next cycle| CheckUpdate
```

### Capture animal

This only happens if the camera/detection is enabled

If the camera is operating in the “capture” mode, the SD card will store video clips of 5-10sec for every motion detection event. 

```mermaid
flowchart TD
    Movement(Movement sensor)
    ML(Run machine learning model)
    SaveSD[Save to SD card / Metadata + Data]
    CheckSettings(Check notification settings)
    SendNotification(Send notification)
    EndCycle[End detection cycle]

    Start --> Movement
		Movement --> |trigger| ML

    ML --> |if enabled| SaveSD
    SaveSD --> EndCycle

    ML --> CheckSettings
    CheckSettings --> |enabled| SendNotification
    SendNotification --> EndCycle

    CheckSettings --> |disabled| EndCycle

    EndCycle --> Movement
```

### Device monitoring

To monitor the health of the device itself, the following flow describes the steps the camera does to report health status to the platform. 

```mermaid
flowchart TD
    CheckConfig[Check if heath check notifications are enabled]
    SendStatus(Apply changes)
    EndCycle(End of cycle)

    Start --> CheckConfig

		CheckConfig --> |yes| SendStatus
    SendStatus --> EndCycle
		CheckConfig --> |no| EndCycle
    EndCycle --> |wait next cycle| CheckConfig
```
