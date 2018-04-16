```
line-height:1.5
```
设置样式为1.5倍的行高 假如font-size:12px 那么line-height就是12*1.5＝18px。

```
user-select：none | text | all | element
none：文本不能被选择
text：可以选择文本
all：当所有内容作为一个整体时可以被选择。如果双击或者在上下文上点击子元素，那么被选择的部分将是以该子元素向上回溯的最高祖先元素。
element：可以选择文本，但选择范围受元素边界的约束
```
```
-webkit-tap-highlight-color: transparent
```
（移动端上）监听的元素被点击的时候会被高亮显示，比如android上表现为一个蓝框加上半透明的背景，和本来的样式不一样，就要去掉
```
<style type="text/css">
        ul{width:80%;height: 200px; list-style: none; font-size: 0;
         给父盒子加font-size：0可以去除默认空白间距 }
        li{width: 200px;height: 200px; background:pink; margin-left: 10px;
         display: inline-block;转换为行内块  font-size: 12px; 把字体大小改回来 }
</style>
```
盒子强制在一行显示：inline-block 属于标准流，因此比起浮动和定位，更为稳定。

```
vertical-align: top;
```
把元素的顶端与行中最高元素的顶端对齐
```
//html
<router-link tag="div" class="tab-item" to="/recommend">
   <span class="tab-link"></span>
</router-link>
//css
.tab-link
      color: $color-text-1
&.router-link-active
  .tab-link
      color: $color-theme
      border-bottom: 2px solid $color-theme
```
>当某个链接或元素被选中时可以时，需要改变其颜色或状态，而stylus中提供&选择器,&指向父选择器，用于判断父元素达到某条件时改变状态，下面的例子中当父元素router-link有被选中（active）时，子元素改变颜色并加上下划线。
