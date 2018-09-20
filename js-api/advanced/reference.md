# Reference

### After app loads

To execute code after acquire app loads, push your code to acquire array using **`acquire.push()`**.

{% hint style="info" %}
 Make sure to put **`acquire.push()`** before init.js under **`<HEAD>`** section of your code.
{% endhint %}

#### Sample Code

```javascript
<script>
   window.acquire = window.acquire || [];
   acquire.push(function(){
      // your code here will run
      // after acquire widget loads completely.
   });
</script>

<script async src="https://s.acquire.io/.../init.js"></script>
```

### Methods on acquireIO Object

|  Method |  Description |
| :--- | :--- |
| `max()` |  Maximizes Chat Widget |
| `min()` | Minimizes Chat Widget |
|  `startChat()` | Starts a new chat |
| `myself()` |  Return current User Object |
| `availableAgents()` | Return list of available agents as Array |

```javascript
acquireIO.max();
acquireIO.min();
acquireIO.startChat();
acquireIO.myself();
acquireIO.availableAgents();
```

