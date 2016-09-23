字体
-----
  
谷歌浏览器强制字体最小12px,可以通过缩放来解决这个问题

`-webkit-transform: scale(0.75);`  12*0.75 =9

注意：transform：scale()针对块级元素，会影响文字所在容器缩放。
注意：-webkit-text-size-adjust:none;只支持到chrome-27.0，现在最新版本为48.0
  
单位
-----
  
|css单位|定义       |计算规则|
|-------|:---------:|:-------|
|px     |           |        |
|em (font size of the element)  |  相对于父元素的字体大小的单位|依赖父元素|
|rem(font size of the root element)| 相对于根元素的字体大小的单位 |依赖根元素|


|移动端屏幕适配|特征|优缺点|
|--------------|----|------|
|流式布局|百分比定义宽度，高度大都是用px来固定住|大屏幕下页面元素宽度被拉的很长，但是高度还是和原来一样，非常的不协调|
|固定宽度|固定宽度，超出部分留白|大屏幕下页面小，两边留白|
|响应式  |@media|复杂性项目工作量大，维护难，费时费工|
|设置viewport|<meta name="viewport" content="width=320,maximum-scale=1.3,user-scalable=no">|部分页面元素变模糊|
|rem| | |
|zoom|| |
 

计算工具：http://pxtoem.com/


分辨率
------

场景：html body(overflow:hidden) 隐藏滚动轴下

|常见分辨率|窗口大小（win+chrome）不含书签栏|
|----------|:------------------------------:|
|1920*1080 |              1920*979|
|1600*900  |              1600*799|
|1366*768  |              1366*667|


盒模型
-------

技巧和经验
---------

[预/后处理](css/css-plus.md)

[1px on retina](css/1px-on-retina.md)



代码规范
--------
