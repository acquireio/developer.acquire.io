---
description: >-
  The state event triggers when the agent changes it's state to either
  available/unavailable
---

# onAgentStateChange \(Available/Unavailable\)

> The on function with event as state is to off the default behaviour when event occurs and trigger helps to manually fire the event update with the necessary parameters.

```text
window.acquire = window.acquire || [];
acquire.push(function(app){
    app.on('state',function(){console.log(arguments)});
    app.trigger('state',1,2,3);
});
```

