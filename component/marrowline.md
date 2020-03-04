# m-arrowline-tool 箭头按钮
自由绘制箭头

## 基本用法
```vue
/*vue*/
<desc>

将`m-arrowline-tool`放入`m-toolbar`插槽中即可

------
**请注意** 示例代码块中显示的插槽是`v-slot:footer=""`，实际代码并没有末尾的`=""`，应该是`v-slot:footer`

</desc>
<template>
  <div style="height:400px;">
	 	<m-view :src="defaultImgUrl">
      <template v-slot:footer>
        <m-toolbar>
          <m-arrowline-tool></m-arrowline-tool>
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

## 默认箭头大小与颜色
```vue
/*vue*/
<desc>

将`m-arrowline-tool`放入`m-toolbar`插槽中,设置`size`和`predefine`属性即可

------
**请注意** 示例代码块中显示的插槽是`v-slot:footer=""`，实际代码并没有末尾的`=""`，应该是`v-slot:footer`

</desc>
<template>
  <div style="height:400px;">
	 	<m-view :src="defaultImgUrl">
      <template v-slot:footer>
        <m-toolbar>
          <m-arrowline-tool :size="size" :predefine="predefine"></m-arrowline-tool>
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
				defaultImgUrl:"https://tangme.github.io/master-photo-doc/_media/photos.svg",
				size:[1,10,20],
				predefine:["#ffd700"]
			}
		}
	}
</script>
```

## Attributes
| 参数      | 说明     | 类型  | 可选值 | 默认值                                                       |
| --------- | -------- | ----- | ------ | ------------------------------------------------------------ |
| size      | 箭头大小 | Array | -      | [2, 4, 6]                                                    |
| predefine | 箭头颜色 | Array | -      | ["#ff4500","#ff8c00","#ffd700","#90ee90","#00ced1","#1e90ff","#c71585"] |