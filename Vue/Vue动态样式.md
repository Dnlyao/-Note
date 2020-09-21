
### div绑定数据

NavWidth为样式绑定，动态改变width，NavWidth不需要再data里面声明。

innerwidth 返回窗口的文档显示区的宽度。

``` 
<div  
class="nav"
 :style="{width: NavWidth}">

js部分
  computed: {
    NavWidth: function () {
      let widt = window.innerWidth - 400 + "px";
      return widt;
    },
  },
```



