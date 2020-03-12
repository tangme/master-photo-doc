# m-clear-tool 清空按钮
清楚所有编辑

## 基本用法
```vue
/*vue*/
<desc>

将`m-clear-tool`放入`m-toolbar`插槽中即可

------
**请注意** 示例代码块中显示的插槽是`v-slot:footer=""`，实际代码并没有末尾的`=""`，应该是`v-slot:footer`

</desc>
<template>
  <div style="height:400px;">
  	<m-view :src="defaultImgUrl">
      <template v-slot:footer>
        <m-toolbar>
          <m-rect-tool></m-rect-tool>
          <m-clear-tool></m-clear-tool>
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

## 

