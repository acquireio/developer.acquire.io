# Authorization

All requests to Acquire's API require an **API\_KEY**. Authentication is provided by the API\_KEY. To create or delete an API\_KEY, log in to Acquire and go to**`Settings > For Developers > API Key`**  
  
**Authentication example**  
Include this HTTP header for each API request:

`Authorization: Bearer ${API_KEY}`

**Header Name:** Authorization  
**Header Value:** Bearer {{API\_KEY}}

Note: _Please make sure there is a space between the Bearer and API KEY._

### **Sample Code**

```javascript
curl --request GET 'https://{{account_id}}.acquire.io/api/v1/account/department' \
--header 'Authorization: Bearer ${API_KEY}'
```

### **How to Generate an API\_KEY**

{% hint style="danger" %}
Make sure you have the necessary permissions to generate an **API\_KEY**.
{% endhint %}

Follow the steps to generate an API\_KEY:

1. Log in to your Acquire account.
2. Navigate to `Settings > For Developers > API Key`.
3. Click on 'Create API Key' and enter a token name and select your token permissions.
4. Click on 'Next'. An API\_KEY will be generated.
5. Copy the API\_KEY and secure it in a safe location. You will not be able to display it again if you misplace it.
6. Once done, close the menu.

![Settings &amp;gt; For Developers &amp;gt; API Key](../.gitbook/assets/apikey.gif)

{% hint style="warning" %}
#### Save Your API\_KEY

There is no way to display your API\_KEY after closing the menu. Secure it in a safe location before exiting the screen.
{% endhint %}

{% hint style="success" %}
All API requests must be over HTTPS. 
{% endhint %}

### Revoking an API KEY __

Following steps to revoke API Key

1. Log in to your Acquire account.
2. Navigate to `Settings > For Developers > API Key`
3. In the 'Action' column, click on the ellipsis \('...'\) and select 'Delete'.
4. A confirmation will display. Click on 'Delete API Key' to delete the key.

![Delete API KEY](../.gitbook/assets/delete-api-key.gif)

{% hint style="danger" %}
### Delete Carefully

Deleting an API\_KEY cannot be undone, so delete with caution.
{% endhint %}

