title:: myTable/fields

- | 配置项 | 描述 | 数据类型 | 默认值 | 可选值 | 版本 |
  |--|--|--|--|--|--|
  |label|列标题|String||||
  |field|列字段名[:br]可以是带 `.` 的字符串，会自动分割找相应对象内的数据。[:br]注意：在插槽中，名称中的 `.` 会替换成 `_` 。|String||||
  |type|列展示类型，[:br]如果值为`action`，则为操作列[:br]其它值走`<my-data-style>` 组件统一处理|String||||
  |[actionItems](myTable/fields/actionItems)|行操作项，详见下方相关章节|Function||||
  |formatter|实现了`<el-table-column>` 的formatter方法|Function||||
  |elPorps|<el-table-column> 配置项|Object||||