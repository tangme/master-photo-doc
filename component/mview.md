# m-view 画布
展示与编辑图片

## 仅展示图片
```vue
/*vue*/
<desc>

设置`src`属性，即可指定画布默认显示的图片

------
**请注意** 示例代码块中显示的插槽是`v-slot:header=""`，实际代码并没有末尾的`=""`，应该是`v-slot:header`

</desc>
<template>
  <div style="height:400px;">
	 <m-view :src="defaultImgUrl">
	 	<template v-slot:header>
			<m-viewbar>
			  <m-zoomin></m-zoomin>
			  <m-zoomnum></m-zoomnum>
			  <m-zoomout></m-zoomout>
			  <m-fitcenter></m-fitcenter>
			  <m-rotate direction="left"></m-rotate>
			  <m-rotate direction="right"></m-rotate>
			</m-viewbar>
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

## 编辑图片
```vue
/*vue*/
<desc>
将`m-toolbar`放入画布底部插槽中，并配置需要使用的编辑按钮即可

------
* **请注意** 示例代码块中显示的插槽是`v-slot:header=""`，实际代码并没有末尾的`=""`，应该是`v-slot:header`
* **请注意** 示例代码块中显示的插槽是`v-slot:footer=""`，实际代码并没有末尾的`=""`，应该是`v-slot:footer`
</desc>

<template>
  <div style="height:400px;">
	 <m-view :src="defaultImgUrl">
		  <template v-slot:header>
				<m-viewbar>
				  <m-zoomin></m-zoomin>
				  <m-zoomnum></m-zoomnum>
				  <m-zoomout></m-zoomout>
				  <m-fitcenter></m-fitcenter>
				  <m-rotate direction="left"></m-rotate>
				  <m-rotate direction="right"></m-rotate>
				</m-viewbar>
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

## Attributes 属性
| 参数     | 说明                                               | 类型     | 可选值 | 默认值   |
| -------- | -------------------------------------------------- | -------- | ------ | -------- |
| src      | 默认图片                                           | *String* | -      | -        |
| width    | 组件宽度，须提供单位 `px、%、`等                   | *String* | -      | 100%     |
| height   | 组件高度，须提供单位 `px、%、`等 PS:包涵工具栏高度 | *String* | -      | 100%     |
| bg-color | 默认背景颜色                                       | *String* | -      | \#1f2430 |

## Slot 插槽
| 名称   | 说明                  |
| ------ | --------------------- |
| header | 在 画布(canvas) 头部插入内容 |
| footer | 在 画布(canvas) 底部插入内容 |