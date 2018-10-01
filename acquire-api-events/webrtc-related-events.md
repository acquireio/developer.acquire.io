# WebRTC Related Events

Acquire WebRTC related event in you can use multiple events and manage custom easily. When you conect video or voice call after all events call.

### WebRTC Related Events 

**`1. rtcroom-incall: true/false`** Acquire WebRTC event type **`"rtcroom-incall"`** uers  video or voice call  after this api given user's response true or false. if you want to use video or voice call connect and disconnect after action then use this event.

**`2. rtcroom`**

Event **`"rtcroom"`** in two type parameter using first **RTCRoom object**, and second  **RTCRoomUser object**. This event will give **rtcroom object** whenver gets ready and **RTCRoomUse**r which is current's user's object and is responsible for making calls and picking calls.

RTCRoomUser Object RTCRoomUser Object have following methods.

 **status\(\)** : status of call 

**`standby`**: means no call at all 

**`incall`** : we are in call of voice/video call, but we didn't have joined the call yet.

**`joined`** : means we are in call and we've joined call as well

**video\_mute\(\) ;**

**audio\_mute\(\) ;**

Above two functions allow anyone to mute or get status of mute of audio or video. when pass true. it will mute the stream, if pass false, it will unmute stream if passed nothing it will return the state of mute.

**stopRTCCall\(\);**

using this function by apis you can disconnect call.

