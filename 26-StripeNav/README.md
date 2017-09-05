### 实现效果
鼠标移到指定元素上时，下拉框以动画的形式进出

### 思路
1.  监听鼠标进入与移除事件，当鼠标进入菜单选项中时显示下拉菜单，并显示白色背景；鼠标移除时使下拉菜单和白色背景消失。
2.  过渡动画的实现原理大致如下：当鼠标移动到某一个选项后，首先使下拉菜单显示，但是在150ms内使其显示出来，这里用了`settimeout(fn,150)`，来延迟添加下拉菜单的`trigger-enter-active`类名，这样就会有一个过渡的效果了。

### 知识点

这里之所以使用[`translate3D`](http://www.zhangxinxu.com/wordpress/2012/09/css3-3d-transform-perspective-animate-transition/)，是因为translate3D属性会触发硬件加速，开启了硬件加速的`transform`是不会触发界面`repaint`的，拥有更好的性能。
