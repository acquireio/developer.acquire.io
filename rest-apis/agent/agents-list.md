# Agents List

Using acquire agent API for agents all details and get activities. You can do setup acquire backend on your own dashboard easily use this. Agent List API in all agents details available. Acquire Agent List API in you can get agent's **`'secret_key'`** and use anywhere but make sure secure this.

#### **Get Auth Token**

We provide an Access Token as soon as you create an app on your workspace. First login Acquire dashboard and Go **Setting &gt; API Token and Whitelist &gt; API Token** \( [https://app.acquire.io/setting/token](https://app.acquire.io/setting/token) \). Copy API token and use API header in **`auth_token`** parameter. If you want to new token generate click on button "**Generate New Token**".

![](../../.gitbook/assets/api-auth-token-1.png)

Your Access Token can give access to your private Acquire data and should be treated like a password. **If an app provider asks you for your Access Token, please do not provide it. Instead, let us know - apps are required to use OAuth rather than asking users for Access Tokens.**

{% hint style="danger" %}
 **API auth token  \[YOUR\_API\_AUTH\_TOKEN\]  do not use  public and make sure secure.**  
{% endhint %}

{% hint style="success" %}
If you want to use auth token in API for makes a own dashboard then save anywhere secure and use server side.
{% endhint %}

![](../../.gitbook/assets/image%20%281%29.png)

| Parameter | Value |
| :--- | :--- |
| **Path** | https://app.acquire.io/api/account/agents |
| **Method** | POST |
| **Authorization**  | **Bearer \[YOUR\_API\_AUTH\_TOKEN\]** |
| **Content-type** | application/json |

#### **Body \(**row**\)**

```javascript
{"page":1,"limit":25,"sort_by":{"key":"","order":""}}
```

#### **Response JSON**

```javascript
{
    "success": true,
    "error": null,
    "data": {
        "rows": [
            {
                "id": 14755,
                "user_id": 15022,
                "account_id": 10111,
                "user_name": "David",
                "user_email": "davidklok@acquire.io",
                "allowed_ip": "",
                "role": 1,
                "role_name": "Administrator",
                "role_status": "active",
                "user_status": "active",
                "secret_key": "[SECRET KEY]",
                "user_type": "Zapier",
                "department_id": null,
                "department_name": null
            }
        ],
        "count": 1,
        "page": 1,
        "limit": 25
    }
}

```

#### **Sample Code**

{% tabs %}
{% tab title="PHP" %}
```php
$curl = curl_init();

curl_setopt_array($curl, array(
  CURLOPT_URL => "https://app.acquire.io/api/account/agents",
  CURLOPT_RETURNTRANSFER => true,
  CURLOPT_ENCODING => "",
  CURLOPT_MAXREDIRS => 10,
  CURLOPT_TIMEOUT => 30,
  CURLOPT_HTTP_VERSION => CURL_HTTP_VERSION_1_1,
  CURLOPT_CUSTOMREQUEST => "POST",
  CURLOPT_POSTFIELDS => "{"page":"","limit":"","sort_by":{"key":"","order":""}}",
  CURLOPT_HTTPHEADER => array(
    "Authorization: Bearer [TOKEN]",
    "Content-Type: application/json",
  ),
));

$response = curl_exec($curl);
$err = curl_error($curl);

curl_close($curl);

if ($err) {
  echo "cURL Error #:" . $err;
} else {
  echo $response;
}
```
{% endtab %}

{% tab title="Ruby" %}
```javascript
require 'uri'
require 'net/http'

url = URI("https://app.acquire.io/api/account/agents")

http = Net::HTTP.new(url.host, url.port)

request = Net::HTTP::Post.new(url)
request["Authorization"] = 'Bearer [TOKEN]]'
request["Content-Type"] = 'application/json'
request.body = "{\"page\":\"\",\"limit\":\"\",\"sort_by\":{\"key\":\"\",\"order\":\"\"}}"

response = http.request(request)
puts response.read_body

```
{% endtab %}

{% tab title="cURL" %}
```javascript
curl -X POST \
  https://app.acquire.io/api/account/agents \
  -H 'Authorization: Bearer [TOKEN]' \
  -H 'Content-Type: application/json' \
  -d '{"page":"","limit":"","sort_by":{"key":"","order":""}}'
```
{% endtab %}

{% tab title="jQuery" %}
```javascript
 var settings = {
  "async": true,
  "crossDomain": true,
  "url": "https://app.acquire.io/api/account/agents",
  "method": "POST",
  "headers": {
    "Authorization": "Bearer [TOKEN]",
    "Content-Type": "application/json",
  },
  "processData": false,
  "data": "{\"page\":\"\",\"limit\":\"\",\"sort_by\":{\"key\":\"\",\"order\":\"\"}}"
}

$.ajax(settings).done(function (response) {
  console.log(response);
});
```
{% endtab %}

{% tab title="Python" %}
```javascript
import requests

url = "https://app.acquire.io/api/account/agents"

payload = "{\"page\":\"\",\"limit\":\"\",\"sort_by\":{\"key\":\"\",\"order\":\"\"}}"
headers = {
    'Authorization': "Bearer [TOKEN]]",
    'Content-Type': "application/json",
    }

response = requests.request("POST", url, data=payload, headers=headers)

print(response.text)
```
{% endtab %}

{% tab title="Node" %}
```javascript
var request = require("request");

var options = { method: 'POST',
  url: 'https://app.acquire.io/api/account/agents',
  headers: 
   {'Content-Type': 'application/json',
     Authorization: 'Bearer [TOKEN]' },
  body: { page: '', limit: '', sort_by: { key: '', order: '' } },
  json: true };

request(options, function (error, response, body) {
  if (error) throw new Error(error);

  console.log(body);
});

```
{% endtab %}
{% endtabs %}



