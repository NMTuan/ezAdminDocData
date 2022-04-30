- ## 介绍
  background-color:: #787f97
	-
	- 确认对话框页
	-
	- 在管理系统中, 会频繁碰到需要确认的操作, 比如: 切换数据状态, 置顶, 下线, 删除等.
	- 此组件就是为了方便快捷的处理这些操作.
	-
	- 通过简单的配置即可完成一个带[[功能权限]]的操作确认.
	-
- ## 示例 example.vue
  background-color:: #787f97
	- ```vue
	  <template>
	    <my-dialog-confirm
	      :dialog-props="dialogProps"
	      :confirm-props="confirmProps"
	    >
	      操作后数据将无法找回, 确定要操作吗?
	    </my-dialog-confirm>
	  </template>
	  <script>
	  export default {
	    page: { name: '确认对话框' },
	    data () {
	      return {
	        dialogProps: {
	          title: '删除'
	        },
	        confirmProps: {
	          submitText: '删除',
	          submitType: 'danger',
	          submitApi: this.$api.confirm
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
	  |[[dialogProps]]|对话框配置|Object||||
	  |[[confirmProps]]|确认框配置|Object||||
- ## 插槽 \#slotName=\"payload\"
  background-color:: #787f97
	- |插槽|描述|参数|版本|
	  |--|--|--|--|
	  |default|内容插槽|||
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