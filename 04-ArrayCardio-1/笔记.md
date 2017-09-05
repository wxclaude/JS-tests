### 主要考察了Array的几个基本方法：
> [filter](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Array/filter)、map、sort、[reduce](https://developer.mozilla.org/zh-CN/docs/Web/JavaScript/Reference/Global_Objects/Array/Reduce_clone)

总结：
1. 可以通过console.table()将结果按照表格打印出来
2. reduce()方法在不指定第一个参数时默认取数组的第一个元素作为prev，取数组的第二个元素为cur。可以手动传入一个obj为prev，并设置reduce()方法的第二个参数为具体的obj