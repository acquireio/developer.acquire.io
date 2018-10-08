# Thread

### Start New Thread

To start a new conversation thread.

{% tabs %}
{% tab title="Attributes" %}
| Attribute | Type | Description |
| :--- | :--- | :--- |
| **`status`** | `string` | New thread status string 'new' |
{% endtab %}

{% tab title="Sample Code" %}
```javascript
<script> 
   window.acquire = window.acquire || [];
   window.acquire.push(function(app){
      app.threadManager().status('new');
   });
</script>
```
{% endtab %}
{% endtabs %}

