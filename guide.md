# 安装


## CDN
------
对于制作原型或学习，你可以这样使用最新版本：	
```
<!-- 引入样式 -->
<link rel="stylesheet" href="https://cdn.jsdelivr.net/npm/master-photo/dist/masterphoto.css">
<!-- 引入组件库 -->
<script src="https://cdn.jsdelivr.net/npm/master-photo/dist/masterphoto.umd.min.js"></script>
```	

对于生产环境，我们推荐链接到一个明确的版本号和构建文件，以避免新版本造成的不可预期的破坏：
```
<!-- 引入样式 -->
<link rel="stylesheet" href="https://cdn.jsdelivr.net/npm/master-photo@0.1.0/dist/masterphoto.css">
<!-- 引入组件库 -->
<script src="https://cdn.jsdelivr.net/npm/master-photo@0.1.0/dist/masterphoto.umd.min.js"></script>
```	



## NPM 安装
------
```
npm install master-photo -S
```

### 安装说明

> 在安装 `fabric` 模块时，`fabric`会需要下载`canvas`依赖模块，`canvas`模块下载后，还会下载`node-canvas-prebuilt` 内容；
>
> 国内访问`Github`的速度大家都知道不咋地，当然通过设置镜像可以解决绝大多数问题，但是但是`node-canvas-prebuilt` 的文件下载，可以直接在`taobao`镜像网站找到，但是下载`canvas`模块时，走的还是`github`的地址，导致下载那个漫长。并且如果只是游览器端使用，并不需要用到`node-canvas-prebuilt`。
>
> 所以建议，将项目下载到本地后
>
> 1、在`package.json`文件中先删除`fabric`依赖
>
> 2、运行`npm i`安装命令
>
> 3、运行`npm i fabric`安装命令
>
> 4、安装`fabric`时，出现 `node-pre-gyp WARN Using request for node-pre-gyp https download` 信息时，结束安装
>
> 以上步骤，能保证顺利运行项目。PS:为何要先删`fabric`依赖信息，再装`fabric`，是因为本项目依赖`node-sass`，`node-sass`模块也需要下载二进制文件，不能保证在结束`fabric`模块安装时，已将`node-sass`二进制文件下载完毕，所导致的后续错误。

### 使用
```
import Vue from 'vue'
import Masterphoto from "master-photo";
import "master-photo/dist/masterphoto.css";

Vue.use(Masterphoto);
```



## Browser Support
------
Modern browsers and Internet Explorer 10+.


