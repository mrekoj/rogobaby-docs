## Speak Directive
**Sample Message**
```
{
    "directive": {
        "header": {
            "namespace": "SpeechSynthesizer",
            "name": "Speak",
            "messageId": "{{STRING}}",
            "dialogRequestId": "{{STRING}}"
        },
        "payload": {
            "url": "{{STRING}}",
            "format": "{{STRING}}",
            "token": "{{STRING}}"
        }
    }
}
```
## SpeechStarted Event
**Sample Message**
```
{
    "event": {
        "header": {
            "namespace": "SpeechSynthesizer",
            "name": "SpeechStarted",
            "messageId": "{{STRING}}"
        },
        "payload": {
            "token": "{{STRING}}"
        }
    }
}
```
## SpeechFinished Event
**Sample Message**
```
{
    "event": {
        "header": {
            "namespace": "SpeechSynthesizer",
            "name": "SpeechFinished",
            "messageId": "{{STRING}}"
        },
        "payload": {
            "token": "{{STRING}}"
        }
    }
}
```