# Sender Emails

Acquire live chat dashboard gives your team leader an overview of agent activity at any given time.

Acquire Profiles Sender Emails API header in Content-Type application/x-www-form-urlencoded send.

| Parameter | Value |
| :--- | :--- |
| **Path** | https://app.acquire.io/setting/email-setting |
| **Method** | POST |
| **Authorization** | Bearer **\[YOUR\_API\_AUTH\_TOKEN\]** |
| **Content-type** | application/x-www-form-urlencoded |

#### **Response JSON**

```javascript

{
    "success": true,
    "error": null,
    "data": {
        "total": 1,
        "data": [
            {
                "id": 15416,
                "sender_email": "johndeo@gmail.com",
                "sender_name": "John Deo",
                "type": "user",
                "is_active": "1",
                "is_default": "1",
                "date_created": "2018-04-17 06:12:58"
            }
        ]
    }
}

```

#### **Sample Code**

{% tabs %}
{% tab title="Node" %}
```javascript
 var http = require("http");

	var options = {
		"method": "POST",
		"hostname": [
			"app",
			"acquire",
			"io"
		],
		"path": [
			"profile",
			"setting",
			"email-setting"
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

	req.end();
```
{% endtab %}

{% tab title="PHP" %}
```javascript
 $curl = curl_init();

	curl_setopt_array($curl, array(
		CURLOPT_URL => "https://app.acquire.io/profile/setting/email-setting",
		CURLOPT_RETURNTRANSFER => true,
		CURLOPT_ENCODING => "",
		CURLOPT_MAXREDIRS => 10,
		CURLOPT_TIMEOUT => 30,
		CURLOPT_HTTP_VERSION => CURL_HTTP_VERSION_1_1,
		CURLOPT_CUSTOMREQUEST => "POST",
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

		url = URI("https://app.acquire.io/profile/setting/email-setting")

		http = Net::HTTP.new(url.host, url.port)

		request = Net::HTTP::Post.new(url)
		request["Authorization"] = 'Bearer [YOUR_API_AUTH_TOKEN]'
		request["Content-Type"] = 'application/x-www-form-urlencoded'

		response = http.request(request)
	puts response.read_body
```
{% endtab %}

{% tab title="cURL" %}
```javascript
curl --request POST \
		--url 'https://app.acquire.io/profile/setting/email-setting' \
		--header 'Authorization: Bearer [YOUR_API_AUTH_TOKEN]'\
		--header 'Content-Type: application/x-www-form-urlencoded'
```
{% endtab %}

{% tab title="jQuery" %}
```javascript
var settings = {
		"async": true,
		"crossDomain": true,
		"url": "https://app.acquire.io/profile/setting/email-setting",
		"method": "POST",
		"headers": {
			"Authorization": "Bearer [YOUR_API_AUTH_TOKEN]",
			"Content-Type": "application/x-www-form-urlencoded"
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

		url = "https://app.acquire.io/profile/setting/email-setting"

		headers = {'Authorization: Bearer [YOUR_API_AUTH_TOKEN]','Content-Type': 'application/x-www-form-urlencoded'}

		response = requests.request("POST", url, headers=headers)

	print(response.text)
```
{% endtab %}
{% endtabs %}

