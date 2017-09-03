### 思路：
目的是实现鼠标按下并拖拽时类似画笔的效果，画出来的线条有2个特点：
1. 刚开始粗细随机，随着绘画进行，会**随机渐粗或渐细**，在达到最粗或者0时改变渐变方向
2. 绘制过程中随机改变颜色

### 知识点：
1. [Canvas用法](https://developer.mozilla.org/zh-CN/docs/Web/API/Canvas_API)

> 不用多说，就是用canvas画的

2. 用变量改变[HSL色彩模式](http://mothereffinghsl.com/)来实现改变线条颜色

> 通俗来讲，就是色调、饱和度、亮度