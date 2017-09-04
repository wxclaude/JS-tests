### 实现效果
主要实现一个控制视频播放速率的效果

### 思路
监听右侧滑块的`mousemove`事件，计算出现在的速率，然后改变`video`的`playbackRate`属性

### 知识点
1.  通过`(max - min) * percent + min`计算当前速率
2.  [`video.playbackRate`](https://developer.mozilla.org/zh-CN/docs/Web/API/HTMLMediaElement/playbackRate)代表视频的播放速率，是一个可读可写的属性，因此我们可直接为该属性赋值。