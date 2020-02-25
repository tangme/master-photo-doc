# m-file-tool

## Attributes
| 参数                       | 说明                    | 类型    | 可选值        | 默认值 |
| -------------------------- | ----------------------- | ------- | ------------- | ------ |
| btns                       | 配置文件按钮            | Object  | -             |        |
| btns.localfile             | 是否显示打开本地按钮    | Boolean | true/false    | true   |
| btns.onlinefile            | 是否显示打开在线按钮    | Boolean | true/false    | true   |
| btns.savelocal             | 是否显示保存本地按钮    | Boolean | true/false    | true   |
| btns.savecloud             | 是否显示保存服务端按钮  | Object  |               |        |
| btns.savecloud.url         | 服务端接口地址          | String  | -             | -      |
| btns.savecloud.contentType | 提交时 请求头部内容类型 | String  | json/formdata | json   |