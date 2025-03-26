# API de Autenticação

![Java](https://img.shields.io/badge/java-%23ED8B00.svg?style=for-the-badge&logo=openjdk&logoColor=white)
![Spring](https://img.shields.io/badge/spring-%236DB33F.svg?style=for-the-badge&logo=spring&logoColor=white)
![JWT](https://img.shields.io/badge/JWT-black?style=for-the-badge&logo=JSON%20web%20tokens)

Este projeto é uma API desenvolvida utilizando **Java, Java Spring, Flyway Migrations, PostgreSQL como banco de dados e Spring Security com JWT para controle de autenticação.**

## Tabela de Conteúdos

- [Instalação](#instalação)
- [Configuração](#configuração)
- [Uso](#uso)
- [Endpoints da API](#endpoints-da-api)
- [Autenticação](#autenticação)
- [Banco de Dados](#banco-de-dados)
- [Contribuição](#contribuição)

## Instalação

1. Clone o repositório:

```bash
git clone https://github.com/pedrosoaresdev/authjwt
```

2. Instale as dependências com Maven.

3. Instale o [PostgreSQL](https://www.postgresql.org/).

## Uso

1. Inicie a aplicação com Maven.
2. A API estará acessível em: [http://localhost:8080](http://localhost:8080).

## Endpoints da API

A API fornece os seguintes endpoints:

```markdown
GET /product - Retorna uma lista de todos os produtos (acessível por todos os usuários autenticados).

POST /product - Registra um novo produto (somente usuários com acesso ADMIN).

POST /auth/login - Faz login no aplicativo.

POST /auth/register - Registra um novo usuário no aplicativo.
```

## Autenticação

A API utiliza Spring Security para controle de autenticação. Os seguintes papéis (roles) estão disponíveis:

```
USER -> Papel padrão para usuários logados.
ADMIN -> Papel de administrador para gerenciar parceiros (registrar novos parceiros).
```

Para acessar endpoints protegidos como um usuário ADMIN, forneça as credenciais de autenticação apropriadas no cabeçalho da requisição.

## Banco de Dados

O projeto utiliza [PostgreSQL](https://www.postgresql.org/) como banco de dados. As migrações necessárias do banco são gerenciadas pelo Flyway.

## Contribuição

Contribuições são bem-vindas! Se você encontrar algum problema ou tiver sugestões de melhorias, abra uma issue ou envie um pull request para o repositório.

Ao contribuir para este projeto, siga o estilo de código existente, as [convenções de commit](https://www.conventionalcommits.org/en/v1.0.0/) e envie suas alterações em um branch separado.
