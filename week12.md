
# Week 12 notes


**Some readings**

[SQL Lite Prisma full tutorial](https://www.robinwieruch.de/next-prisma-sqlite/)
[SQL Lite Prisma](https://www.prisma.io/dataguide/sqlite)
[Basics of Database Design] (https://support.microsoft.com/en-us/office/database-design-basics-eb2159cf-1e30-401a-8084-bd4f9c9ca1f5)
(video) [SQL Step-by-step for beginners](https://www.youtube.com/watch?app=desktop&v=qCIFuoN32cM)
[Data Modeling with prisma](https://www.prisma.io/docs/orm/overview/introduction/data-modeling)

## Databse Design

- Relationships
- Unique identifiers
- Types

## 


## SQL Lite

- SQL Lite is a database file used on your computer
- Great for small applications, not so much for larger
- Locking structure (can't read and write at the same time)
- Runs on all the same rules as other SQL databases


## Relationships in Prisma

TODO:

## Using Prisma with SQL Lite

installing SQL Lite

```
    npm install sqlite3
```

When initializing prisma
```
    npx prisma init --datasource-provider sqlite
```

A change to the schema

```
    generator client {
    provider = "prisma-client-js"
    }

    datasource db {
    provider = "sqlite"
    url      = env("DATABASE_URL")
    }
```

Add the path to the db in the .env
```
DATABASE_URL="file:./database.db"
```

Make the DB file in your project (right-click, make a file named database.db)