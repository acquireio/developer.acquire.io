# Installation

Choose one of the following methods to install the widget.

### Copy code from Acquire

1. Log in to your Acquire account.
2. Go to **Settings.** 
3. Select **Installation and Setup** and click on **Web widget.**
4. You will be redirected to the **Widget Code** page.
5. To embed the **Acquire widget** on your website, copy the Javascript code snippet and paste it in the **Head** tag of your website.

### Copy code here

Alternatively, copy the code to the Head tag of your website. Replace {accountId} with your Acquire account ID. 

```text
<!--  Widget Code -->
<script type="text/javascript">
((function(){
    window.acquire = window.acquire || [{s:Date.now()}];
    var load=function(){
        var script="https://{accountId}.acquire.io/widget.js";
        var x=document.createElement('script');
        x.src=script;x.async=true;
        var sx=document.getElementsByTagName('script')[0];
        sx.parentNode.insertBefore(x, sx);
    };
    if(document.readyState === "complete")
        load();
    else if (window.addEventListener)
        window.addEventListener('load',load,false);
    else if (window.attachEvent) {
        window.attachEvent("onload", load);
    }
})())
</script>
<noscript>
<a href="https://www.acquire.io?welcome" title="live chat software">Acquire</a></noscript>
<!-- / Widget Code -->
```

