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
