## StopCapture Directive
**Sample Message**
```
{
    "directive": {
        "header": {
            "namespace": "SpeechRecognizer",
            "name": "StopCapture",
            "messageId": "{{STRING}}",
            "dialogRequestId": "{{STRING}}"
        },
        "payload": {
        }
    }
}
```
## ExpectSpeech Directive
**Sample Message**
```
{
    "directive": {
        "header": {
            "namespace": "SpeechRecognizer",
            "name": "ExpectSpeech",
            "messageId": "{{STRING}}",
            "dialogRequestId": "{{STRING}}"
        },
        "payload": {
            "timeoutInMilliseconds": {{LONG}},
            "initiator": {
                "type": "{{STRING}}",
                "payload": {
                    "token": "{{STRING}}"
                }
            }
        }
    }
}
```
## ExpectSpeechTimedOut Event
**Sample Message**
```
{
    "event": {
        "header": {
            "namespace": "SpeechRecognizer",
            "name": "ExpectSpeechTimedOut",
            "messageId": "{{STRING}}",
        },
        "payload": {
        }
    }
}
```