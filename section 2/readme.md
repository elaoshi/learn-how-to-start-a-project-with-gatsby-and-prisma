brew tap prisma/prisma
brew install prisma

一开始要新建一个目录，
在目录下 进行初始化 工作。 # 坑 1 

开始 初使化
prisma init --endpoint http://localhost:4466


这里会生成 2个文件

.yml 和 .prisma 


初使化后， deploy 到 prisma 上。
prisma deploy

Prisma Admin: http://localhost:4466/_admin

