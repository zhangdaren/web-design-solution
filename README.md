# -
工作中碰到的各种疑难杂症留存，长期更新。


1.在IE浏览器中，下面这行代码引入的js文件将不会被加载：
<script type="text/javascript " src="../js/jquery-ui.min.js"></script> 
原因在于type="text/javascript " 多了一个空格。

2.IOS浏览器中，添加了click事件的元素，在点击时会有一个高亮半透明灰色矩形产生，去掉它，可以使用CSS：-webkit-tap-highlight-color: transparent;

3.table元素里，给td添加padding将会影响单元格边框厚度。


