### 实现效果
初始文档里仅仅提供了一个 script 标签，供我们从[Cornify.com](https://www.cornify.com/)加载一个 JS 文件，调用其中的 cornify_add() 方法时，会在页面中追加 p 标签，并在 DOM 中插入一个图标。Cornify 的具体效果可以到官网首页去体验。

而这个挑战要实现的效果是，当在此页面完整输入了“暗号”（一串事先定义好的字符串）时，生成新的 Cornify 特效。

### 思路
1.  指定可激发特效的字符串，初始化一个数组用于存放按过的键
2.  监听并获取输入的字符，调用[`includes()`](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/String/includes)判断是否已经包含
3.  在符合条件时，调用 cornify