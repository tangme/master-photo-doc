# m-mosaic-tool 马赛克按钮
自会绘制马赛克
## 基本用法
```vue
/*vue*/
<desc>

将`m-mosaic-tool`放入`m-toolbar`插槽中即可

------
**请注意** 示例代码块中显示的插槽是`v-slot:footer=""`，实际代码并没有末尾的`=""`，应该是`v-slot:footer`

</desc>
<template>
  <div style="height:400px;">
	 	<m-view :src="defaultImgUrl">
      <template v-slot:footer>
        <m-toolbar>
          <m-mosaic-tool></m-mosaic-tool>
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

## 默认马赛克画笔大小
```vue
/*vue*/
<desc>

将`m-mosaic-tool`放入`m-toolbar`插槽中,设置`size`属性即可

------
**请注意** 示例代码块中显示的插槽是`v-slot:footer=""`，实际代码并没有末尾的`=""`，应该是`v-slot:footer`

</desc>
<template>
  <div style="height:400px;">
	 	<m-view :src="defaultImgUrl">
      <template v-slot:footer>
        <m-toolbar>
          <m-mosaic-tool :size="size"></m-mosaic-tool>
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
| 参数 | 说明     | 类型  | 可选值 | 默认值    |
| ---- | -------- | ----- | ------ | --------- |
| size | 画笔大小 | Array | -      | [2, 4, 6] |