# m-undo-tool 撤销按钮
提供撤销之前编辑的操作

## 基本用法
```
/*vue*/
<desc>

将`m-undo-tool`放入`m-toolbar`插槽中即可

------
**请注意** 示例代码块中显示的插槽是`v-slot:footer=""`，实际代码并没有末尾的`=""`，应该是`v-slot:footer`

</desc>
<template>
  <div style="height:400px;">
	 	<m-view :src="defaultImgUrl">
      <template v-slot:footer>
        <m-toolbar>
          <m-rect-tool></m-rect-tool>
          <m-undo-tool></m-undo-tool>
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