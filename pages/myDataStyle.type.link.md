- 为当前数据增加超链接。
- | props配置项 | 描述 | 数据类型 | 默认值 | 可选值 | 版本 |
  |--|--|--|--|--|--|
  |toName|点击跳转路由的name值。[:br]该操作会以router.params的方式传递以下数据：[:br]{ ...this.$route.params, ...data }|String||||
  |byRef|传递相关数据(表格行)|Boolean|true|||
  |handleRef(data)|自定义数据传递|Function||||
  |class|className样式|String|text-primary-400[:br]hover:underline|||