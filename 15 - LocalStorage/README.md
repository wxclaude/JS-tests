### 实现效果：
实现一个todo list，可以添加item，并且点击item可以改变其状态，将所有item存到localstorage中，以保证刷新后不消失

### 思路：
1.  页面加载时，先获取本地缓存items，如果没有，就初始化为空数组
2.  给add按钮绑定事件，点击时将输入的item添加到本地存储
3.  给checkbox绑定事件，点击时切换checkbox状态，并更新本地存储

### 知识点
[localstorage](https://developer.mozilla.org/en-US/docs/Web/API/Window/localStorage)常用API：
-   myStorage = window.localStorage; //获取方式
-   localStorage.setItem(‘key’,value); //设置本地缓存，以key-value的形式
-   localStorage.getItem("myCat"); //根据参数key取得本地缓存中对应的值
[sessionstorage](https://developer.mozilla.org/en-US/docs/Web/API/Window/sessionStorage)常用API：
-   sessionStorage.setItem('key', 'value'); //保存数据到sessionStorage
-   var data = sessionStorage.getItem('key'); //获取sessionStorage里的数据
-   sessionStorage.removeItem('key'); //移除sessionStorage里的某条数据
-   sessionStorage.clear(); //移除sessionStorage里的所有数据
