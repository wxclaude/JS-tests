### 思路：
提供了一份json数据的地址，目的就是模拟一次ajax请求，并将拿到的数据进行模糊匹配

1. 运用fetch()发送HTTP请求
> 返回Promise对象，得到我们所需要的json数据

2. 给输入框绑定监听事件（change、keyup）
3. 根据输入的查询字符串，构建查询正则
4. 返回查询的结果，构造结果列表展现出来
### 知识点：
1. Promise异步请求
> 考察了Promise特性的[fetch()](https://developer.mozilla.org/zh-CN/docs/Web/API/Fetch_API/Using_Fetch)、then()、json()等方法

> 主要是fetch()方法请求数据

2. 数组的一系列方法

> filter()、map()等

3. [javascript创建正则对象](http://www.jb51.net/article/76303.htm)

> 顺带复习了一下正则表达式