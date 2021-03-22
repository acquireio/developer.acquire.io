---
description: >-
  Fire the event with the parameters getting from the close event with the
  acquire object
---

# onChatClosed

> The on function with event and callback helps to off the default close event and trigger helps to fire the event with the necessary parameters

```text
window.acquire = window.acquire || [];
acquire.push(function(app){
    app.on('close',function(){console.log(arguments)});
    app.trigger('close',1,2,3);
})
```

