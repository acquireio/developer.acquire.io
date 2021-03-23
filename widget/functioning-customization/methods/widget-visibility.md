---
description: Change the visibility of the widget
---

# Widget visibility

> Pass the value to hide widget property as "yes" in case if you want to hide and "no" to make the widget appear

```text
window.acquire = window.acquire || [];
acquire.push(function(app){
    app.applyAction("update-settings",{"crm.hide_widget_in_web":"no"});
})
```

