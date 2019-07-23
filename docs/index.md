# Overview

We provide 3 interfaces for the client to interact with our cloud.

###Websocket Interface
```
Endpoint : ws://api.fpt.io:8080
```
This is stream interface for client upload voice stream to Rogo cloud, Rogo cloud will process voice stream and return action to the client like play music, audiobook, ...

###MQTT Interface
```
Endpoint : tcp://mqtt.fpt.io:1883
```
The client must connect to MQTT interface to received command from cloud such as alarm, notify, ... and send events to cloud such as user push next, back button,...

###HTTP Interface
Build later !

## Events
When client connect to cloud there are two kind of events between them

* Event send from client to cloud such as push voice button, volume up, volume down,...
* Event send from cloud to client, call directive such as event play audio, event speak text to speak,...