- ## 介绍
  background-color:: #787f97
	-
	- 对话框组件页
	- 基于`el-dialog`组件, 加入了路由处理等逻辑.
	- 与`el-dialog`区别如下:
		- 1. `visible`属性不可配置, 永远为`true`. 无需担心对话框的显示状态, 全部集成到路由中去了.
		  2. `append-to-body`属性默认值改为了`true`. 防止可能出现的渲染异常.
	-
- ## 示例 example.vue
  background-color:: #787f97
	- ```vue
	  <template>
	    <my-dialog :dialog-props="dialogProps">
	      这里是对话框内容
	    </my-dialog>
	  </template>
	  <script>
	  export default {
	    page: { name: '常规对话框' },
	    data () {
	      return {
	        dialogProps: {
	          title: '对话框的标题',
	          width: '320px',
	          top: '10px'
	        }
	      }
	    }
	  }
	  </script>
	  ```
- ## 配置 :attribute="value"
  background-color:: #787f97
	-
	- 由于`myDialog`是对`el-dialog`的简单包装, 所以`el-dialog`的配置也适用于`myDialog`.
	- #+BEGIN_NOTE
	  但需要注意: 
	  
	  这里所有的配置项不是直接绑定到`<my-dialog>`的, 
	  而是包在了一个元素`dialog-props`中
	  #+END_NOTE
	- |配置项|描述|数据类型|默认值|可选值|版本|
	  |--|--|--|--|--|--|
	  |[[dialogProps]]|对话框配置项|Object||||
	-
- ## 插槽 \#slotName=\"payload\"
  background-color:: #787f97
	- |插槽|描述|参数|版本|
	  |--|--|--|--|
	  |default|对话框内容插槽|||
- ## 事件 @eventName="handle"
  background-color:: #787f97
	- |事件|描述|参数|版本|
	  |--|--|--|--|
	  |||||
- ## 方法 $refs[].method()
  background-color:: #787f97
	- |方法|描述|参数|版本|
	  |--|--|--|--|
	  |||||
-