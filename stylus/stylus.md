## 安装stylus
>npm install stylus stylus-loader --save-dev
## 在.vue文件stylus的使用
在style标签加上lang='stylus'
```
<style scoped lang="stylus">
  #app
    height 80px
    min-width 800px
</style>
```
## 外部引用.styl文件
```
<style lang="stylus">
  @import "assets/base.styl";
  #app
    color #2c3e50
</style>
```
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
