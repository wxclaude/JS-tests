### 总结
这个部分主要是实践了一些在 Console 面板里的调试技巧：
1. 加断点

2. `.log`的更多用法

    这个是最常用的，但它还有一些更多功能：比如参数支持类似 C 语言的字符串替换模式。
    - `%s` 字符串
    - `%d` 整数
    - `%f` 浮点值
    - `%o` Object
    - `%c` 设定输出的样式，在之后的文字将按照第二个参数里的值进行显示
    ```
    console.log("输出一个字符串 %s ", "log");
    console.log("输出一个整数是 %d ", 1.23); //1
    console.log("输出一个小数是 %d ", 1.23); //1.23
    console.log("%c不同样式的输出效果", "color: #00fdff; font-size: 2em;");
    // warning!
    console.warn("三角感叹号图标，淡黄色背景")
    // Error :|
    console.error("红叉图标，红字红色背景");
    // Info
    console.info("蓝色圆形感叹号图标");
    const p = document.querySelector('p');
    console.log(p);//输出这个 DOM 的 HTML 标签
    console.dir(p);//输出这个 DOM 元素的属性列表
    console.clear();//清空 console 面板输出内容,或快捷键Ctrl + L
    console.assert(1===1, "前面表达式为false时输出，否则删除");
    console.table(dogs, ["age"]);//以表格形式打印dogs中age列
    console.time('start point');
    console.timeEnd('end point');
    ```