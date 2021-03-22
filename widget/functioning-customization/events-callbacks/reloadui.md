---
description: Reloading the UI from the acquire object
---

# reloadUI

```text
window.acquire = window.acquire || [];
acquire.push(function(app){
    app.reloadUI();
});
```

