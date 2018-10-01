# WebRTC Related Events

Acquire WebRTC related event in you can use multiple events and manage custom easily. When you connect video or voice call after all events call. RTC Event in chat start after just call **`'rtcroom-incall'`** api. This api in given user's response true or false and default response given false. User receive voice or video call after this API response given true.

### WebRTC Related Events 

**`rtcroom-incall`**: true/false

Acquire WebRTC event type **`'cobrowse-request'`** users request send after call and this API given user's response true or false. if you want to use video or voice call connect and disconnect after action then use this event.

```javascript
<script>
    window.acquire = window.acquire || [];
    window.acquire.push(function(app){
        app.on("rtcroom-incall", function (rtcroom_incall) {
            console.log("rtcroom-incall", rtcroom_incall);
			// response true/false
        });
    });
</script>
```

**`rtcroom`**

Event **`'rtcroom'`** in two type parameter using first RTCRoom object, and second  RTCRoomUser object. This event will given **rtcroom object** whenver gets ready and RTCRoomUser which is current's user's object and is responsible for making calls and picking calls.

```javascript
<script>
    window.acquire.push(function(app){
        app.on("rtcroom", function (rtcroom,rtcroom1) {
            console.log("rtcroom", rtcroom);
            //console only for example
            console.log("rtcroom1", rtcroom1);
        });
    });
</script>
```

#### RTCRoomUser Object

 **`'rtcroom'`** event in second object RTCRoomUser Object available. This object in video or voice call status event available. 

Status three type in divided. first **`'standby'`** mode by default available or second status type **`'incall'`** video or voice call before joined available and last status type **`'joined'`** user call receive time available.

**`status()`** : Status user's video or voice call track and position check. Status three type in divide.

* **`standby`**: This event before call and by default available in object.
* **`incall`** : This event is user's in call video or voice but before call join available.
* **`joined`** : User video and voice call joined after available this event type.

If you want to track call position then use this event status and manage your action.

**`video_mute();`**

**`'video_mute();'`** in pass true then video call mute and this pass false then video call unmute. You can use your action on this event easily.

**`audio_mute();`**

**`'audio_mute();'`** in pass true then audio/voice call mute and this pass false then audio/voice call unmute this is working same as video\_mute. You can use your action on this event easily. When you send true, it will be mute or send false then unmute and if you return send work as same type.

**`stopRTCCall();`**

If you want to disconnect audio or video call then use this function by API and disconnect your call.

