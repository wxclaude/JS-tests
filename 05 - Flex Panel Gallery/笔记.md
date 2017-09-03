### 思路：
1. 首先进行布局，需要自适应调整各块的宽度，所以选择flex布局
2. 每一块分上、中、下文字区域，上下的文字区域通过transform移到外面去
3. 触发点击事件时，调整各部分样式：整个区域变大、中间文字变大、上下文字移入

### 涉及知识点：
1. [flex布局基础知识](http://www.ruanyifeng.com/blog/2015/07/flex-grammar.html)
2. transform: translateX/translateY
3. [HTML5 DOM元素类名相关操作API classList](http://www.zhangxinxu.com/wordpress/2013/07/domtokenlist-html5-dom-classlist-%E7%B1%BB%E5%90%8D/)给当前元素切换active效果