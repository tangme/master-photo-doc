# m-file-tool 文件按钮
提供打开，保存文件功能

## 基本用法
```
/*vue*/
<desc>

将`m-file-tool`放入`m-toolbar`插槽中即可

------
**请注意** 示例代码块中显示的插槽是`v-slot:footer=""`，实际代码并没有末尾的`=""`，应该是`v-slot:footer`

</desc>
<template>
  <div style="height:400px;">
	 	<m-view :src="defaultImgUrl">
      <template v-slot:footer>
        <m-toolbar>
          <m-rect-tool></m-rect-tool>
          <m-file-tool></m-file-tool>
        </m-toolbar>
      </template>
    </m-view>
	</div>
</template>
<script>
export default {
	data() {
		return {
			defaultImgUrl:"https://tangme.github.io/master-photo-doc/_media/photos.svg"
		}
	}
}
</script>
```

## 设置默认显示按钮
```
/*vue*/
<desc>

将`m-file-tool`放入`m-toolbar`插槽中即可

------
**请注意** 示例代码块中显示的插槽是`v-slot:footer=""`，实际代码并没有末尾的`=""`，应该是`v-slot:footer`

</desc>
<template>
	<div>
		<h5>仅显示 打开新文件、保存至本地 按钮</h5>
		<div style="height:400px;">
			<m-view :src="defaultImgUrl">
				<template v-slot:footer>
	        <m-toolbar>
	          <m-file-tool :btns="onlyLocal"></m-file-tool>
	        </m-toolbar>
	      </template>
	    </m-view>
		</div>
		<h5>仅显示 在线新文件、保存至云 按钮</h5>
		<div style="height:400px;">
			<m-view :src="defaultImgUrl">
				<template v-slot:footer>
	        <m-toolbar>
	          <m-file-tool :btns="onlyOnline"></m-file-tool>
	        </m-toolbar>
	      </template>
	    </m-view>
		</div>
	</div>
</template>
<script>
	export default {
		data() {
			return {
				defaultImgUrl:"https://tangme.github.io/master-photo-doc/_media/photos.svg",
				onlyLocal:{onlinefile:false},
				onlyOnline:{
					localfile:false,
					savelocal:false,
					savecloud:{
						url:'设定保存图片的服务器接口地址即可显示此按钮'
						}
					}
			}
		}
	}
</script>
```

## Attributes
| 参数                       | 说明                    | 类型    | 可选值        | 默认值 |
| -------------------------- | ----------------------- | ------- | ------------- | ------ |
| btns                       | 配置文件按钮            | Object  | -             |        |
| btns.localfile             | 是否显示打开本地按钮    | Boolean | true/false    | true   |
| btns.onlinefile            | 是否显示打开在线按钮    | Boolean | true/false    | true   |
| btns.savelocal             | 是否显示保存本地按钮    | Boolean | true/false    | true   |
| btns.savecloud             | 是否显示保存服务端按钮  | Object  |               |        |
| btns.savecloud.url         | 服务端接口地址          | String  | -             | -      |
| btns.savecloud.contentType | 提交时 请求头部内容类型 | String  | json/formdata | json   |