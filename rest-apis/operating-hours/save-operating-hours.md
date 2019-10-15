# Save Operating Hours

Operating hours POST API is used to add operating hours the hours set will determine when the widget is displayed. Widget will not be displayed outside of operating hours, even if an user is online.

| Parameter | Value |
| :--- | :--- |
| **Path** | https://app.acquire.io/api/account/setting/operating-hours-save |
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
  "data": []
}
```

**Sample Code**

{% tabs %}
{% tab title="PHP" %}
```javascript
<?php

$curl = curl_init();

curl_setopt_array($curl, array(
  CURLOPT_URL => "https://app.acquire.io/api/account/setting/operating-hours-save",
  CURLOPT_RETURNTRANSFER => true,
  CURLOPT_ENCODING => "",
  CURLOPT_MAXREDIRS => 10,
  CURLOPT_TIMEOUT => 30,
  CURLOPT_HTTP_VERSION => CURL_HTTP_VERSION_1_1,
  CURLOPT_CUSTOMREQUEST => "POST",
  CURLOPT_POSTFIELDS => "{\n  \"working_hours_toggle\": 1,\n  \"working_schedule\":[\n  \t\t\t\t{\"working_day\":\"mon\",\"working_from_time\":\"06:00\",\"working_to_time\":\"20:00\"},\n  \t\t\t\t{\"working_day\":\"tue\",\"working_from_time\":\"01:00\",\"working_to_time\":\"01:15\"},\n  \t\t\t\t{\"working_day\":\"wed\",\"working_from_time\":\"06:00\",\"working_to_time\":\"20:00\"},\n  \t\t\t\t{\"working_day\":\"thu\",\"working_from_time\":\"06:00\",\"working_to_time\":\"20:00\"},\n  \t\t\t\t{\"working_day\":\"fri\",\"working_from_time\":\"01:30\",\"working_to_time\":\"19:30\"},\n  \t\t\t\t{\"working_day\":\"sun\",\"working_from_time\":\"01:00\",\"working_to_time\":\"01:15\"}\n  \t\t\t]\n}",
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

url = URI("https://app.acquire.io/api/account/setting/operating-hours-save")

http = Net::HTTP.new(url.host, url.port)

request = Net::HTTP::Post.new(url)
request["Authorization"] = 'Bearer [API_TOKEN]'
request["Content-Type"] = 'application/json'
request.body = "{\n  \"working_hours_toggle\": 1,\n  \"working_schedule\":[\n  \t\t\t\t{\"working_day\":\"mon\",\"working_from_time\":\"06:00\",\"working_to_time\":\"20:00\"},\n  \t\t\t\t{\"working_day\":\"tue\",\"working_from_time\":\"01:00\",\"working_to_time\":\"01:15\"},\n  \t\t\t\t{\"working_day\":\"wed\",\"working_from_time\":\"06:00\",\"working_to_time\":\"20:00\"},\n  \t\t\t\t{\"working_day\":\"thu\",\"working_from_time\":\"06:00\",\"working_to_time\":\"20:00\"},\n  \t\t\t\t{\"working_day\":\"fri\",\"working_from_time\":\"01:30\",\"working_to_time\":\"19:30\"},\n  \t\t\t\t{\"working_day\":\"sun\",\"working_from_time\":\"01:00\",\"working_to_time\":\"01:15\"}\n  \t\t\t]\n}"

response = http.request(request)
puts response.read_body
```
{% endtab %}

{% tab title="cURL" %}
```javascript
curl -X POST \
  https://app.acquire.io/api/account/setting/operating-hours-save \
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
}'
```
{% endtab %}

{% tab title="jQuery" %}
```javascript
var settings = {
  "async": true,
  "crossDomain": true,
  "url": "https://app.acquire.io/api/account/setting/operating-hours-save",
  "method": "POST",
  "headers": {
    "Authorization": "Bearer [API_TOKEN]",
    "Content-Type": "application/json",
  
  },
  "processData": false,
  "data": "{\n  \"working_hours_toggle\": 1,\n  \"working_schedule\":[\n  \t\t\t\t{\"working_day\":\"mon\",\"working_from_time\":\"06:00\",\"working_to_time\":\"20:00\"},\n  \t\t\t\t{\"working_day\":\"tue\",\"working_from_time\":\"01:00\",\"working_to_time\":\"01:15\"},\n  \t\t\t\t{\"working_day\":\"wed\",\"working_from_time\":\"06:00\",\"working_to_time\":\"20:00\"},\n  \t\t\t\t{\"working_day\":\"thu\",\"working_from_time\":\"06:00\",\"working_to_time\":\"20:00\"},\n  \t\t\t\t{\"working_day\":\"fri\",\"working_from_time\":\"01:30\",\"working_to_time\":\"19:30\"},\n  \t\t\t\t{\"working_day\":\"sun\",\"working_from_time\":\"01:00\",\"working_to_time\":\"01:15\"}\n  \t\t\t]\n}"
}

$.ajax(settings).done(function (response) {
  console.log(response);
});
```
{% endtab %}

{% tab title="Nodejs" %}
```javascript
var request = require("request");

var options = { method: 'POST',
  url: 'https://app.acquire.io/api/account/setting/operating-hours-save',
  headers: 
   { 
     'Content-Type': 'application/json',
     Authorization: 'Bearer [API_TOKEN]' },
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

