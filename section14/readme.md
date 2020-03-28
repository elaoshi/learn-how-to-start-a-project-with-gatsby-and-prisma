
# create account in prisma cloud

get login url 

# run : 
prisma login -k xxxxxx

# init project , it will generate endpoint in cloud for us !

prisma init hello-world

# select server the us one 
if issues shows , ignore it . 

# run 
cd hello-world
prisma deploy

# done , then we have remote space

https://us1.prisma.sh/eric-xxxx/hello-world/dev/_admin

# then import data
prisma import -d ex.....

