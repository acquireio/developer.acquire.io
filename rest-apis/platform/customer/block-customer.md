# Block Customer

Block a Customer.

| Parameter | Value |
| :--- | :--- |
| **Path** | ​[https://{{account\_id}}.acquire.io/api/v1](https://%7B%7Baccount_id%7D%7D.acquire.io/api/v1/crm/objects/company/%7B%7BcompanyId%7D%7D)/crm/block-visitor​ |
| **Method** | **POST** |
| **Authorization** | Bearer \*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*YOUR\_API\_KEY\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\* |
| **Content-type** | application/json |

**Body\(raw\)**

```text
{
    "data": [
        827
    ],
    "type": "contact",
    "blockTill": "2021-09-09T07:08:12.658Z"
}
```

**Response JSON**

```text
{
    "data": true
}
```

