# Agents List

Acquire dashboard in created your agents details get in this api.

| Parameter | Value |
| :--- | :--- |
| **Path** | https://app.acquire.io/account/agents |
| **Method** | POST |
| **Content-type** | application/x-www-form-urlencoded |

#### **Body**

| Parameter | Value |
| :--- | :--- |
| **page** | 1 |
| **limit** | 10 |

#### **Response JSON**

```javascript

{
    "success": true,
    "error": null,
    "data": {
        "rows": [
            {
                "role_id": 14167,
                "user_id": 15416,
                "account_id": 10719,
                "user_name": "John Deo",
                "user_email": "johndeo@acquire.io",
                "allowed_ip": "",
                "user_role_id": 1,
                "role_name": "Administrator",
                "role_status": "active",
                "user_status": "active",
                "secret_key": "[AGENT_SECRET_KEY]";,
                "department_id": null,
                "department_name": null
            }
        ],
        "count": 1,
        "page": 1,
        "limit": 10
    }
}

```

#### **Sample Code**

{% tabs %}
{% tab title="PHP" %}
```javascript
$curl = curl_init();

	curl_setopt_array($curl, array(
		CURLOPT_URL => "https://app.acquire.io/account/agents",
		CURLOPT_RETURNTRANSFER => true,
		CURLOPT_ENCODING => "",
		CURLOPT_MAXREDIRS => 10,
		CURLOPT_TIMEOUT => 30,
		CURLOPT_HTTP_VERSION => CURL_HTTP_VERSION_1_1,
		CURLOPT_CUSTOMREQUEST => "POST",
		CURLOPT_POSTFIELDS => "------WebKitFormBoundary7MA4YWxkTrZu0gW\r\nContent-Disposition: form-data;
			name=\"page\"\r\n\r\n1\r\n------WebKitFormBoundary7MA4YWxkTrZu0gW\r\nContent-Disposition: form-data;
			name=\"limit\"\r\n\r\n10\r\n------WebKitFormBoundary7MA4YWxkTrZu0gW--",
		CURLOPT_HTTPHEADER => array(
		"Content-Type: application/x-www-form-urlencoded",
		"content-type: multipart/form-data; boundary=----WebKitFormBoundary7MA4YWxkTrZu0gW"
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

	url = URI("https://app.acquire.io/account/agents")

	http = Net::HTTP.new(url.host, url.port)

	request = Net::HTTP::Post.new(url)
	request["Content-Type"] = 'application/x-www-form-urlencoded'
	request.body = "------WebKitFormBoundary7MA4YWxkTrZu0gW\r\nContent-Disposition: form-data;
					name=\"page\"\r\n\r\n1\r\n------WebKitFormBoundary7MA4YWxkTrZu0gW\r\nContent-Disposition: form-data;
					name=\"limit\"\r\n\r\n10\r\n------WebKitFormBoundary7MA4YWxkTrZu0gW--"

	response = http.request(request)
	puts response.read_body

```
{% endtab %}

{% tab title="cURL" %}
```javascript
curl --request POST \
		--url 'https://app.acquire.io/account/agents' \
		--header 'Content-Type: application/x-www-form-urlencoded' \
		--header 'content-type: multipart/form-data; boundary=----WebKitFormBoundary7MA4YWxkTrZu0gW' \
		--form page=1 \
		--form limit=10
```
{% endtab %}

{% tab title="jQuery" %}
```javascript
 var form = new FormData();
		form.append("page", "1");
		form.append("limit", "10");

	var settings = {
		"async": true,
		"crossDomain": true,
		"url": "https://app.acquire.io/account/agents",
		"method": "POST",
		"headers": {
		"Content-Type": "application/x-www-form-urlencoded"
	},
		"processData": false,
		"contentType": false,
		"mimeType": "multipart/form-data",
		"data": form
	}
	$.ajax(settings).done(function (response) {
	console.log(response);
	});
```
{% endtab %}

{% tab title="Python" %}
```javascript
import requests

	url = "https://app.acquire.io/account/agents"

	payload = "------WebKitFormBoundary7MA4YWxkTrZu0gW\r\nContent-Disposition: form-data;
			name=\"page\"\r\n\r\n1\r\n------WebKitFormBoundary7MA4YWxkTrZu0gW\r\nContent-Disposition: form-data;
			name=\"limit\"\r\n\r\n10\r\n------WebKitFormBoundary7MA4YWxkTrZu0gW--"
	headers = {'Content-Type': 'application/x-www-form-urlencoded'}

	response = requests.request("POST", url, data=payload, headers=headers)

	print(response.text)
```
{% endtab %}

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
		"account",
		"agents"
	],
	"headers": {
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

	req.write("------WebKitFormBoundary7MA4YWxkTrZu0gW\r\nContent-Disposition: form-data;
		name=\"page\"\r\n\r\n1\r\n------WebKitFormBoundary7MA4YWxkTrZu0gW\r\nContent-Disposition: form-data;
		name=\"limit\"\r\n\r\n10\r\n------WebKitFormBoundary7MA4YWxkTrZu0gW--");
	req.end();
```
{% endtab %}
{% endtabs %}



