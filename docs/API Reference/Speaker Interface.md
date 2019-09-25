## SetVolume Directive

The `SetVolume` directive adjust volume, using scale 0-100

**Sample Message**

```json
{
    "directive": {
        "header": {
            "namespace": "Speaker",
            "name": "SetVolume",
            "messageId": "{{STRING}}",
            "dialogRequestId": "{{STRING}}"
        },
        "payload": {
            "volume": "{{LONG}}"
        }
    }
}
```

**Header Parameters** 

| Parameter | Description | Type |
| ------------ | ------------- | ------------ |
| messageId | A unique ID used to represent a specific message.  | string |  
| dialogRequestId | A unique ID | string |
