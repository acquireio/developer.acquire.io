# Widget UI

### Set Vertical Margin

Set the vertical offset of the chat button from the edge of the browser window.

#### **Parameters**

| Method | Parameters | Type | Description |
| :--- | :--- | :--- | :--- |
| `setVerticalMargin` | `distance` | `Integer` | Distance from the edge of the browser window, in pixels \(number\) |

#### **Sample code**

Set the widget margin for vertical to 35 pixels for bottom**.**

```javascript
<script>
     window.acquire = window.acquire || [];
     acquire.push(function(app){
         var setUIConfogFn = function(){
                    if(app) {
                        app.ui.setVerticalMargin(35);
                    }
                }
         app.on('ui_reloaded', (socket, cr, sr) => {
                    setUIConfogFn();
                });

        setUIConfogFn();
     });
</script>
```

### Set Horizontal Margin

Set the horizontal offset of the chat button from the edge of the browser window.

#### **Parameters**

|  Method | Parameters | Type | Description |
| :--- | :--- | :--- | :--- |
|  `setHorizontalMargin` | `distance` | `Integer` |  Distance from the edge of the browser window, in pixels \(number\) |

#### **Sample code**

Set the widget margin for horizontal to 35 pixels for left/right

```javascript
<script>
    window.acquire = window.acquire || [];
     acquire.push(function(app){
         var setUIConfogFn = function(){
                    if(app) {
                        app.ui.setHorizontalMargin(35);
                    }
                }
         app.on('ui_reloaded', (socket, cr, sr) => {
                    setUIConfogFn();
                });

        setUIConfogFn();
     });
</script>
```

### Check Widget Status

Widget status is maximize if true.

#### **Sample code**

To check widget visible or hidden

```javascript
<script>
     window.acquire = window.acquire || [];
     acquire.push(function(app){
         var status = app.ui.isMax() ? 'visible' : 'hidden';
     });
</script>
```

### Maximise Widget

Show the chat widget.

**Note:**  It is recommended to show the chat widget only when initial hidden or if any unread message in thread.

#### **Parameters**

|  Method |  Parameters |  Type |  Description |
| :--- | :--- | :--- | :--- |
|  `status` |  `value` |  `String` |  Chat widget status in string 'max' |

#### **Sample code**

To widget show

```javascript
<script>
     window.acquire = window.acquire || [];
     acquire.push(function(app){
         app.ui.status('max');
     });
</script>

//on html element onclick
<a href="javascript:;" onclick="acquireIO.ui.status('max');">Open Widget</a>
```

### Minimise Widget

Hide the chat widget and show launcher.

#### **Parameters**

| Method |  Parameters |  Type |  Description |
| :--- | :--- | :--- | :--- |
|  `status` |  `value` |  `String` |   Chat widget status in string 'min' |

#### **Sample code**

To widget show

```javascript
<script>
     window.acquire = window.acquire || [];
     acquire.push(function(app){
         app.ui.status('min');
     });
</script>

//on html element onclick
<a href="javascript:;" onclick="acquireIO.ui.status('min');">Open Widget</a>
```



