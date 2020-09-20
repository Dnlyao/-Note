  # 扫描器无焦点扫描，并且不会单出软键盘#

>利用jq，onblur是当input框失去焦点的时候，onfocus是当input框获取焦点的时候。获取焦点时，把输入框的readonly等于true，失去焦点时，反之。这样输入时，设置定时器，完成输入动作后，立刻转换。所以软键盘不会弹出。

```
<input type="text" readonly autofocus="autofocus" onblur="onBlur()" onfocus="onFocus()" id="inputs"
placeholder="测试"style="position:fixed;left: 0;top: 0;z-index: 10;">

function onFocus() {
var target = event.target
setTimeout(function () {
 target.readOnly = false
}, 200)
}

function onBlur() {event.target.readOnly = true}
```
