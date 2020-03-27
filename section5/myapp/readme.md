# 更新 model 

往 datamodel.prisma 里改数据

注： 每次  prisma deploy --force 不把原有数据删掉。

如果不是require 的值，则直接使用 deploy 就好。
如果是有 require 的字段 那会有提示出现，如果确认无事，则可用 --force 来直接更新。

prisma deploy
