# Requirement For Acquire

### Client Requirements <a id="client-requirements"></a>

Web browser support for the Acquire app:

* Chrome \(Latest version\*\)
* Firefox \(Latest version\*\)
* Safari 10 and later
* Internet Explorer 11.0+
* Microsoft Edge

Web browser support for the Acquire Messenger:

* Chrome \(Latest version\*\)
* Firefox \(Latest version\*\)
* Safari 8 and later
* Internet Explorer 11.0+
* Microsoft Edge

{% hint style="info" %}
Important: We don't support web sockets on older versions of Internet Explorer.
{% endhint %}

* **Acquire Conversations for iOS:** Requires iOS 10.0 or later.
* **Acquire Messenger for iOS:** Requires iOS 8.0 or later.
* **Acquire Conversations for Android:** Requires Android API 21 \(5.0\) or later.
* **Acquire Messenger for Android:** Requires Android API 15 \(4.0.3\) or later.

If you find that you are using an outdated browser, you can upgrade it here. If you find issues in any of our supported browsers, please let us know by mailing us at [hello@acquire.io](../../rest-apis/profiles-api/sender-emails.md).

we only support the latest versions of Chrome and Firefox.

### Network Requirements:

* Ports 443,80
* Protocols: HTTP, HTTPS, WebSocket
* Domains: app.acquire.io, s.acquire.io, media.acquire.io, cdn.acquire.io, [fonts.gstatic.com](http://fonts.gstatic.com/) [unpkg.com](http://unpkg.com/),[ cdn.acquire.io](http://cdn.acquire.io/), [apis.google.com](http://apis.google.com/) , [fonts.googleapis.com](http://fonts.googleapis.com/),[ fonts.gstatic.com](http://fonts.gstatic.com/), [cdn.polyfill.io](http://cdn.polyfill.io/), [maxcdn.bootstrapcdn.com](http://maxcdn.bootstrapcdn.com/), [cdnjs.cloudflare.com](http://cdnjs.cloudflare.com/)

if you want to enable video call, voice call, and screen sharing then add following firewall rules :

{% hint style="info" %}
Port: 443 and 80 on TCP and UDP **turn.acquire.io**
{% endhint %}

if you have enabled recording in your account then must allow following firewall rules :

{% hint style="info" %}
Port 80 and 443 for **rcdn.acquire.io**
{% endhint %}

\(Must be FQDN-based whitelisting not IP based\)

### TLS/SSL Best Practices:

We will update our TLS/SSL configuration from time to time and consider best practices / recommendations on a case by case basis. We err on the side of ensuring that communicating with Acquire is always secure, and so our TLS/SSL configuration may result in older or manually configured clients not being able to talk to Acquire. We announce TLS/SSL configuration changes as a "Product Update" in the Intercom application and for additional information about our TLS/SSL configuration please see our security page.

