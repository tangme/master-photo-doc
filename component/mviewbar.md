# m-viewbar 查看工具栏
提供查看相关按钮的展示

## 基本用法
```vue
/*vue*/
<desc>

将`m-viewbar`放入画布顶部插槽中，并配置需要使用的按钮即可

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

## Slot
| 名称    | 说明               |
| ------- | ------------------ |
| default | 查看工具栏默认插槽 |