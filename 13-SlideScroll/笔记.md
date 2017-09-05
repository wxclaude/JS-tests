### 实现效果
   滚轮滑到下面图片位置时，图片从侧方缓入效果

### 思路
1.  给图片设置transform、transition完成从左缓入的效果
2.  监听scroll事件，当滚到图片位置时触发图片缓入效果

### 知识点
1.  通过[debounce](http://www.css88.com/archives/tag/debounce)降低触发次数，减少影响性能问题
2.  元素的位置判断，涉及[多个位置属性](http://www.softwhy.com/forum.php?mod=viewthread&tid=8298)

    加上一张常用的图

    ![](http://www.softwhy.com/data/attachment/forum/201307/19/205303er94rvxa2plbdvat.gif)