# Get Operating Hours

Operating hours GET API is used to get a list of operating hours set by the user.

| Parameter | Value |
| :--- | :--- |
| **Path** | https://app.acquire.io/api/account/setting/operating-hours |
| **Method** | POST |
| **Authorization** | Bearer \[YOUR\_API\_AUTH\_TOKEN\] |
| **Content-type** | application/json |

**Body\(row\)**

```javascript
{
  "working_hours_toggle": 1,
  "working_schedule":[
  				{"working_day":"mon","working_from_time":"06:00","working_to_time":"20:00"},
  				{"working_day":"tue","working_from_time":"01:00","working_to_time":"01:15"},
  				{"working_day":"wed","working_from_time":"06:00","working_to_time":"20:00"},
  				{"working_day":"thu","working_from_time":"06:00","working_to_time":"20:00"},
  				{"working_day":"fri","working_from_time":"01:30","working_to_time":"19:30"},
  				{"working_day":"sun","working_from_time":"01:00","working_to_time":"01:15"}
  			]
}
```

**Response JSON**

```javascript
{
    "success": true,
    "error": null,
    "data": [
        {
            "working_day": "thu",
            "working_from_time": "06:00",
            "working_to_time": "20:00"
        },
        {
            "working_day": "thu",
            "working_from_time": "06:00",
            "working_to_time": "20:00"
        },
        {
            "working_day": "thu",
            "working_from_time": "06:00",
            "working_to_time": "20:00"
        },
        {
            "working_day": "fri",
            "working_from_time": "06:00",
            "working_to_time": "20:00"
        },
        {
            "working_day": "fri",
            "working_from_time": "06:00",
            "working_to_time": "20:00"
        },
        {
            "working_day": "sat",
            "working_from_time": "06:00",
            "working_to_time": "20:00"
        },
        {
            "working_day": "sat",
            "working_from_time": "06:00",
            "working_to_time": "20:00"
        }
    ]
}
```

**Sample Code**

{% tabs %}
{% tab title="PHP" %}
```javascript
<?php

$curl = curl_init();

curl_setopt_array($curl, array(
  CURLOPT_URL => "https://app.acquire.io/api/account/setting/operating-hours",
  CURLOPT_RETURNTRANSFER => true,
  CURLOPT_ENCODING => "",
  CURLOPT_MAXREDIRS => 10,
  CURLOPT_TIMEOUT => 30,
  CURLOPT_HTTP_VERSION => CURL_HTTP_VERSION_1_1,
  CURLOPT_CUSTOMREQUEST => "GET",
  CURLOPT_POSTFIELDS => "{\n  \"working_hours_toggle\": 1,\n  \"working_schedule\":[\n  \t\t\t\t{\"working_day\":\"mon\",\"working_from_time\":\"06:00\",\"working_to_time\":\"20:00\"},\n  \t\t\t\t{\"working_day\":\"tue\",\"working_from_time\":\"01:00\",\"working_to_time\":\"01:15\"},\n  \t\t\t\t{\"working_day\":\"wed\",\"working_from_time\":\"06:00\",\"working_to_time\":\"20:00\"},\n  \t\t\t\t{\"working_day\":\"thu\",\"working_from_time\":\"06:00\",\"working_to_time\":\"20:00\"},\n  \t\t\t\t{\"working_day\":\"fri\",\"working_from_time\":\"01:30\",\"working_to_time\":\"19:30\"},\n  \t\t\t\t{\"working_day\":\"sun\",\"working_from_time\":\"01:00\",\"working_to_time\":\"01:15\"}\n  \t\t\t]\n}\n",
  CURLOPT_HTTPHEADER => array(
    "Authorization: Bearer [API_TOKEN]",
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

url = URI("https://app.acquire.io/api/account/setting/operating-hours")

http = Net::HTTP.new(url.host, url.port)

request = Net::HTTP::Get.new(url)
request["Content-Type"] = 'application/json'
request["Authorization"] = 'Bearer [API_TOKEN]'
request.body = "{\n  \"working_hours_toggle\": 1,\n  \"working_schedule\":[\n  \t\t\t\t{\"working_day\":\"mon\",\"working_from_time\":\"06:00\",\"working_to_time\":\"20:00\"},\n  \t\t\t\t{\"working_day\":\"tue\",\"working_from_time\":\"01:00\",\"working_to_time\":\"01:15\"},\n  \t\t\t\t{\"working_day\":\"wed\",\"working_from_time\":\"06:00\",\"working_to_time\":\"20:00\"},\n  \t\t\t\t{\"working_day\":\"thu\",\"working_from_time\":\"06:00\",\"working_to_time\":\"20:00\"},\n  \t\t\t\t{\"working_day\":\"fri\",\"working_from_time\":\"01:30\",\"working_to_time\":\"19:30\"},\n  \t\t\t\t{\"working_day\":\"sun\",\"working_from_time\":\"01:00\",\"working_to_time\":\"01:15\"}\n  \t\t\t]\n}\n"

response = http.request(request)
puts response.read_body
```
{% endtab %}

{% tab title="cURL" %}
```javascript
curl -X GET \
  https://app.acquire.io/api/account/setting/operating-hours \
  -H 'Authorization: Bearer [API_TOKEN]' \
  -H 'Content-Type: application/json' \
  -d '{
  "working_hours_toggle": 1,
  "working_schedule":[
  				{"working_day":"mon","working_from_time":"06:00","working_to_time":"20:00"},
  				{"working_day":"tue","working_from_time":"01:00","working_to_time":"01:15"},
  				{"working_day":"wed","working_from_time":"06:00","working_to_time":"20:00"},
  				{"working_day":"thu","working_from_time":"06:00","working_to_time":"20:00"},
  				{"working_day":"fri","working_from_time":"01:30","working_to_time":"19:30"},
  				{"working_day":"sun","working_from_time":"01:00","working_to_time":"01:15"}
  			]
}
```
{% endtab %}

{% tab title="jQuery" %}
```javascript
var settings = {
  "async": true,
  "crossDomain": true,
  "url": "https://app.acquire.io/api/account/setting/operating-hours",
  "method": "GET",
  "headers": {
    "Content-Type": "application/json",
    "Authorization": "Bearer [API_TOKEN]",
    
  },
  "processData": false,
  "data": "{\n  \"working_hours_toggle\": 1,\n  \"working_schedule\":[\n  \t\t\t\t{\"working_day\":\"mon\",\"working_from_time\":\"06:00\",\"working_to_time\":\"20:00\"},\n  \t\t\t\t{\"working_day\":\"tue\",\"working_from_time\":\"01:00\",\"working_to_time\":\"01:15\"},\n  \t\t\t\t{\"working_day\":\"wed\",\"working_from_time\":\"06:00\",\"working_to_time\":\"20:00\"},\n  \t\t\t\t{\"working_day\":\"thu\",\"working_from_time\":\"06:00\",\"working_to_time\":\"20:00\"},\n  \t\t\t\t{\"working_day\":\"fri\",\"working_from_time\":\"01:30\",\"working_to_time\":\"19:30\"},\n  \t\t\t\t{\"working_day\":\"sun\",\"working_from_time\":\"01:00\",\"working_to_time\":\"01:15\"}\n  \t\t\t]\n}\n"
}

$.ajax(settings).done(function (response) {
  console.log(response);
});
```
{% endtab %}

{% tab title="Nodejs" %}
```javascript
var request = require("request");

var options = { method: 'GET',
  url: 'https://app.acquire.io/api/account/setting/operating-hours',
  headers: 
   {
     Authorization: 'Bearer [API_TOKEN]',
     'Content-Type': 'application/json' },
  body: 
   { working_hours_toggle: 1,
     working_schedule: 
      [ { working_day: 'mon',
          working_from_time: '06:00',
          working_to_time: '20:00' },
        { working_day: 'tue',
          working_from_time: '01:00',
          working_to_time: '01:15' },
        { working_day: 'wed',
          working_from_time: '06:00',
          working_to_time: '20:00' },
        { working_day: 'thu',
          working_from_time: '06:00',
          working_to_time: '20:00' },
        { working_day: 'fri',
          working_from_time: '01:30',
          working_to_time: '19:30' },
        { working_day: 'sun',
          working_from_time: '01:00',
          working_to_time: '01:15' } ] },
  json: true };

request(options, function (error, response, body) {
  if (error) throw new Error(error);

  console.log(body);
});
```
{% endtab %}
{% endtabs %}

