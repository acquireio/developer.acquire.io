# Profile Delete

Profiles Delete API header parameter in Content-Type application/json and body in data raw \(application/json\) send.

#### **Permanently delete a user**

User Delete Requests allow you to irrevocably remove data about a User. After creating a User Delete Request, the User’s data will be hard-deleted. This deletion cannot be cancelled or reversed.

User Delete Requests can be created via a **POST** to **https://app.acquire.io/profile/lead/delete**

| Parameter | Value |
| :--- | :--- |
| **Path** | https://app.acquire.io/profile/lead/delete |
| **Method** | POST |
| **Authorization** | Bearer **\[YOUR\_API\_AUTH\_TOKEN\]** |
| **Content-type** | application/json |

#### **Body**raw\(application/json\)

```javascript

{
  "id": [
    3112
  ]
}

```

#### **Response JSON Format**

```javascript

{
    "success": true,
    "error": null,
    "data": "Selected profile(s) successfully deleted!"
}

```

#### **Hard delete**

{% hint style="info" %}
 **Important:** If you delete a profile/lead after you can not restore and access user’s data.
{% endhint %}



