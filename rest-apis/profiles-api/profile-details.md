# Profile Details

Acquire live chat dashboard gives your team leader an overview of agent activity at any given time.

Profile Details API in header parameter Authorization: Bearer **\[YOUR\_API\_AUTH\_TOKEN\]**, Content-Type : application/json and body parameter in id send.



| Parameter | Value |
| :--- | :--- |
| **Path** | https://app.acquire.io/api/profile/lead/detail |
| **Method** | POST |
| **Authorization** | Bearer **\[YOUR\_API\_AUTH\_TOKEN\]** |
| **Content-type** | application/json |
| **zone** | {"timezone":"Mountain/Arizona","offset":"-06:00"} |

#### **Body**

| Parameter | Value |
| :--- | :--- |
| **id** | 70711 |

#### **Response JSON**

```javascript

{
    "success": true,
    "error": null,
    "data": {
        "id": 70711,
        "visitor_id": 37167,
        "chatid": 70711,
        "ref": null,
        "visitor_name": "John Deo",
        "visitor_email": "johndeo@acquire.io",
        "visitor_phone": "16502379946",
        "visitor_remarks": "https://acquire.io/",
        "visitor_address": "San Francisco, California, United States",
        "company_name": "",
        "lead_id": 0,
        "date_created": "2018-07-12 11:05:51",
        "first_visit": "12-07-2018 11:05:51 AM",
        "ip": "50.0.000.00",
        "browser_name": "SDK",
        "browser_version": "1.0.6",
        "os_name": "iOS",
        "device_name": "mobile",
        "os_version": "10.3.2",
        "visitor_user_agent_engine_name": "AcquireIO iOS SDK",
        "visitor_user_agent_engine_version": "1.0.6",
        "visitor_user_agent_cpu_arch": "",
        "page_views": 750,
        "crm_record_id": 1442,
        "total_visit": 76,
        "last_visit": "2018-09-01 08:36:07",
        "total_chat": 76,
        "ua": "SDK,1.0.6,iOS,10.3.2,ios,mobile,Apple,,AcquireIO iOS SDK,1.0.6",
        "country": "United States",
        "country_code": "USA",
        "tags": "",
        "tags_name": "Existing customer ",
        "meta_fields": null,
        "followers": null,
        "custom_fields_value": "company-name - acquire",
        "fields": {
            "company-name": "acquire"
        },
        "custom_fields": [
            {
                "type": "text",
                "label": "company name",
                "name": "company-name",
                "value": ""
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
		CURLOPT_URL => "https://app.acquire.io/profile/lead/detail",
		CURLOPT_RETURNTRANSFER => true,
		CURLOPT_ENCODING => "",
		CURLOPT_MAXREDIRS => 10,
		CURLOPT_TIMEOUT => 30,
		CURLOPT_HTTP_VERSION => CURL_HTTP_VERSION_1_1,
		CURLOPT_CUSTOMREQUEST => "POST",
		CURLOPT_POSTFIELDS => "------WebKitFormBoundary7MA4YWxkTrZu0gW\r\nContent-Disposition: form-data; name=\"id\"\r\n\r\n3393\r\n------WebKitFormBoundary7MA4YWxkTrZu0gW--",
		CURLOPT_HTTPHEADER => array(
			"Authorization: Bearer [YOUR_API_AUTH_TOKEN]",
			"Content-Type: application/json",
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

	url = URI("https://app.acquire.io/profile/lead/detail")

	http = Net::HTTP.new(url.host, url.port)

	request = Net::HTTP::Post.new(url)
	request["Authorization"] = 'Bearer [YOUR_API_AUTH_TOKEN]'
	request["Content-Type"] = 'application/json'
	request.body = "------WebKitFormBoundary7MA4YWxkTrZu0gW\r\nContent-Disposition: form-data; name=\"id\"\r\n\r\n3393\r\n------WebKitFormBoundary7MA4YWxkTrZu0gW--"

	response = http.request(request)
	puts response.read_body
```
{% endtab %}

{% tab title="cURL" %}
```javascript
curl --request POST \
		--url 'https://app.acquire.io/profile/lead/detail' \
		--header 'Authorization: Bearer [YOUR_API_AUTH_TOKEN]' \
		--header 'Content-Type: application/json' \
		--header 'content-type: multipart/form-data; boundary=----WebKitFormBoundary7MA4YWxkTrZu0gW' \
		--form id=3393
```
{% endtab %}

{% tab title=" jQuery" %}
```javascript
 var form = new FormData();
	form.append("id", "3393");

	var settings = {
		"async": true,
		"crossDomain": true,
		"url": "https://app.acquire.io/profile/lead/detail",
		"method": "POST",
		"headers": {
			"Authorization: Bearer [YOUR_API_AUTH_TOKEN]",
			"Content-Type": "application/json"
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

	url = "https://app.acquire.io/profile/lead/detail"

	payload = "------WebKitFormBoundary7MA4YWxkTrZu0gW\r\nContent-Disposition: form-data; name=\"id\"\r\n\r\n3393\r\n------WebKitFormBoundary7MA4YWxkTrZu0gW--"
	headers = {'Authorization: Bearer [YOUR_API_AUTH_TOKEN]','Content-Type': 'application/json'}

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
			"profile",
			"lead",
			"detail"
		],
		"headers": {
			"Authorization: Bearer [YOUR_API_AUTH_TOKEN]",
			"Content-Type": "application/json"
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

	req.write("------WebKitFormBoundary7MA4YWxkTrZu0gW\r\nContent-Disposition: form-data; name=\"id\"\r\n\r\n3393\r\n------WebKitFormBoundary7MA4YWxkTrZu0gW--");
	req.end();
```
{% endtab %}
{% endtabs %}

