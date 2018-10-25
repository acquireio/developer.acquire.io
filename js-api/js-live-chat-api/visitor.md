# Visitor

## Get Visitor

### Visitor Name

Get the name of the visitor.

#### Sample Code

```javascript
<script>
   window.acquire = window.acquire || [];
   window.acquire.push(function(app){
      app.userDetails.subscribe(function(){
           alert(app.userDetails().name);
      });
   });
</script>
```

### Visitor Email

Get the email address of the visitor.

#### Sample Code

```javascript
<script>
   window.acquire = window.acquire || [];
   window.acquire.push(function(app){
      app.userDetails.subscribe(function(){
           alert(app.userDetails().email);
      });
   });
</script>
```

### Visitor Phone

Get the phone number of the visitor.

#### Sample Code

```javascript
<script>
   window.acquire = window.acquire || [];
   window.acquire.push(function(app){
      app.userDetails.subscribe(function(){
           alert(app.userDetails().phone);
      });
   });
</script>
```

## Set Visitor

### Set Customer Tracking

Set the visitor’s name, email address, phone number and remark.  
Use the script at right to update visitor details.

#### **Step 1: Embed tracking code**

Copy the sample customer tracking code under `<HEAD>` section of your webpage `before widget code.`

#### **Step 2: Reload Webpage**

Save your code and reload webpage.

{% hint style="info" %}
Make sure you replace inside bracket words with your own code that outputs real user data for the currently logged-in user on each of your pages.

All are optional, you can pass only those value that you wanted and you can remove which details you don't have.
{% endhint %}

A convenience function to set multiple settings at once. Accepts a settings object.

#### **Parameters userDetails key detail:**

{% tabs %}
{% tab title="Attributes" %}
| **Attribute** | **Type** | **Description** |
| :--- | :--- | :--- |
| `name` | _`string`_ | Visitor’s name |
| `email` | _`string`_ | Visitor’s email address |
| `phone` | _`string`_ | Visitor’s phone number |
| `remark` | _`string`_ | Visitor’s remark |
{% endtab %}

{% tab title="Sample Code" %}
```javascript
<script>
   window.acquire=window.acquire||[];
   window.acquire.push({
                  userDetails:{
                      name:'Visitor',
                      phone:'0000000000',
                      email:'visitor@site.com',
                      remarks:'anything remark to customer track'
                  },
                });
</script>
```
{% endtab %}
{% endtabs %}

### Visitor Page Update

Programmatically update visitor’s web-path.

{% hint style="info" %}
**Note:** Chat triggers set to run “When a visitor has loaded the chat widget” will be fired when the visitor path is changed.
{% endhint %}

{% tabs %}
{% tab title="Attributes" %}
| **Attribute** | **Type** | **Description** |
| :--- | :--- | :--- |
| `title` | _`string`_ | title of page |
| `url` | _`string`_ | Url for page |

| _`Optional - If not specified, the current page’s location and title will be used; if specified, the updated page url and title will be taken from the options object.`_ |
| :---: |
{% endtab %}

{% tab title="Sample Code" %}
Update visitor’s path with specific page url and title:

```javascript
<script>
    // update visitor's path with specific page url and title
    window.acquire=window.acquire||[];
    window.acquire.push(function(app){
      app.visitorPageUpdate('example title', 'http://example.com');
    });
</script>
```
{% endtab %}
{% endtabs %}

Update visitor’s path with current page’s location and title:

```javascript
<script>
    // update visitor's path with current page's location and title
    acquireIO.visitorPageUpdate(title, url);
</script>
```

