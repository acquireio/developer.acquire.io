# One Click Button

> Start video, audio and chat support with one click of button.

Copy the code on the right inside the body tag to customize a quick connection to support.

## Methods

|  Method |  Parameters |  Type |  Description |
| :--- | :--- | :--- | :--- |
|  max\(\) |  video |  _`String`_ |  Starts a video call with widget maximized |
|  | audio | _`String`_ |  Starts a audio call with widget maximized |
|  | text | _`String`_ |  Starts a text chat with widget maximized |

### Sample Code to embedd \( for video call \)

```text
<a href="javascript:acquireIO.max('video')"> Start Video Call Now </a>
```

### Sample Code to embedd \( for audio call \)

```text
<a href="javascript:acquireIO.max('audio')"> Start Audio Call Now </a>
```

### Sample Code to embedd \( for text chat \)

```text
<a href="javascript:acquireIO.max('text')"> Start Text Chat Now </a>
```

## Quick Chat Link for Specific Agent

 To make a custom link to initiate chat with specific agent, use the following code to generate link.

### Embedd Code For Text Chat

```text
<a href="javascript:acquireIO.max('text',AGENT_ID)">Start the Chat</a>
```

####  **Get AGENT\_ID**

 First login [Acquire dashboard](https://app.acquire.io/)  and open **Agents** and copy specific **`agent ID`**.

{% file src="../../.gitbook/assets/get-agent-id-1.png" caption="Get AGENT\_ID" %}



