### 实现效果：
使用浏览器的摄像头，实时记录影像，并输出到canvas中，并用canvas对图像进行滤镜的处理。

### 知识点：
1.  `navigator.mediaDevices.getUserMedia()`方法提示用户允许使用视频或者音频设备，如果用户点击允许，则返回一个Promise对象，MediaStream对象作为此Promise对象的Resolved［成功］状态的回调函数参数；但如果用户点击拒绝或者媒体可以用的时候，同样返回一个Promise对象，且PermissionDeniedError或者NotFoundError作为此Promise的Rejected［失败］状态的回调函数参数。但是，用户也可以直接取消选择，不同意也不拒绝，所以返回的Promise对象可能既不会触发resolve 也不会触发 reject。参数为一个对象，包含要请求的视频和音频情况，布尔类型，请求权限的话为true，vice via。 更详细的内容还请进一步查阅[参考文档](https://developer.mozilla.org/zh-CN/docs/Web/API/MediaDevices/getUserMedia)。
2.  `URL.createObjectURL()`方法是为了创建一个 DOMString 包含一个表示参数中给定的对象的URL。这个 URL 的生命周期和创建它的窗口中的 document 绑定。这个新的URL 对象表示着指定的 File 对象或者 Blob 对象。 （DOMString 是一个UTF-16字符串。由于JavaScript已经使用了这样的字符串，所以DOMString直接映射到一个String。） 更详细的内容请进一步查看[参考文档](https://developer.mozilla.org/zh-CN/docs/Web/API/URL/createObjectURL)。
3.  canvas绘图部分

    -   `ctx.drawImage()`更够将当前的视频流（video）中的一帧画在canvas中。
    -   `ctx.getImageData()`返回一个ImageData对象，用来描述canvas区域隐含的像素数据，这个区域通过矩形表示，起始点为(sx, sy)、宽为sw、高为sh。[参考文档](https://developer.mozilla.org/zh-CN/docs/Web/API/CanvasRenderingContext2D/getImageData)
    -   `ctx.putImageData()`是 Canvas 2D API 将数据从已有的 ImageData 对象绘制到位图的方法。 如果提供了脏矩形，只能绘制矩形的像素。[参考文档](https://developer.mozilla.org/zh-CN/docs/Web/API/CanvasRenderingContext2D/putImageData)
    -   imagedata中有大量的数据，其中分别代表了图片的颜色信息，分别为red，green，blue，alpha的值，因此我们可以同添加自定义滤镜，通过改变颜色的rgba的值，控制页面的效果。

4.  摄像记录导入canvas

    -   在没次点击照相的时候，都要求播一遍音效，并且为了模拟现实情况，我们在用户点击时，设置当前的播放时间为0，再播放音效。
    -   `canvas.toDataURL('image/jpeg');`方法返回一个包含图片展示的 data URI 。可以使用 type 参数其类型，默认为 PNG 格式。图片的分辨率为96dpi。[参考文档](https://developer.mozilla.org/zh-CN/docs/Web/API/HTMLCanvasElement/toDataURL)
    -   接下来新建一个a元素，设置其href的值为data。在插入在文档中。实现截图成功的效果。
