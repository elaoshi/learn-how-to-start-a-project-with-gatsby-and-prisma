# 前台 ，添加用户

打开浏览器
http://localhost:4466/myapp/dev/


输入以下命令，添加数据：

```
mutation {
  createUser(data: {
    name: "Sarah"
    country: "au"
    postcode:"123"
  }) {
    id
  }
}
```

可在右边查看结果

可执行查询users，查看结果
···
query {
  users {
    name
  }
}
···