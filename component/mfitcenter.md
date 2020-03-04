# m-fitcenter 缩放居中
将画布元素适应画布大小居中显示

## 基本用法
```vue
/*vue*/
<desc>

将`m-fitcenter`放入`m-viewbar`插槽中即可

------
**请注意** 示例代码块中显示的插槽是`v-slot:header=""`，实际代码并没有末尾的`=""`，应该是`v-slot:header`

</desc>
<template>
  <div style="height:400px;">
	 <m-view :src="defaultImgUrl">
	 	<template v-slot:header>
			<m-viewbar>
			  <m-zoomin></m-zoomin>
			  <m-fitcenter></m-fitcenter>
			  <m-zoomout></m-zoomout>
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