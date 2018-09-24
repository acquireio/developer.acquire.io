# Team Analytics

Acquire live chat dashboard gives your team leader an overview of agent activity at any given time. Your agents all chat data reports get and view in this API and you see data on multiple parameter like this: Today, Yesterday, daily, weekly and monthly.

Team Analytics API body parameter in Select your timezone, date start, date end, filter\_type and agent\_id. Filter Type in today, yesterday, daily, weekly and monthly parameter available.

**Team Analytics**

[![](https://developers.acquire.io/media/data/article/agents-analytics.PNG)](https://developers.acquire.io/media/data/article/agents-analytics.PNG)

| Parameter | Value |
| :--- | :--- |
| **Path** | https://app.acquire.io/analytics/agent/overview |
| **Method** | POST |
| **Authorization** | Bearer \[YOUR\_API\_AUTH\_TOKEN\] |
| **Content-type** | application/x-www-form-urlencoded |

**Body**

| Parameter | Value |
| :--- | :--- |
| **timezone** | Europe/London |
| **date\_start** | 2018-05-23 00:00:00 |
| **date\_end** | 2018-07-18 23:59:59 |
| **filter\_type** | daily |
| **agent\_id** |  |

**Response JSON**

```javascript

{
    "success": true,
    "error": null,
    "data": {
        "chat_report": {
            "analytics": {
                "15416": {
                    "assigned_chat": 62,
                    "total_chat": 61,
                    "unanswered_chat": 0,
                    "total_missed_chat": 0,
                    "average_chat_time": "08 minutes 52 seconds ",
                    "average_response_time": "02 seconds ",
                    "total_time_on_chat": "09 hours 35 seconds ",
                    "average_drop_off_time": "",
                    "rating_positive": 3,
                    "rating_negative": 0
                }
            },
            "login_scale": {}
        }
    }
}

```

**Sample Code**

{% tabs %}
{% tab title="PHP" %}
```javascript
$curl = curl_init();

	curl_setopt_array($curl, array(
		CURLOPT_URL => "https://app.acquire.io/analytics/agent/overview",
		CURLOPT_RETURNTRANSFER => true,
		CURLOPT_ENCODING => "",
		CURLOPT_MAXREDIRS => 10,
		CURLOPT_TIMEOUT => 30,
		CURLOPT_HTTP_VERSION => CURL_HTTP_VERSION_1_1,
		CURLOPT_CUSTOMREQUEST => "POST",
		CURLOPT_POSTFIELDS => "timezone=Europe%2FLondon&date_start=2018-05-23%2000%3A00%3A00&date_end=2018-07-18%2023%3A59%3A59&filter_type=&agent_id=",
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

	url = URI("https://app.acquire.io/analytics/agent/overview")

	http = Net::HTTP.new(url.host, url.port)

	request = Net::HTTP::Post.new(url)
	request["Authorization"] = 'Bearer [YOUR_API_AUTH_TOKEN]'
	request["Content-Type"] = 'application/x-www-form-urlencoded'
	request.body = "timezone=Europe%2FLondon&date_start=2018-05-23%2000%3A00%3A00&date_end=2018-07-18%2023%3A59%3A59&filter_type=&agent_id="

	response = http.request(request)
	puts response.read_body
```
{% endtab %}

{% tab title="cURL" %}
```javascript
curl --request POST \
		--url 'https://app.acquire.io/analytics/agent/overview' \
		--header 'Authorization: Bearer [YOUR_API_AUTH_TOKEN]' \
		--header 'Content-Type: application/x-www-form-urlencoded' \
		--data 'timezone=Europe%2FLondon&date_start=2018-05-23%2000%3A00%3A00&date_end=2018-07-18%2023%3A59%3A59&filter_type=&agent_id='
```
{% endtab %}

{% tab title="jQuery" %}
```javascript
var settings = {
		"async": true,
		"crossDomain": true,
		"url": "https://app.acquire.io/analytics/agent/overview",
		"method": "POST",
		"headers": {
		"Authorization": "Bearer [YOUR_API_AUTH_TOKEN]"
		"Content-Type": "application/x-www-form-urlencoded"
	},
		"data": {
			"timezone": "Europe/London",
			"date_start": "2018-05-23 00:00:00",
			"date_end": "2018-07-18 23:59:59",
			"agent_id": ""
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

		url = "https://app.acquire.io/analytics/agent/overview"

		payload = "timezone=Europe%2FLondon&date_start=2018-05-23%2000%3A00%3A00&date_end=2018-07-18%2023%3A59%3A59&filter_type=&agent_id="
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
		"https://app.acquire.io/"
		],
		"path": [
		"analytics",
		"agent",
		"overview"
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

	req.write(qs.stringify({ timezone: 'Europe/London',
		date_start: '2018-05-23 00:00:00',
		date_end: '2018-07-18 23:59:59',
		filter_type: undefined,
		agent_id: '' }));
	req.end();
```
{% endtab %}
{% endtabs %}

