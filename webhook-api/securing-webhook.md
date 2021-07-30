# Securing Webhook

#### Securing Webhook and Signature Hash validation <a id="securing-webhook-and-signature-hash-validation"></a>

When a webhook is configured, a unique signature key is generated and given in the webhook response. The value of this header is an HMAC-SHA256. This signature key is used to sign the webhook payloads, which are sent to your endpoint with the signature key name `x-acquire-signature`.

[See the Getting Started Guide in our Help Docs.](https://help.acquire.io/for-developers/hmac-for-webhooks)

**Your HMAC/Secret Key**

When you create a new webhook you have to allocate/add HMAC/Secret Key.

**Verify Signature -**

All outbound requests keep a hash authenticated header key using the standard SHA256 hash in the header `x-acquire-signature`. To verify the signature on your server generate a SHA256 hash and compare it with the hash sent in the Acquire header `x-acquire-signature`. You will need the HMAC/Secret Key that you provided in the webhook creation.

**Verify Signature example nodejs code:**

```text
validateSignature = (secret, body, signature) => {
    // Create a SHA256 hashed code using the HMAC/Secret key and update the hash with body using utf8
    var signatureComputed = crypto.createHmac('SHA256', secret).update(
        new Buffer(JSON.stringify(body), 'utf8')).digest('hex');
    return (signatureComputed === signature);
};
```

