# Triggers List

Using this api for get acquire app in created all triggers list.

| Parameter | Value |
| :--- | :--- |
| **Path** | https://app.acquire.io /account/triggers/list |
| **Method** | POST |
| **Authorization** | Bearer \[YOUR\_API\_AUTH\_TOKEN\] |
| **Content-type** | application/x-www-form-urlencoded |

**Body**

| Parameter | Value |
| :--- | :--- |
| **Page** | 1 |
| **Limit** | 10 |

**Response JSON**

```javascript

{
    "success": true,
    "error": null,
    "data": {
        "rows": [
            {
                "total": 13,
                "id": 15624,
                "status": "disable",
                "name": "Dialog Flow Bot Test",
                "account_id": 15,
                "date_start": null,
                "type": "web",
                "date_end": null,
                "opened": 0,
                "clicked": 0,
                "replied": 0,
                "ac_name": "John Deo"
            },
            {
                "total": 13,
                "id": 15209,
                "status": "active",
                "name": "FB Test Bot",
                "account_id": 15,
                "date_start": null,
                "type": "web",
                "date_end": null,
                "opened": 0,
                "clicked": 0,
                "replied": 0,
                "ac_name": "John Deo"
            }
        ],
        "count": 13,
        "page": 1,
        "limit": 10
    }
}

```

**Sample Code**

{% tabs %}
{% tab title="PHP" %}
```javascript
$curl = curl_init();

    curl_setopt_array($curl, array(
        CURLOPT_URL => "http://app.acquire.io/account/triggers/list",
        CURLOPT_RETURNTRANSFER => true,
        CURLOPT_ENCODING => "",
        CURLOPT_MAXREDIRS => 10,
        CURLOPT_TIMEOUT => 30,
        CURLOPT_HTTP_VERSION => CURL_HTTP_VERSION_1_1,
        CURLOPT_CUSTOMREQUEST => "POST",
        CURLOPT_POSTFIELDS => "page=1&limit=10&search=",
        CURLOPT_HTTPHEADER => array(
        "Authorization: Bearer [YOUR_API_AUTH_TOKEN]",
        "Content-Type: application/x-www-form-urlencoded"
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

    url = URI("http://app.acquire.io/account/triggers/list")

    http = Net::HTTP.new(url.host, url.port)

    request = Net::HTTP::Post.new(url)
    request["Authorization"] = 'Bearer [YOUR_API_AUTH_TOKEN]'
    request["Content-Type"] = 'application/x-www-form-urlencoded'
    request.body = "page=1&limit=10&search="

    response = http.request(request)
    puts response.read_body
```
{% endtab %}

{% tab title="cURL" %}
```javascript
curl --request POST \
        --url 'http://app.acquire.io/account/triggers/list' \
        --header 'Authorization: Bearer [YOUR_API_AUTH_TOKEN]' \
        --header 'Content-Type: application/x-www-form-urlencoded' \
        --data 'page=1&limit=10&search='
```
{% endtab %}

{% tab title="jQuery" %}
```javascript
var settings = {
        "async": true,
        "crossDomain": true,
        "url": "http://app.acquire.io/account/triggers/list",
        "method": "POST",
        "headers": {
            "Authorization": "Bearer [YOUR_API_AUTH_TOKEN]",
            "Content-Type": "application/x-www-form-urlencoded"
            },
        "data": {
            "page": "1",
            "limit": "10",
            "search": ""
            }
        }

    $.ajax(settings).done(function (response) {
      console.log(response);
    });
```
{% endtab %}

{% tab title="Python" %}
```javascript
import requests

    url = "http://app.acquire.io/account/triggers/list"

    payload = "page=1&limit=10&search="
    headers = {'Authorization': 'Bearer [YOUR_API_AUTH_TOKEN]'}
    headers = {'Content-Type': 'application/x-www-form-urlencoded'}

    response = requests.request("POST", url, data=payload, headers=headers)

    print(response.text)
```
{% endtab %}

{% tab title="Node" %}
```javascript
var qs = require("querystring");
    var http = require("http");

    var options = {
        "method": "POST",
        "hostname": [
			"app",
			"acquire",
			"io"
    ],
        "path": [
            "account",
            "triggers",
            "list"
        ],
        "headers": {
            "Authorization": "Bearer [YOUR_API_AUTH_TOKEN]",
            "Content-Type": "application/x-www-form-urlencoded"
        }
    };

    var req = http.request(options, function (res) {
    var chunks = [];

    res.on("data", function (chunk) {
        chunks.push(chunk);
    });

    res.on("end", function () {
        var body = Buffer.concat(chunks);
        console.log(body.toString());
    });
    });

    req.write(qs.stringify({ page: '1', limit: '10', search: '' }));
    req.end();
```
{% endtab %}
{% endtabs %}

