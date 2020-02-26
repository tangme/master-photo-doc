# master-photo
------

## master-photo是什么
> `master-photo` 是基于 `fabricjs`,`Element-ui`开发的一个可以编辑图片的组件库，提供在游览器环境上自由的编辑处理图片。[体验在线示例](https://tangme.github.io/master-photo-demo/)

## 更新日志

### 0.1.1
------
`2020-02-26`

#### 新特性

#### 问题修复
##### m-file-tool
* 保存图片调用`toDataURL`，捕获`SecurityError`异常
* 属性`btns`配置导致的显示问题


#### 优化
###### m-toolbar
* 新增默认slot
* 优化按钮间间隙

##### m-file-tool
* 画布无任何元素，保存时增加提示
* 操作文件按钮时，其它操作工具栏未隐藏配置

#### 非兼容性更新
###### m-toolbar
* 移除 `tools` 属性

### 0.1.0 Spark
------
`2020-02-24`
* 初始化项目，完成16个基础组件