# Mobile APIs

**Base URL** : `https://api.fpt.io/rest/mobile`

**Header** : `"Authorization": "Bearer {{AccessToken}}"`

## API stop music

**Path** : `/stop`

**Method** : `POST`

**Auth required** : `YES`

**Request** :

```json
{
    "device_id":"{{long}}"
}
```

**Response** :

```json
{
    "status": "{{int}}",
    "message":   "{{string}}",
    "timestamp": "{{string}}",
}
```

## API pause music

**Path** : `/pause`

**Method** : `POST`

**Auth required** : `YES`

**Request** :

```json
{
    "device_id":"{{long}}"
}
```

**Response** :

```json
{
    "status": "{{int}}",
    "message":   "{{string}}",
    "timestamp": "{{string}}",
}
```

## API next music

**Path** : `/next`

**Method** : `POST`

**Auth required** : `YES`

**Request** :

```json
{
    "device_id":"{{long}}"
}
```

**Response** :

```json
{
    "status": "{{int}}",
    "message":   "{{string}}",
    "timestamp": "{{string}}",
}
```

## API back music

**Path** : `/previous`

**Method** : `POST`

**Auth required** : `YES`

**Request** :

```json
{
    "device_id":"{{long}}"
}
```

**Response** :

```json
{
    "status": "{{int}}",
    "message":   "{{string}}",
    "timestamp": "{{string}}",
}
```

## API change volume

**Path** : `/volume`

**Method** : `POST`

**Auth required** : `YES`

**Request** :

```json
{
    "device_id":"{{long}}",
    "volume" : "{{int}}"
}
```

**Response** :

```json
{
    "status": "{{int}}",
    "message":   "{{string}}",
    "timestamp": "{{string}}",
}
```

## API get battery

**Path** : `/battery?device_id={device_id}`

**Method** : `GET`

**Auth required** : `YES`

**Request** : 

Query param :
```
    "device_id":"{{long}}"
```
**Response** :

```json
{
    "status": "{{int}}",
    "message":   "{{string}}",
    "timestamp": "{{string}}",
    "data" : {
        "value" : "{{INT}}"
    }
}
```
