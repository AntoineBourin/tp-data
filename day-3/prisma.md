# Installation Prisma

`npm install @prisma/client`

`npm install prisma --save-dev`

Adapteur de requête pour sqlite

`npm install @prisma/adapter-better-sqlite3`

## Initialisation

`npx prisma init --datasource-provider sqlite`

### Exemple de schema Order

schema.prisma

```
model Order {
  id    Int             @id @default(autoincrement())
  productId  String
  firstName  String
  lastName   String
  email      String
}
```

### Executer une migration

`npx prisma migrate dev --name init`

## Génération du client Prisma

`npx prisma generate`

## Ajout du singleton pour interagir avec le client

prisma.ts

```
import { PrismaBetterSqlite3 } from "@prisma/adapter-better-sqlite3";
import { PrismaClient } from "../generated/prisma/client";

const prismaClientSingleton = () => {
  const adapter = new PrismaBetterSqlite3({
    url: process.env.DATABASE_URL,
  });
  return new PrismaClient({
    adapter,
  });
};

declare const globalThis: {
  prismaGlobal: ReturnType<typeof prismaClientSingleton>;
} & typeof global;

const prisma = globalThis.prismaGlobal ?? prismaClientSingleton();

export default prisma;

if (process.env.NODE_ENV !== "production") globalThis.prismaGlobal = prisma;
```

## Visualisation des données

`npx prisma studio`

## Interaction avec BDD

`prisma.order.create({ data: order })`

`prisma.order.findMany({ where: { productId: id } })`

## S'assurer que le client est généré après l'installation des dépendances

```
"scripts": {
    "dev": "next dev",
    .....
    "postinstall": "prisma generate"
  },
```
