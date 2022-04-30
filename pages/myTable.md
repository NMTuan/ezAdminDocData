- ## 介绍
  background-color:: #787f97
	-
	- 表格列表页
	-
	- 后台管理的数据展现中, 最常用的一种方式就是表格列表.
	- 此组件简化了表格列表的编码开发时间.
	- 此组件集成了以下内容:
		- 数据表格
		- 数据行的操作
		- 数据单元的展示
		- 分页
		- 操作按钮
		- 搜索
		- 高级搜索
	-
- ## 示例 example.vue
  background-color:: #787f97
	- ```vue
	  <template>
	    <my-table v-bind="tableProps" />
	  </template>
	  <script>
	  export default {
	    page: {
	      name: '表格',
	      sort: 200
	    },
	    data () {
	      return {
	        tableProps: {
	          // 列表配置
	          fields: [
	            { label: '战争名称', field: 'name' },
	            { label: '时间/年', field: 'date'},
	            { label: '双方统帅', field: 'leader'},
	            { label: '结果', field: 'result' },
	            // 列表数据操作项
	            { label: '操作', type: 'action',
	              actionItems: [
	                {
	                  label: '详情',
	                  toName: 'history-detail',
	                  handler () {
	                  }
	                }
	              ]
	            }
	          ],
	          // 数据来源
	          fetchApi: this.$api.myTable,
	          // 操作项
	          actions: [
	            {
	              label: '添加',
	              toName: 'history-create'
	            }
	          ],
	          // 搜索项
	          searchItems: [
	            { label: '战争名称', field: 'titleA' }
	          ],
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
	  |[fields](myTable/fields)|列配置|||||
	  |type|显示类型|||||
	  |elProps|elementUI配置项|||||
	  |data|静态数据|||||
	  |fetchApi|异步数据接口|||||
	  |fetchFields|发起异步请求时的参数|||||
	  |fetchDataKey|异步响应中, 表格数据的key|||||
	  |fetchTotalKey|异步响应中, 总条数的key|||||
	  |queryPageKey|搜索参数: 页码的参数名|||||
	  |queryLimitKey|搜索参数: 条数的参数名|||||
	  |queryLimitValue|搜索参数: 每页显示条数|||||
	  |[actions](myTable/actions)|表格操作项|||||
	  |[searchItems](myTable/searchItems)|搜索项|||||
	  |searchItemsLimit|限制界面上搜索项的数量, 0为不限.|Number|0|||
- ## 插槽 \#slotName=\"payload\"
  background-color:: #787f97
	- |插槽|描述|参数|版本|
	  |--|--|--|--|
	  |fields[].field.replaceAll('.', '_')|表格列插槽。以列field为名字的插槽。[:br]当内置的展示方式无法满足时，可使用此插槽。|{ field, row, rowIndex, column, columnIndex, value }||
	  |beforeTable表格前插槽。|表格前插槽。|{ fetchData }||
	  |afterTable|表格后插槽。|{ fetchData }||
- ## 事件 @eventName="handle"
  background-color:: #787f97
	- |事件|描述|参数|版本|
	  |--|--|--|--|
	  |reloaded|页面数据重载后的钩子|||
- ## 方法 $refs[].method()
  background-color:: #787f97
	- |方法|描述|参数|版本|
	  |--|--|--|--|
	  |||||