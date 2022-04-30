title:: myTable/actions

- | 配置项 | 描述 | 数据类型 | 默认值 | 可选值 | 版本 |
  |--|--|--|--|--|--|
  |label|按钮名称|String||||
  |toName|点击跳转路由的name值。[:br]该操作会以router.params的方式传递以下数据：[:br]{ ...this.$route.params, current: this.currentRow, selected: this.selected}|String||||
  |type|`<el-tag>`表现形式|String||primary[:br]success[:br]info[:br]warning[:br]danger||
  |forCurrent|只针对高亮行进行操作。[:br]为true时，只有高亮行时，该按钮才可操作。|Boolean||||
  |forSelected|只针对复选数据进行操作。[:br]为true时，只有复选行后，该按钮才可操作。|Boolean||||
  |elProps|`<el-button>`配置项|Object||||
  |handler({current, selected})|自定义点击事件[:br]current： 当前高亮行数据[:br]selected：复选行数据（须设置表格的type=selection）|Function||||