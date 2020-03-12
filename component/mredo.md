# m-redo-tool 重做按钮
回退撤销功能操作

## 基本用法
```vue
/*vue*/
<desc>

将`m-redo-tool`放入`m-toolbar`插槽中即可

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
          <m-redo-tool></m-redo-tool>
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

## 隐藏标记

```vue
/*vue*/
<desc>

设置`hideBadge`即可

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
          <m-redo-tool hideBadge></m-redo-tool>
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

| 参数      | 说明           | 类型    | 可选值 | 默认值 |
| --------- | -------------- | ------- | ------ | ------ |
| hideBadge | 隐藏操作记录数 | Boolean | -      | false  |

