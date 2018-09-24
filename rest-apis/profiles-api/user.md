# User

Acquire live chat dashboard gives your team leader an overview of agent activity at any given time.

Profiles User API body parameter in add limit, page and filter\[master\]

#### **Profiles Use**

\*\*\*\*

| Parameter | Value |
| :--- | :--- |
| **Path** | https://app.acquire.io/profile/lead/list |
| **Method** | POST |
| **Authorization** | Bearer **YOUR\_API\_AUTH\_TOKEN** |
| **Content-type** | application/x-www-form-urlencode |

#### **Body**

| Parameter | Value |
| :--- | :--- |
| **limit** | 10 |
| **page** | 1 |
| **filter\[master\]** | chathistory |

#### **Response JSON Format**

```javascript

{
    "success": true,
    "error": null,
    "data": {
        "total": 1,
        "data": [
            {
                "id": 70574,
                "session_id": 70574,
                "checked_status": 0,
                "visitor_id": 70574,
                "source": null,
                "name": "",
                "email": "",
                "visitor_phone": "",
                "location_full_name": "San Francisco, California, United States",
                "ip": "",
                "country_name": "United States",
                "timezone": "America/Yakutat",
                "country_code": "USA",
                "date_updated": "2018-08-02 07:30:28",
                "city": "517",
                "browser_language": "",
                "conversion": "",
                "first_seen": null,
                "last_seen": null,
                "lead_id": 0,
                "chat_id": ,
                "recording_available": null,
                "rating": null,
                "chat_updated": "2018-08-02 07:31:02",
                "chat_created": "2018-08-02 07:30:28",
                "chat_date_created": null,
                "chat_date_updated": null,
                "ua": "Chrome,,Mac,,Desktop,,,WebKit",
                "browser_name": "Chrome",
                "browser_version": "",
                "os_name": "Mac OS",
                "os_version": "",
                "tags": "",
                "agent_name": "John Deo",
                "bg_color": "#4a1271"
            }
        ],
        "main_query_time": 0.006,
        "chat_user_query_time": 0.003,
        "notify_query_time": 0.011,
        "tag_query_time": 0.002,
        "overall_time": 0.022
    }
}

```

#### **Sample Code**

{% tabs %}
{% tab title="PHP" %}
```javascript
$curl = curl_init();

	curl_setopt_array($curl, array(
		CURLOPT_URL => "http://app.acquire.io/profile/lead/list",
		CURLOPT_RETURNTRANSFER => true,
		CURLOPT_ENCODING => "",
		CURLOPT_MAXREDIRS => 10,
		CURLOPT_TIMEOUT => 30,
		CURLOPT_HTTP_VERSION => CURL_HTTP_VERSION_1_1,
		CURLOPT_CUSTOMREQUEST => "POST",
		CURLOPT_POSTFIELDS => "limit=50&page=1&filter%5Bmaster%5D=chathistory",
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

	url = URI("http://app.acquire.io/profile/lead/list")

	http = Net::HTTP.new(url.host, url.port)

	request = Net::HTTP::Post.new(url)
	request["Authorization"] = 'Bearer [YOUR_API_AUTH_TOKEN]'
	request["Content-Type"] = 'application/x-www-form-urlencoded'
	request.body = "limit=50&page=1&filter%5Bmaster%5D=chathistory"

	response = http.request(request)
	puts response.read_body
```
{% endtab %}

{% tab title="cURL" %}
```javascript
curl --request POST \
		--url 'http://app.acquire.io/profile/lead/list' \
		--header 'Authorization: Bearer [YOUR_API_AUTH_TOKEN]' \
		--header 'Content-Type: application/x-www-form-urlencoded' \
		--data 'limit=50&page=1&filter%5Bmaster%5D=chathistory'
```
{% endtab %}

{% tab title="jQuery" %}
```javascript
var settings = {
		"async": true,
		"crossDomain": true,
		"url": "http://app.acquire.io/profile/lead/list",
		"method": "POST",
		"headers": {
				"Authorization: Bearer [YOUR_API_AUTH_TOKEN]"
				"Content-Type": "application/x-www-form-urlencoded"
			},
		"data": {
			"limit": "50",
			"page": "1",
			"filter[master]": "chathistory"
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

		url = "http://app.acquire.io/profile/lead/list"

		payload = "limit=50&page=1&filter%5Bmaster%5D=chathistory"
		headers = {'Authorization: Bearer [YOUR_API_AUTH_TOKEN]','Content-Type': 'application/x-www-form-urlencoded'}

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
			"profile",
			"lead",
			"list"
		],
		"headers": {
			"Authorization: Bearer [YOUR_API_AUTH_TOKEN]",
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

	req.write(qs.stringify({ limit: '50', page: '1', 'filter[master]': 'chathistory' }));
	req.end();
```
{% endtab %}
{% endtabs %}

