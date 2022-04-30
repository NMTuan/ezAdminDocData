- ## 介绍
  background-color:: #787f97
	-
	- 表单对话框页
	-
	- 后台管理中, 大量的添加/编辑操作, 都涉及到表单.
	- 为了轻松愉快的制作这些表单页面.
	- 基于`myDialog`和`myForm`, 制作了此组件.
	- 为防止用户填写表单时出现对话框异常关闭的问题. `dialogProps`中固定了几个配置
		- `close-on-click-modal="false"` 不允许点击遮罩层关闭对话框
		- `close-on-press-escape="false"` 不允许通过按`ESC`键关闭对话框
	-
- ## 示例 example.vue
  background-color:: #787f97
	- ```vue
	  <template>
	    <my-dialog-form
	      v-model="formData"
	      :dialog-props="dialogProps"
	      :form-props="formProps"
	    >
	      <!-- 123 -->
	    </my-dialog-form>
	  </template>
	  <script>
	  export default {
	    page: {
	      name: '表单对话框'
	    },
	    data () {
	      return {
	        formData: {
	          name: 123
	        },
	        dialogProps: {
	          title: '创建用户信息'
	        },
	        formProps: {
	          fields: [
	            { label: '姓名', field: 'name' },
	            { label: '年龄', field: 'age' },
	            {
	              label: '性别',
	              field: 'sex',
	              options: [
	                { label: '男', value: '1' },
	                { label: '女', value: '2' },
	                { label: '未知', value: '0' }
	              ]
	            }
	          ],
	          // fetchApi: this.$api.fetchForm,
	          submitApi: this.$api.updateForm
	        }
	      }
	    }
	  }
	  </script>
	  ```
- ## 配置 :attribute="value"
  background-color:: #787f97
	- |配置项|描述|数据类型|默认值|可选值|版本|
	  |--|--|--|--|--|--|
	  |value / v-model|表单绑定值|Object||||
	  |[[dialogProps]]|对话框配置|Object||||
	  |[[formPorps]]|表单配置|Object||||
- ## 插槽 \#slotName=\"payload\"
  background-color:: #787f97
	- |插槽|描述|参数|版本|
	  |--|--|--|--|
	  ||每个表单项都有一个插槽, 插槽名称为表单项的`field`值|||
- ## 事件 @eventName="handle"
  background-color:: #787f97
	- |事件|描述|参数|版本|
	  |--|--|--|--|
	  |input|当表单数据发生改变时触发|([[formData]])||
- ## 方法 $refs[].method()
  background-color:: #787f97
	- |方法|描述|参数|版本|
	  |--|--|--|--|
	  |||||
-