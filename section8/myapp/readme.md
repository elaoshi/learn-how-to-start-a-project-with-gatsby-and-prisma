
# 添加 relationship between Car and User

# 生成新的测试环境

prisma deploy 

# 查看后台

添加了 cars 字段，看下效果。

# 添加一个 User ,然后再添加一个 Car

# 结果可见成功的连接了两个对象

for user:
```
{
  users {
    id
    name
    cars {
      id
    }
  }
}

```

for car:
```
{
  cars {
    id
    name
    owner {
      id
    }
  }
}
```

