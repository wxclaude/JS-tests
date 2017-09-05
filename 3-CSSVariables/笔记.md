### 我的思路：
1. 通过滑块改变图片外框的宽度
2. 通过滑块改变整个元素的模糊度
3. 通过点击调出颜色选取器，用来改变图片外框的颜色

> 通过监听[HTML5的range滑块控件](http://www.w3school.com.cn/jsref/dom_obj_range.asp)
> [的oninput事件](https://stackoverflow.com/questions/18544890/onchange-event-on-input-type-range-is-not-triggering-in-firefox-while-dragging)直接改变img的padding、blur值。
> 其中，'onchange'只有在鼠标释放后才触发。

**缺点:**

   1. 要单独为每一个Input绑定一次事件。
   2. 考虑事件的回调函数如果用箭头函数来写，还会有this的坑。
   3. 如果有多个相同属性颜色变化，需要一个个去改

### 改进方案：
1. 通过[CSS变量](https://developer.mozilla.org/zh-CN/docs/Web/CSS/Using_CSS_variables)来控制background、padding、filter属性值，将这些属性值放到:root(即html上)，通过CSS变量来引用
2. 此时每次需要更新属性的时候只要更改下:root下的CSS变量即可
3. 可以通过自定义属性来识别当前的Input，没有必要一个个绑定事件

### 知识点：
1. data-*自定义属性，用于判断是否需要加"px"
2. :root添加复用的CSS变量（--background:'yellow'），子元素使用到该复用的变量时，通过var(--background)引用
3. 原生JS改变style样式通过element.style.setProperty()方法
4. HTML5的range滑块通过监听oninput事件来实时反馈行为
5. 通过[CSS滤镜](https://developer.mozilla.org/zh-CN/docs/Web/CSS/filter)提供毛玻璃效果