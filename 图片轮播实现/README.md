#图片轮播的实现
		这里有四种实现图片轮播的方式，通过JavaScript原生实现。
		很多大型网站都会用到图片轮播这个特效，其实使用jQuery就能简单快捷的实现，这里整合了4种使用原生js实现该特效的方法.
		也许我的方法不是最好的，还需要我再继续探索。

###第一种方法：[图片轮播1](https://github.com/Lemon23/JavaScript/blob/master/图片轮播实现/图片轮播1.html)
>#####效果：![P-1](https://github.com/Lemon23/JavaScript/raw/master/pic/P-1.png "图片轮播1效果图")
>>		设置间隔时间为4秒，点击图片左右的翻滚箭头可以手动触发下一张轮播图片。
>>		使用 offsetWidth 对象计算可见宽度，onclick() 点击触发函数。

###第二种方法：[图片轮播2](https://github.com/Lemon23/JavaScript/blob/master/图片轮播实现/图片轮播2.html)
>#####效果：![P-2](https://github.com/Lemon23/JavaScript/raw/master/pic/P-2.png "图片轮播2效果图")
>>		实现效果是图片不间断向上轮播，判断当图片滚到最底端时再跳到最顶端继续轮播。
>>		设置定时器，当鼠标移上时清除定时器达到滚动停止的效果，当鼠标移开时，重设定时器，图片继续轮播。

###第三种方法：[图片轮播3](https://github.com/Lemon23/JavaScript/blob/master/图片轮播实现/图片轮播3.html)
>>		利用数组放入图片进行轮播，这种方法代码简单，实现的效果也极其简单。
>>		没有设置onclick()点击触发函数，只是轮流播放图片。

###第四种方法：[图片轮播4](https://github.com/Lemon23/JavaScript/blob/master/图片轮播实现/图片轮播4.html)
>#####效果：![P-4](https://github.com/Lemon23/JavaScript/raw/master/pic/P-4.png "图片轮播4效果图")
>>		实现效果最完美的一个方案，设置了图片左右翻滚触发箭头，添加了图片左下角文字信息，还配置了右下角图片序号部分，也可以通过点击实现图片跳转。
>>		通过设置了定时器，每3秒变换一次图片，给左右箭头添加鼠标事件处理，根据图片组相对当前移动距离。
