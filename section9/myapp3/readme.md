
# 添加 seed

run :  
prisma deploy
prisma seed

注： 如果 执行 seed 多次，它会插入多次初始数据。


# reset to init data
prisma seed --reset