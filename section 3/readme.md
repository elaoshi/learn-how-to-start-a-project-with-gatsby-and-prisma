brew tap prisma/prisma
brew install prisma

# 一开始要新建一个目录，
在目录下 进行初始化 工作。 # 坑 1 

# 开始 初使化
prisma init --endpoint http://localhost:4466


这里会生成 2个文件

.yml 和 .prisma 


# 初使化后， deploy 到 prisma 上。
prisma deploy

Prisma Admin: http://localhost:4466/_admin

# 加 generate client 

generate:
  - generator: typescript-client
    output: ./generated/prisma-client/


prisma generate

# add options to tsconfig.json : 
{
  "compilerOptions": {
    "lib": ["es2016", "esnext.asynciterable"]
  }
}

# initialize an empty NPM project 
npm init -y
npm install --save prisma-client-lib
npm install --save-dev typescript ts-node

# Almost done!

touch index.ts

# add code : 

import { prisma } from './generated/prisma-client'

// A `main` function so that we can use async/await
async function main() {
  // Create a new user called `Alice`
  const newUser = await prisma.createUser({ name: 'Alice' })
  console.log(`Created new user: ${newUser.name} (ID: ${newUser.id})`)

  // Read all users from the database and print them to the console
  const allUsers = await prisma.users()
  console.log(allUsers)
}

main().catch(e => console.error(e))

# add a start script to package.json

"start": "ts-node index.ts"


# npm run start