---
description: Change the window state save setting
---

# Widget window state

> Pass the value to widget\_state property as "yes" in case if you want to hide and "no" to make the widget appear

```text
window.acquire = window.acquire || [];
acquire.push(function(app){
    app.applyAction("update-settings",{"crm.widget_state_unsave":"no"});
})
```

