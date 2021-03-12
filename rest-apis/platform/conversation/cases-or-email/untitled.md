# Untitled

{% api-method method="get" host="https://{{account\_id}}.acquire.io/api/v1/mail/add-message?-x-user-type=user" path="" %}
{% api-method-summary %}
Send Email
{% endapi-method-summary %}

{% api-method-description %}

{% endapi-method-description %}

{% api-method-spec %}
{% api-method-request %}
{% api-method-path-parameters %}
{% api-method-parameter name="" type="string" required=false %}

{% endapi-method-parameter %}
{% endapi-method-path-parameters %}

{% api-method-headers %}
{% api-method-parameter name="Authorization" type="string" required=false %}
Bearer {{api\_key}}
{% endapi-method-parameter %}
{% endapi-method-headers %}
{% endapi-method-request %}

{% api-method-response %}
{% api-method-response-example httpCode=200 %}
{% api-method-response-example-description %}

{% endapi-method-response-example-description %}

```
{
    "data": {
        "id": 407,
        "caseMessageId": 407,
        "channelId": null,
        "caseId": 90,
        "inboxId": 1,
        "mailId": 1,
        "type": "message",
        "senderType": "user",
        "senderId": 93,
        "to": [
            {
                "Name": "",
                "Email": "developer@acquire.io"
            }
        ],
        "from": {
            "Name": "test",
            "Email": "surendra@acquire.io",
            "MailboxHash": ""
        },
        "cc": [],
        "bcc": [],
        "reply_to": null,
        "subject": "test",
        "textBody": "test api email\n\nOn Mon, Sep 14 2020, at 05:00 PM<\"surendra@acquire.io\"> wrote:test\n\nOn Mon, Sep 14 2020, at 04:36 PM<\"surendra@acquire.io\"> wrote:yrety",
        "htmlBody": "<div class=\"content-writer\" data-reactroot=\"\">test api email</div><div class=\"acq-content hide\" data-reactroot=\"\"><br><br><div>On Mon, Sep 14 2020, at 05:00 PM&lt;\"surendra@acquire.io\"&gt; wrote:</div><blockquote><div class=\"content-writer\" data-reactroot=\"\">test</div><div class=\"acq-content hide\" data-reactroot=\"\"><br><br><div>On Mon, Sep 14 2020, at 04:36 PM&lt;\"surendra@acquire.io\"&gt; wrote:</div><blockquote>yrety</blockquote></div></blockquote></div>",
        "mailboxMessageId": "0.5345358743514836",
        "messageId": null,
        "mailboxInReplyTo": "<c89eb634-612c-45af-8edf-7e06d425833f@mtasv.net>",
        "originalRecipient": "developer@acquire.io",
        "parentId": 14,
        "attachments": [],
        "dateCreated": "2021-03-12T09:21:20.000Z",
        "dateSeen": null,
        "dateBounce": null,
        "dateFailed": null,
        "dateDelivery": null,
        "seen": "no",
        "isDraft": "no",
        "scheduleAt": "2021-03-12T09:21:20.000Z",
        "meta": null,
        "clickedDate": null,
        "unsubscribeDate": null,
        "appMessageId": null,
        "appThreadId": null,
        "user": {
            "departments": [],
            "roles": [],
            "id": 93,
            "name": "test",
            "firstName": "test",
            "lastName": "",
            "photo": "",
            "email": "",
            "clientId": "",
            "parentId": 0,
            "metaDetails": {
                "isBotClient": false,
                "label": ""
            },
            "type": "user",
            "accessLevel": null
        },
        "sender": {
            "type": "user",
            "id": 93,
            "name": "test",
            "email": "",
            "photo": ""
        },
        "mailMsgId": 13
    }
}
```
{% endapi-method-response-example %}
{% endapi-method-response %}
{% endapi-method-spec %}
{% endapi-method %}

