title:: myForm/fields/fetchOptions

- LATER 异步获取候选项
- 示例
- ```js
  {
    label: '所在组',
      field: 'groupName',
        type: 'select',
          fetchOptions: async () => {
            const res = await this.$api.getUserGroup({
              limit: 99
            })
            return res.data.list.reduce((total, item) => {
              total.push({ label: item.groupName, value: item.id })
              return total
            }, [])
          }
  },
  
  ```
-
- 异步获取候选项,
- 最终需返回特定格式的数据
-