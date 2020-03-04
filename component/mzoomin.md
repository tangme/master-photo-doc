# m-zoomin 放大按钮
将画布整体放大

## 基本用法
```vue
/*vue*/
<desc>

将`m-zoomin`放入`m-viewbar`插槽中即可

------
**请注意** 示例代码块中显示的插槽是`v-slot:header=""`，实际代码并没有末尾的`=""`，应该是`v-slot:header`

</desc>
<template>
  <div style="height:400px;">
	 <m-view :src="defaultImgUrl">
	 	<template v-slot:header>
			<m-viewbar>
			  <m-zoomin></m-zoomin>
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