# Installation

Visit [acquire.io](https://www.acquire.io/) and click a Sign Up.  
Once logged In then click on integration button and inside [widget section ](https://www.acquire.io/)get chat box initiation code.

### Step 1: Insert Widget Code to webpage

Copy the following sample widget code and paste it inside `<HEAD>` section of your webpage

### Step 2: Reload Webpage <a id="step-2--reload-webpage"></a>

Save your code and reload webpage.

### Sample Widget Code

```javascript
<!--  Widget Code -->
<script type="text/javascript">
    ((function() {
                var load = function() {
                    var script = "https://s.acquire.io/a-ACCOUNT_ID/init.js";
                    var x = document.createElement('script');
                    x.src = script;
                    x.async = true;
                    var sx = document.getElementsByTagName('script')[0];
                    sx.parentNode.insertBefore(x, sx);
                };
                if (document.readyState === "complete") load();
                else if (window.addEventListener) 
                // W3C DOM                    
                window.addEventListener('load',load,false);                
                else if (window.attachEvent) { 
                // IE DOM                    
                window.attachEvent("onload", load);                
                }})())
</script> 
<noscript> <a href="https://www.acquire.io?welcome" title="live chat software">Acquire </a> </noscript>
<!-- / Widget Code -->
```

