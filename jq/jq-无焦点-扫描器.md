```
<input type="text" readonly autofocus="autofocus" onblur="onBlur()" onfocus="onFocus()" id="inputs" placeholder="测试"style="position:fixed;left: 0;top: 0;z-index: 10;">
function findBlur() {$('#inputs').focus()}
function onFocus() {
var target = event.target
setTimeout(function () {
 target.readOnly = false
}, 200)
}
function onBlur() {event.target.readOnly = true}
```
> 这是第一层
>> 第二层嵌套
>> ```
>> <!--这是多行代码输入的地方,下面是例子-->
>> <!DOCTYPE html PUBLIC "-//W3C//DTD HTML 4.01 Transitional//EN" "http://www.w3.org/TR/html4/loose.dtd">
>> <html> 
>> ```
