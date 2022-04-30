- ## 介绍
  background-color:: #787f97
	-
	- 表单组件页
	-
	- 基于`elementUI`的表单组件.
	- 无需维护大量的表单代码, 直接通过json配置整个表单.
	-
	- 目前已支持的表单项有:
	- {{embed ((6260c174-773b-47b0-b76b-38d165698cfc))}}
	-
- ## 示例 example.vue
  background-color:: #787f97
	- ```vue
	  <template>
	    <my-form v-bind="props" />
	  </template>
	  <script>
	  export default {
	    page: {
	      name: '表单'
	    },
	    data () {
	      return {
	        props: {
	          fields: [
	            { label: '姓名', field: 'name' },
	            {
	              label: '性别',
	              field: 'sex',
	              type: 'select',
	              options: [
	                { label: '男', value: '1' },
	                { label: '女', value: '2' },
	                { label: '未知', value: '0' }
	              ]
	            }
	          ]
	        }
	      }
	    }
	  }
	  </script>
	  ```
- ## 配置 :attribute="value"
  background-color:: #787f97
	- id:: 625e6637-15ca-4e66-9f94-7f0de72951eb
	  |配置项|描述|数据类型|版本|
	  |--|--|--|--|
	  |value / v-model|绑定值|Object||
	  |[fields](myForm/fields)|表单项的配置|Array||
	  |[buttons](myForm/buttons)|表单按钮的配置|Array||
	  |[fetchApi](myForm/fetchApi)|进入表单页时, 拉取表单数据的接口|Function||
	  |[fetchFields](myForm/fetchFields)|拉取表单数据时, 传递的参数|Array, Object||
	  |[handleFetchData()](myForm/handleFetchData)|自定义请求回来的数据|Function||
	  |afterFetched(formData, res)|完成数据处理后的钩子|Function||
	  |beforeSubmit(formData)|表单提交前的数据处理|Function||
	  |[submitApi](myForm/submitApi)|表单提交的接口|Function||
	  |succeed(res)|提交成后的数据处理|Function||
	  |[cancel()](myForm/cancel)|取消操作|Function||
	  |elProps|elementUI的配置|Object||
- ## 插槽 \#slotName=\"payload\"
  background-color:: #787f97
	- | 插槽 | 描述 | 参数 | 版本 |
	  |---|---|---|---|
	  |||||
- ## 事件 @eventName="handle"
  background-color:: #787f97
	- |事件|描述|参数|版本|
	  |--|--|--|--|
	  |input|当表单数据发生改变时触发|(formData)||
- ## 方法 $refs[].method()
  background-color:: #787f97
	- |方法|描述|参数|版本|
	  |--|--|--|--|
	  |||||
-