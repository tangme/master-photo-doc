# m-rotate 旋转按钮
将画布元素进行旋转

## 基本用法
```
/*vue*/
<desc>

将`m-rotate`放入`m-viewbar`插槽中，并设置`direction`旋转方向属性即可

------
**请注意** 示例代码块中显示的插槽是`v-slot:header=""`，实际代码并没有末尾的`=""`，应该是`v-slot:header`

</desc>
<template>
  <div style="height:400px;">
	 <m-view :src="defaultImgUrl">
	 	<template v-slot:header>
			<m-viewbar>
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

## Attributes 属性
| 参数     | 说明                                               | 类型     | 可选值 | 默认值   |
| -------- | -------------------------------------------------- | -------- | ------ | -------- |
| direction      | 旋转方向                                     | *String* | right/left      | right        |
