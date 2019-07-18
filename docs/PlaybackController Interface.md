## PlayCommandIssued Event
The `PlayCommandIssued` event must be sent when user press on-client starts/resumes button.  

**Sample Message**
```
{
    "context": [
        ...     
    ],   
    "event": {
        "header": {
            "namespace": "PlaybackController",
            "name": "PlayCommandIssued",
            "messageId": "{{STRING}}"
        },
        "payload": {
        }
    }
}
```
**Header Parameters** 

| Parameter | Description | Type |
| ------------ | ------------- | ------------ |
| messageId | A unique ID used to represent a specific message.  | string |  

## PauseCommandIssued Event
The `PauseCommandIssued` event must be sent when user press on-client pause button.  

**Sample Message**
```
{
    "context": [
        ...      
    ],    
    "event": {
        "header": {
            "namespace": "PlaybackController",
            "name": "PauseCommandIssued",
            "messageId": "{{STRING}}"
        },
        "payload": {
        }
    }
}
```
**Header Parameters** 

| Parameter | Description | Type |
| ------------ | ------------- | ------------ |
| messageId | A unique ID used to represent a specific message.  | string |  

## NextCommandIssued Event
The `NextCommandIssued` event must be sent when user press on-client next button, the cloud will send the next media item to the client if the client context has the next item.     

**Sample Message**
```
{
    "context": [
        ...     
    ],     
    "event": {
        "header": {
            "namespace": "PlaybackController",
            "name": "NextCommandIssued",
            "messageId": "{{STRING}}"
        },
        "payload": {
        }
    }
}
```
**Header Parameters** 

| Parameter | Description | Type |
| ------------ | ------------- | ------------ |
| messageId | A unique ID used to represent a specific message.  | string |  

## PreviousCommandIssued Event
The `PreviousCommandIssued` event must be sent when user press on-client previous button, the cloud will send the previous media item to the client if the client context has the previous item. 

**Sample Message**
```
{
    "context": [
        ...       
    ],     
    "event": {
        "header": {
            "namespace": "PlaybackController",
            "name": "PreviousCommandIssued",
            "messageId": "{{STRING}}"
        },
        "payload": {
        }
    }
}
```
**Header Parameters** 

| Parameter | Description | Type |
| ------------ | ------------- | ------------ |
| messageId | A unique ID used to represent a specific message.  | string |  