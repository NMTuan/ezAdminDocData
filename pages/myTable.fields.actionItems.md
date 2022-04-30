title:: myTable/fields/actionItems

- | 配置项 | 描述 | 数据类型 | 默认值 | 可选值 | 版本 |
  |--|--|--|--|--|--|
  |label||String||||
  |toName||String||||
  |type|操作按钮表现形式|String||primary[:br]success[:br]info[:br]warning[:br]danger||
  |hidden|某些状态下隐藏该操作项[:br]例：hidden: {key: [1,2,3]}[:br]当前行中，如果key的值为1、2或3时，当前按钮隐藏|Object||||
  |auth|功能权限的判断（判断路由name）[:br]有toName的时候可省略，按照toName去判断权限|String||||
  |handler(row)|自定义点击事件|Function||||