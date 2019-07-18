## Websocket API
```
Endpoint : ws://api.fpt.io:8080&token=
```
**token:** client can get token when connect to FPT OAuth server  
In test enviroment, client can pass value 1 to token.  

When connect to websocket endpoint client send audio chunk to the endpoint using 16 kHz, mono, 16bit little-endian format, size of the audio chunk is 320 bytes.  

If the client detects silent or user unleash voice command button, then the client must send **"EOS"** signal(in bytes) to cloud.

## HTTP API
HTTP API using for upload voice file to cloud.  

Build later...