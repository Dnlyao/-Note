```javascript
/**
* 自定义函数名：PrefixZero
* @param num： 被操作数
* @param n： 固定的总位数
*/
function PrefixZero(num, n) {
    return (Array(n).join(0) + num).slice(-n);
}
```

实例

```javascript
var myNum = 9;
var myNum2 = 12;

console.log('原变量myNum：'+myNum);//9
console.log('处理后myNum：'+PrefixZero(myNum, 3));//009
 
console.log('原变量myNum2：'+myNum2);
console.log('处理后myNum2：'+PrefixZero(myNum2, 3));//012
```



>1.Array(5) => 创建了一个长度为5的空数组

```javascript
console.log(Array(5));// [empty × 5]
```

>2.Array(5).join(0) => 用0拼接将数组转换成字符串


```javascript
console.log(Array(5).join(0));// 0000
```

>3.Array(5).join(0)+91 => 通过+,实现字符串的拼接

```javascript
console.log(Array(5).join(0)+91);// 000091
```
>4.(Array(5).join(0) + 91).slice(-5) => slice(startIndex,endIndex)方法，用于截取

- 参数是起始位置，含头不含尾
- 只有一个参数时，表示从该起始位置一直截取到最后。
- 参数值为负数时，表示从后往前数，如最后一位，索引是-1

