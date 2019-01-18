# Triggers Detail

Trigger all details get using this api and trigger id send in body.

| Parameter | Value |
| :--- | :--- |
| **Path** | https://app.acquire.io /api/account/triggers/edit |
| **Method** | POST |
| **Authorization** | Bearer \[YOUR\_API\_AUTH\_TOKEN\] |
| **Content-type** | application/x-www-form-urlencoded |

**Body**

| Parameter | Value |
| :--- | :--- |
| **id** | 14339 |

#### **Response JSON**

```javascript

{
    "success": true,
    "error": null,
    "data": {
        "id": 15624,
        "account_id": 15,
        "name": "Dialog Flow Bot Test",
        "status": "disable",
        "title_enable": "yes",
        "keep_enable": "yes",
        "order": 0,
        "date_start": null,
        "date_end": null,
        "matching_rules": "all",
        "type": "web",
        "opened": 0,
        "clicked": 0,
        "replied": 0,
        "_old_id": null,
        "account_trigger_flter": [
            {
                "id": 23141,
                "when": "match",
                "trigger_id": 15624,
                "account_id": 15,
                "output": "apply_chatbot",
                "output_data": "93",
                "status": "active"
            }
        ],
        "account_trigger_rule": [
            {
                "id": 27348,
                "trigger_id": 15624,
                "account_id": 15,
                "input": "page_url",
                "input_data": "s/[YOUR_ACCOUNT_ID]?page=features",
                "condition": "match",
                "status": "active",
                "extra_fields": ""
            }
        ]
    }
}

```

**Sample Code**

{% tabs %}
{% tab title="PHP" %}
```javascript
$curl = curl_init();

	curl_setopt_array($curl, array(
		CURLOPT_URL => "https://app.acquire.io/account/triggers/edit",
		CURLOPT_RETURNTRANSFER => true,
		CURLOPT_ENCODING => "",
		CURLOPT_MAXREDIRS => 10,
		CURLOPT_TIMEOUT => 30,
		CURLOPT_HTTP_VERSION => CURL_HTTP_VERSION_1_1,
		CURLOPT_CUSTOMREQUEST => "POST",
		CURLOPT_POSTFIELDS => "id=14339",
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

	url = URI("https://app.acquire.io/account/triggers/edit")

	http = Net::HTTP.new(url.host, url.port)

	request = Net::HTTP::Post.new(url)
	request["Authorization"] = 'Bearer [YOUR_API_AUTH_TOKEN]'
	request["Content-Type"] = 'application/x-www-form-urlencoded'
	request.body = "id=14339"

	response = http.request(request)
	puts response.read_body
```
{% endtab %}

{% tab title="cURL" %}
```javascript
curl --request POST \
		--url 'https://app.acquire.io/account/triggers/edit' \
		--header 'Authorization: Bearer [YOUR_API_AUTH_TOKEN]' \
		--header 'Content-Type: application/x-www-form-urlencoded' \
		--data id=14339
```
{% endtab %}

{% tab title="jQuery" %}
```javascript
var settings = {
		"async": true,
		"crossDomain": true,
		"url": "https://app.acquire.io/account/triggers/edit",
		"method": "POST",
		"headers": {
		"Authorization": "Bearer [YOUR_API_AUTH_TOKEN]",
		"Content-Type": "application/x-www-form-urlencoded"
		},
		"data": {
			"id": "14339"
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

		url = "https://app.acquire.io/account/triggers/edit"

		payload = "id=14339"
		headers = {'Authorization': 'Bearer [YOUR_API_AUTH_TOKEN]','Content-Type': 'application/x-www-form-urlencoded'}

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
		"edit"
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

	req.write(qs.stringify({ id: '14339' }));
	req.end();
```
{% endtab %}
{% endtabs %}

