### 实现效果：

对数组进行排序，将乐队按照乐曲名称进行排序，曲名前面的a/an/the不参与排序。

### 知识点：

-   [`Array.prototype.replace()`](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/String/replace)：先取出乐队名称前面的a/an/the后在进行排序
-   [`Array.prototype.sort()`](https://developer.mozilla.org/en/docs/Web/JavaScript/Reference/Global_Objects/Array/sort)