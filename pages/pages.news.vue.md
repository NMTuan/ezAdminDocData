title:: pages/news.vue

- 新闻列表页
- ```vue
  <template>
    <my-table v-bind="tableProps" />
  </template>
  <script>
  export default {
    page: {
      name: '新闻列表'
    },
    data () {
      return {
        tableProps: {
          fetchApi: this.$api.getNewsList,
          fields: [
            { label: '编号', field: 'id' },
            { label: '标题', field: 'title' },
            { label: '摘要', field: 'description' },
            { label: '作者', field: 'author' },
            { label: '状态', field: 'state' },
            { label: '创建时间', field: 'createAt' }
          ]
        }
      }
    }
  }
  </script>
  
  ```