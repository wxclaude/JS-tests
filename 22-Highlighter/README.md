### 实现效果：
当鼠标移动到锚点处，会有一个白色的色块移动到当前锚点所在的位置。

### 知识点：

[`object.getBoundingClientRect()`](https://developer.mozilla.org/zh-CN/docs/Web/API/Element/getBoundingClientRect)

返回元素的大小及其相对于视口的位置。返回值是一个DOMRect对象,该对象包含了一组用于描述边框的只读属性——left、top、right和bottom，单位为像素。除了 width 和 height 外的属性都是相对于视口的左上角位置而言的。