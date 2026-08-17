# Minimal API da Fórmula 1

Lab da DIO: uma API simples de Fórmula 1 com Node.js, TypeScript e Fastify.

Não tem banco de dados. Os dados ficam no próprio código e as rotas devolvem JSON.

Usei o [node-blue-boilerplate](https://github.com/felipeAguiarCode/node-blue-boilerplate) pra não montar o TypeScript do zero.

## Como rodar

Precisa do Node.js 20+.

```bash
git clone https://github.com/sir-devtech/formula-project-dio.git
cd formula-project-dio
npm install
npm run start:dev
```

Sobe em http://localhost:3333

## Rotas

`GET /teams` — lista as equipes

`GET /drivers` — lista os pilotos

`GET /drivers/:id` — busca um piloto pelo id. Se não achar, volta 404.

Exemplos:

- http://localhost:3333/teams
- http://localhost:3333/drivers
- http://localhost:3333/drivers/1
- http://localhost:3333/drivers/99 (esse aqui dá Driver Not Found)

## O que eu fiz

Instalei o Fastify, criei o servidor na porta 3333 e as rotas de teams e drivers. Depois fiz o filtro por id, coloquei mais dados das equipes e habilitei o CORS.

O código principal tá em `src/server.ts`.
