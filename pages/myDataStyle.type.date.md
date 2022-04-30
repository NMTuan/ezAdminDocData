title:: myDataStyle/type/date

- 把时间戳的数据格式化为约定的日期格式。
- LATER 接受10位或13位的时间戳。
  :LOGBOOK:
  CLOCK: [2022-04-22 Fri 17:18:14]--[2022-04-22 Fri 17:18:15] =>  00:00:01
  :END:
- | props配置项 | 描述 | 数据类型 | 默认值 | 可选值 | 版本 |
  |--|--|--|--|--|--|
  |format|格式化数据, 这里使用`day.js`处理.[:br]格式详见[这里](https://dayjs.gitee.io/docs/zh-CN/display/format)|String|"YYYY-MM-DD"|||
  |empty|空值, 零值时显示的内容|String|""|||