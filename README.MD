# Minimal API da Fórmula 1

Projeto do lab **Criando uma Minimal API da Fórmula 1 com Node.js e Fastify**, da DIO.

A API devolve dados de equipes e pilotos em JSON, usando Node.js, TypeScript e Fastify.

## Tecnologias

- Node.js
- TypeScript
- Fastify
- @fastify/cors

Baseado no boilerplate [node-blue-boilerplate](https://github.com/felipeAguiarCode/node-blue-boilerplate).

## Como rodar

Pré-requisitos: Node.js 20+ e npm.

```bash
# clonar o repositório
git clone https://github.com/sir-devtech/formula-project-dio.git

# entrar na pasta
cd formula-project-dio

# instalar dependências
npm install

# iniciar o servidor
npm run start:dev
```

O servidor sobe em `http://localhost:3333`.

## Endpoints

| Método | Rota | Descrição |
| --- | --- | --- |
| GET | `/teams` | Lista as equipes |
| GET | `/drivers` | Lista os pilotos |
| GET | `/drivers/:id` | Busca um piloto pelo id |

### Exemplos

`GET http://localhost:3333/teams`

```json
{
  "teams": [
    { "id": 1, "name": "McLaren", "base": "Woking, United Kingdom" }
  ]
}
```

`GET http://localhost:3333/drivers`

```json
{
  "drivers": [
    { "id": 1, "name": "Max Verstappen", "team": "Red Bull Racing" }
  ]
}
```

`GET http://localhost:3333/drivers/1`

```json
{
  "driver": { "id": 1, "name": "Max Verstappen", "team": "Red Bull Racing" }
}
```

Se o id não existir, a API responde `404` com `{ "message": "Driver Not Found" }`.

## O que foi feito neste lab

1. Usei o boilerplate com TypeScript já configurado.
2. Instalei o Fastify (`npm i fastify`).
3. Criei o servidor em `src/server.ts` na porta 3333.
4. Criei os endpoints `/teams` e `/drivers`.
5. Implementei o filtro de piloto em `/drivers/:id`.
6. Incrementei os dados das equipes e dos pilotos.
7. Habilitei CORS com `@fastify/cors`.

## Links

- Repositório deste projeto: https://github.com/sir-devtech/formula-project-dio
- Boilerplate usado: https://github.com/felipeAguiarCode/node-blue-boilerplate
- Referência do lab: https://github.com/digitalinnovationone/node-formula-1
- Fastify: https://fastify.dev/

## Scripts

- `npm run start:dev`: sobe o servidor em modo desenvolvimento
- `npm run start:watch`: sobe o servidor recarregando ao salvar
- `npm run dist`: gera o build em JavaScript
- `npm run start:dist`: gera o build e executa a versão compilada
