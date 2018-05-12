# 我遇到的一些疑难杂症

标签（空格分隔）： Web前端 js css html

---

以下是我工工作中碰到的各种疑难杂症留存，长期更新。



1. IE浏览器script type属性含多余空格，将不会加载此js文件
如下面代码写法，此js文件将不会加载：
<br>
```<script type="text/javascript " src="../js/jquery-ui.min.js"></script>```
<br>
解决方法，去掉这个多余的引号。只在IE里碰到过，具体版本已忘。
</br>
</br>
</br>
2. 移动端，元素添加了click，在点击时，会有高亮半透明灰色矩形产生，可以使用如下CSS即可去掉。
<br>
    `-webkit-tap-highlight-color: transparent;`
</br>
</br>
</br>
3. 点点点的处理
<br>
`/*PC端点点点(移动端用这个+rem布局时会从字的头部切掉5%左右)*/`
`text-overflow : ellipsis; `
`white-space : nowrap; `
`overflow : hidden; `
<br>
`/*移动端点点点*/`
`display: -webkit-box;`
`-webkit-line-clamp: 1;`
`-webkit-box-orient: vertical;`
`overflow : hidden; `
</br>
</br>
</br>

4. 一整屏渐变背景，在手机上给body添加渐变背景时，如果内容已经超出一屏时（一屏等于100vh，即屏幕显示的高度，非body滚动高度），渐变背景会重复的在第二屏显示。如果想不管body的高度是几屏都是一个完整的渐变，那可以采用以下css：
<br>
`background: linear-gradient(to top, #9A28FD, #A328FD) fixed;`
`background: -webkit-gradient(linear, 0 0, 0 bottom, from(#9A28FD), to(#A328FD)) fixed;`
</br>
</br>
</br>

5. 有时候，需要做按钮的active效果，直接添加:active在PC端是正常的，在移动端却无法响应，此时可以给body添加一个空的事件即可解决，代码如下：
<br>
`<body ontouchstart="">`
</br>
</br>
</br>

6. `new date(2012-02-22 12:00:00)` 这种形式，在ios里不生效。解决方法：将 - 替换为 / 即可。
</br>
</br>
</br>

7. 更多待更新……

----------
待考问题，之前记录时，只留只言片语，未作详细记录。

1. 在table元素,手动给th/td创建边框时，给td添加padding值将会影响单元格边框厚度，呈现的效果就是有些边框正常，有些边框是加粗的。（事后未重现，有待考究）
</br>
</br>
2. json文本里`，`对应的ASCII码为 9，解析有问题(记录留存，重现待考)
