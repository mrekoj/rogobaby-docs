
# Stream API

## Websocket API for recognize voice

```
Endpoint : ws://api.fpt.io:8080&token=
```

**token:** client can get token when connect to FPT OAuth server  
In test enviroment, client can pass value 1 to token.  

When connect to websocket endpoint client send audio chunk to the endpoint using 16 kHz, mono, 16bit little-endian format, size of the audio chunk is 320 bytes.  

If the client detects silent or user unleash voice command button, then the client must send **"EOS"** signal(in bytes) to cloud.

## Websocket API for upload file

```
Endpoint : ws://api.fpt.io:8080&token={token}&deviceId={deviceId}&userId={userId}
```

- **token**    : OAuth2 token
- **deviceId** : id of device upload file
- **userId**   : id of user
- **type**     : ="" or not append -> recognize voice to text; = 1 -> upload file

Client stream array of byte data to endpoint, when finish client must send **"EOS"** signal(in bytes) to cloud.

Cloud will response result in MQTT

## HTTP API

HTTP API using for upload voice file to cloud.  

Build later...
