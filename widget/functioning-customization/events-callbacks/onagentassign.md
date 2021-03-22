---
description: >-
  Update event on acquire object will be triggered after the agent accept the
  chat.
---

# onAgentAssign

> The on function with event as update is to off the default behaviour when event occurs and trigger helps to manually fire the event update with the necessary parameters.

```text
window.acquire = window.acquire || [];
acquire.push(function(app){
    app.on('update',function(){console.log(arguments)});
    app.trigger('update',1,2,3);
});
```



