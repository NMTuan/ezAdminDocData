title:: myForm/buttons/command

- 当前按钮的点击事件.
- 如果配置了此项.
- 则在点击按钮的时候, 会触发$emit('commandValue', payload)
- payload中会传递以下内容
	- |配置项|描述|数据类型|默认值|可选值|版本|
	  |--|--|--|--|--|--|
	  |form|$el.form[:br]主要用于触发一些表单方法.|||||
	  |formData|表单数据|Object||||
	  |changeLoading(Boolean)|切换表单loading状态[:br]传true开启loading[:br]否则结束loading|||||
	  |submit()|内置的表单提交方法|||||
	  |cancel()|内置的取消操作|||||
- #+BEGIN_NOTE
  注意:
  
  如果按钮不配置command, 则走内置逻辑.
  第一个按钮会触发内置的`submit()`方法.
  第二个按钮会触发内置的`cancel()`方法.
  #+END_NOTE
-