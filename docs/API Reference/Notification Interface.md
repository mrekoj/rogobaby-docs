
## Api send notification from Device to Apps
Send notification from device to all app which this device belongs to.

**URL** : `https://api.fpt.io/notification/api/v1/notification`

**Method** : `POST`

**Auth required** : YES

**Header**
```
    "Authorization": "Bearer {{AccessToken}}",
    "Content-type": "multipart/form-data"
```

**Data constraints**
```json
{
    "device_id_send": "{{int}}",   // device id 
    "user_id": "{{int}}",
    "file": "{{file}}"
}
```

**Success Response**
```json
{
    "assets": {
        "url": "{{string}}"
    },
    "created": "{{datetime}}",
    "device_id_receive": "{{int}}",
    "device_id_send": "{{int}}",
    "id": "{{int}}",
    "user_id": "{{int}}"
}
```

**Sample Success Response**
```json
{
    "assets": {
        "url": "https://s3.amazonaws.com/rogo-speaker/2644345.mp3-787881af"
    },
    "created": "Thu, 25 Jul 2019 04:07:39 GMT",
    "device_id_receive": null,
    "device_id_send": 1,
    "id": 8,
    "user_id": 14
}
```

## Api send notification from Mobile App to Device

Send notification from app to the device.

*note: If have notification from mobile app, device instanly receive [SetIndicator](#event-setindicator-directive) event.

**URL** : `https://api.fpt.io/notification/api/v1/notification`

**Method** : `POST`

**Auth required** : YES

**Header**
```json
{
    "Authorization": "Bearer {{AccessToken}}",
    "content-type": "multipart/form-data"
}
```

**Data constraints**
```json
{
    "device_id_receive": "{{int}}", // device id 
    "user_id": "{{int}}",
    "file": "{{file}}"
}
```
```json
{
    "assets": {
        "url": "{{string}}"
    },
    "created": "{{datetime}}",
    "device_id_receive": "{{int}}",
    "device_id_send": "{{int}}",
    "id": "{{int}}",
    "user_id": "{{int}}"
}
```

**Sample Success Response**
```json
{
    "assets": {
        "url": "https://s3.amazonaws.com/rogo-speaker/2644345.mp3-787881af"
    },
    "created": "Thu, 25 Jul 2019 04:07:39 GMT",
    "device_id_receive": 14,
    "device_id_send": null,
    "id": 9,
    "user_id": 14
}
```
## Api read newest notification

**URL** : `https://api.fpt.io/notification/api/v1/notification/read`

**Method** : `GET`

**Auth required** : YES

**Header**
```json
{
    "Authorization": "Bearer {{AccessToken}}",
    "content-type": "multipart/form-data"
}
```
**URL Params**: `device_id_receive=[integer]`

**Success Response:**
```json
{
    "assets": {
        "url": "https://s3.amazonaws.com/rogo-speaker/2644345.mp3-787881af"
    },
    "created": "Thu, 25 Jul 2019 04:07:39 GMT",
    "device_id_receive": 14,
    "device_id_send": null,
    "id": 9,
    "user_id": 14
}
```
**Error Response:**

- Code 404: NOTFOUND do not have any new notification
```json
{
    "error": "notification not found"
}
```
- Code 401: UNAUTHORIZED wrong access token
```json
{
    "error": "unauthorized"
}
```

## Event SetIndicator Directive

 > Have notification sent from app to device

**Sample Message**
```json
{
    "directive": {
        "header": {
            "namespace": "Notifications",
            "name": "SetIndicator"
        },
        "payload": {
            "asset": {
                "url": "{{STRING}}"
            }
        }
    }
}
```