# master-photo
------

## master-photo是什么
> `master-photo` 是基于 `fabricjs`,`Element-ui`开发的一个可以编辑图片的组件库，提供在游览器环境上自由的编辑处理图片。[体验在线示例](https://tangme.github.io/master-photo-demo/)

## 更新日志

### 0.1.2
------
`2020-03-03`

#### 新特性
#### m-undo-tool
* ~~新增标记，用于显示可撤销的记录数~~
* ~~新增隐藏标记属性`hideBadge`~~

### 优化

#### m-undo-tool

* ~~无可撤销的记录时，设置按钮不可用~~
* ~~优化`画笔、马赛克、文字工具`撤销问题~~

### 问题修复

#### m-mosaic-tool

* `size `属性设置无效问题


### 0.1.1
------
`2020-02-26`

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