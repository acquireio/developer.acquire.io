---
description: >-
  The webhooks will assist you to subscribe to realtime HTTP notification of
  changes to specific objects that occur during an Acquire account with a
  configured endpoint. Instead of making an API call du
---

# Webhooks

#### Support Format Encoding <a id="configuration-format"></a>

1. JSON
2. XML
3. x-www-form-urlencoded

#### Configuration <a id="configuration"></a>

You can configure a webhook endpoint URL and other settings on the **Settings &gt; For Developers &gt; Webhooks** in your Acquire account.  


#### Securing Webhook and Signature Hash validation <a id="securing-webhook-and-signature-hash-validation"></a>

When a webhook is configured, a unique signature key is generated and given in the webhook response. The value of this header is an HMAC-SHA256. This signature key is used to sign the webhook payloads, which are sent to your endpoint with the signature key name `x-acquire-signature`.  


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

#### Webhook Events <a id="webhook-events"></a>

<table>
  <thead>
    <tr>
      <th style="text-align:left">WEBHOOK TRIGGER EVENTS</th>
      <th style="text-align:left">DESCRIPTION</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td style="text-align:left">Chat status is set to Pending</td>
      <td style="text-align:left">Indicates when chat state is Pending.</td>
    </tr>
    <tr>
      <td style="text-align:left">Chat status is set to Active</td>
      <td style="text-align:left">Indicates when chat state is Active.</td>
    </tr>
    <tr>
      <td style="text-align:left">Chat status is set to Queue</td>
      <td style="text-align:left">Indicates when chat state is Queue.</td>
    </tr>
    <tr>
      <td style="text-align:left">Chat status is set to Closed</td>
      <td style="text-align:left">Indicates when chat state is Closed.</td>
    </tr>
    <tr>
      <td style="text-align:left">Agent Status Change</td>
      <td style="text-align:left">
        <p>This indicates that when an agent&apos;s status is updated,</p>
        <p>these agent status capture</p>
        <p>(available, unavailable,</p>
        <p>Chat-chat channel is turned on,</p>
        <p>Email-email channel is turned on,</p>
        <p>VOIP-VOIP channel is turned on).</p>
      </td>
    </tr>
  </tbody>
</table>

With events, you can filter what kind of events you want to subscribe.

#### List All Webhooks <a id="all-webhook"></a>

Return list of all created Webhooks.

| GET | `https://YOUR_ACCOUNT_ID.acquire.io/api/v1/webhook?limit=20&relations=binding&select=name` |
| :--- | :--- |


| PARAMETERS | VALUE |
| :--- | :--- |
| relations | binding \| hook\_log |
| select | name \| id \| url \| urlSkipSsl \| status \| events \| notificationEmail \| hmacKey \| format \| historyExpires \| type \| userId |

**Example Request**

```text
 
        curl --location --request GET 'https://YOUR_ACCOUNT_ID.acquire.io/api/v1/webhook?limit=20&relations=binding&select=name' \
--header 'Authorization: Bearer ****************************'
```

#### Get a specific webhook <a id="single-webhook"></a>

Return a single webhook object.

| GET | `https://YOUR_ACCOUNT_ID.acquire.io/api/v1/webhook/3?relations=&relations=binding&select=name` |
| :--- | :--- |


| PARAMETERS | VALUE |
| :--- | :--- |
| relations | binding \| hook\_log |
| select | name \| id \| url \| urlSkipSsl \| status \| events \| notificationEmail \| hmacKey \| format \| historyExpires \| type \| userId |

**Example Request**

```text
 
    curl --location --request GET 'https://YOUR_ACCOUNT_ID.acquire.io/api/v1/webhook/3?relations=&relations=binding&select=name' \
--header 'Authorization: Bearer ****************************'
```

#### Create a webhook <a id="post-webhook"></a>

Create a new webhook.

| POST | `https://YOUR_ACCOUNT_ID.acquire.io/api/v1/webhook` |
| :--- | :--- |


**Example Request**

```text
 
     curl --location --request POST 'https://YOUR_ACCOUNT_ID.acquire.io/api/v1/webhook' \
--header 'Authorization: Bearer ****************************' \
--data-raw '{
  "name": "string",
  "url": "https://webhook.site/424f082f-6fe1-4fe5-83ae-f5a8ea02147f",
  "urlSkipSsl": "yes",
  "status": "active",
  "events": [
    {
      "event": "user:case-invite",
      "params": {}
    }
  ],
  "notificationEmail": "user@example.com",
  "hmacKey": "string",
  "format": "application/json",
  "historyExpires": "2020-09-04T13:15:54.789Z"
}'
```

#### Update a webhook <a id="put-webhook"></a>

Update a webhook.

| PUT | `https://YOUR_ACCOUNT_ID.acquire.io/api/v1/webhook/10` |
| :--- | :--- |


**Example Request**

```text
 
 curl --location --request PUT 'https://YOUR_ACCOUNT_ID.acquire.io/api/v1/webhook/10' \
--header 'Authorization: Bearer ****************************'
```

#### Delete a webhook <a id="delete-webhook"></a>

Delete a webhook.

| DELETE | `https://YOUR_ACCOUNT_ID.acquire.io/api/v1/webhook/10` |
| :--- | :--- |


**Example Request**

```text
 
curl --location --request DELETE 'https://YOUR_ACCOUNT_ID.acquire.io/api/v1/webhook/10' \
--header 'Authorization: Bearer ****************************'
```

#### Sample Webhook Data <a id="resp-webhook"></a>

Here is an example of the JSON data object sent at your configured endpoint.

```text
    
{
  "event": "case:status",
  "data": {
    "caseId": "72",
    "status": "closed",
    "fields": {},
    "contact": {
      "id": "5",
      "fields": {
        "name": "Jhon",
        "email": "jhone@test.com",
        "phone": "62626226",
        "city": "",
        "state": "",
        "countryId": "517",
        "ip": "103.156.142.2"
      }
    },
    "messages": [
      {
        "id": "323",
        "channel": "chat",
        "senderId": "5",
        "senderType": "contact",
        "type": "event",
        "message": "This thread has been reactivated.",
        "seen": "yes",
        "dateCreated": "Wed Mar 03 2021 10:19:49 GMT+0000 (Coordinated Universal Time)"
      },
      {
        "id": "324",
        "channel": "chat",
        "senderId": "5",
        "senderType": "contact",
        "type": "message",
        "message": "dasdas",
        "seen": "yes",
        "dateCreated": "Wed Mar 03 2021 10:19:49 GMT+0000 (Coordinated Universal Time)"
      },
      {
        "id": "325",
        "channel": "chat",
        "senderId": "5",
        "senderType": "contact",
        "type": "event",
        "message": "You're being transferred to one of our agents, they'll be with you shortly.",
        "seen": "yes",
        "dateCreated": "Wed Mar 03 2021 10:19:50 GMT+0000 (Coordinated Universal Time)"
      },
      {
        "id": "326",
        "channel": "chat",
        "senderId": "1",
        "senderType": "user",
        "type": "event",
        "message": "Surendra Suthar just joined this thread.",
        "seen": "yes",
        "dateCreated": "Wed Mar 03 2021 10:19:53 GMT+0000 (Coordinated Universal Time)"
      },
      {
        "id": "327",
        "channel": "chat",
        "senderId": "1",
        "senderType": "user",
        "type": "event",
        "message": "The thread has been closed by Surendra Suthar.",
        "seen": "yes",
        "dateCreated": "Wed Mar 03 2021 10:20:23 GMT+0000 (Coordinated Universal Time)"
      }
    ]
  }
}
    
```

