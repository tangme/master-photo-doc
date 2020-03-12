# m-filter 滤镜面板

提供滤镜选择，对比度，饱和度等操作

## 基本用法

```vue
/*vue*/
<desc>

将`m-filter`放入画布侧边栏插槽中，并按需设置打开的方向即可

------
**请注意** 示例代码块中显示的插槽是`v-slot:side=""`，实际代码并没有末尾的`=""`，应该是`v-slot:side`

</desc>
<template>
  <div style="height:400px;">
	<m-view :src="defaultImgUrl">
    	<template v-slot:side>
         	<m-filter></m-filter>
    	</template>
      	<template v-slot:footer>
        	<m-toolbar>
              <m-rect-tool></m-rect-tool>
              <m-ellipse-tool></m-ellipse-tool>
              <m-arrowline-tool></m-arrowline-tool>
              <m-pencil-tool></m-pencil-tool>
              <m-mosaic-tool></m-mosaic-tool>
              <m-text-tool></m-text-tool>
              <m-undo-tool></m-undo-tool>
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

## Attributes

| 参数      | 说明     | 类型   | 可选值     | 默认值 |
| --------- | -------- | ------ | ---------- | ------ |
| direction | 边框大小 | String | left/right | left   |