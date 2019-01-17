# Profile Visit History

Acquire live chat dashboard gives your team leader an overview of agent activity at any given time.

Acquire Profile Visit History API body parameter in add id and header in Authorization: Bearer \[YOUR\_API\_AUTH\_TOKEN\] and Content-Type application/x-www-form-urlencoded send.

| Parameter | Value |
| :--- | :--- |
| **Path** | https://app.acquire.io/profile/lead/visits |
| **Method** | POST |
| **Authorization** | Bearer **\[YOUR\_API\_AUTH\_TOKEN\]** |
| **Content-type** | application/x-www-form-urlencode |

#### **Body**

| Parameter | Value |
| :--- | :--- |
| id | 186 |

#### **Response JSON**

```javascript

{
    "success": true,
    "error": null,
    "data": []
}

```

#### **Sample Code**

{% tabs %}
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
			"profile",
			"lead",
			"visits"
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

	req.write(qs.stringify({ id: '186' }));
	req.end();
```
{% endtab %}

{% tab title="PHP" %}
```javascript
 $curl = curl_init();

	curl_setopt_array($curl, array(
		CURLOPT_URL => "https://app.acquire.io/profile/lead/visits",
		CURLOPT_RETURNTRANSFER => true,
		CURLOPT_ENCODING => "",
		CURLOPT_MAXREDIRS => 10,
		CURLOPT_TIMEOUT => 30,
		CURLOPT_HTTP_VERSION => CURL_HTTP_VERSION_1_1,
		CURLOPT_CUSTOMREQUEST => "POST",
		CURLOPT_POSTFIELDS => "id=186",
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

		url = URI("https://app.acquire.io/profile/lead/visits")

		http = Net::HTTP.new(url.host, url.port)

		request = Net::HTTP::Post.new(url)
		request["Authorization"] = 'Bearer [YOUR_API_AUTH_TOKEN]'
		request["Content-Type"] = 'application/x-www-form-urlencoded'
		request.body = "id=186"

		response = http.request(request)
		puts response.read_body
```
{% endtab %}

{% tab title="cURL" %}
```javascript
curl --request POST \
		--url 'https://app.acquire.io/profile/lead/visits' \
		--header 'Authorization: Bearer [YOUR_API_AUTH_TOKEN]' \
		--header 'Content-Type: application/x-www-form-urlencoded' \
		--data id=186
```
{% endtab %}

{% tab title="jQuery" %}
```javascript
var settings = {
		"async": true,
		"crossDomain": true,
		"url": "https://app.acquire.io/profile/lead/visits",
		"method": "POST",
		"headers": {
			"Authorization": "Bearer [YOUR_API_AUTH_TOKEN]",
			"Content-Type": "application/x-www-form-urlencoded"
		},
		"data": {
			"id": "186"
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

		url = "https://app.acquire.io/profile/lead/visits"

		payload = "id=186"
		headers = {'Authorization': 'Bearer [YOUR_API_AUTH_TOKEN]','Content-Type': 'application/x-www-form-urlencoded'}

		response = requests.request("POST", url, data=payload, headers=headers)

	print(response.text)
```
{% endtab %}
{% endtabs %}

