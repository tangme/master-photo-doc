# m-toolbar 编辑工具栏
提供编辑相关操作的按钮

## 基本用法
```vue
/*vue*/
<desc>

将`m-toolbar`放入画布顶部插槽中，并配置需要使用的按钮即可

------
**请注意** 示例代码块中显示的插槽是`v-slot:footer=""`，实际代码并没有末尾的`=""`，应该是`v-slot:footer`

</desc>
<template>
  <div style="height:400px;">
	 	<m-view :src="defaultImgUrl">
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

## Slot
| 名称   | 说明                  |
| ------ | --------------------- |
| default | toolbar 默认插槽 |
| begin | toolbar 左侧插入内容 |
| end | toolbar 右侧插入内容 |