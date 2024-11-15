<p align="center">
  <img src="https://www.docker.com/wp-content/uploads/2022/03/horizontal-logo-monochromatic-white.png" alt="Docker Logo" width="300">
</p>

# PostgreSQL + pgAdmin Stack

Este repositório configura um ambiente de desenvolvimento com **PostgreSQL** e **pgAdmin** usando contêineres Docker Compose

## Tecnologias

- ![Docker](https://img.shields.io/badge/Docker-2496ED?style=for-the-badge&logo=docker&logoColor=white)
- ![PostgreSQL](https://img.shields.io/badge/PostgreSQL-336791?style=for-the-badge&logo=postgresql&logoColor=white)
- ![pgAdmin](https://img.shields.io/badge/pgAdmin-0061a6?style=for-the-badge&logo=postgresql&logoColor=white)

## Pré-requisitos

- **Docker** instalado
- **Docker Compose** instalado

## Estrutura do Projeto

- **.data/**: Diretório de armazenamento de dados para persistência do PostgreSQL e pgAdmin.
- **pg-stack.yml**: Arquivo Docker Compose para configurar e iniciar os contêineres.
- **README.md**: Documentação do projeto.

## Configuração dos Contêineres

### PostgreSQL

- **Imagem**: `postgres:14-alpine`
- **Nome do Contêiner**: `dev-postgresql`
- **Porta**: `5433` (localhost) mapeada para `5432` (contêiner)
- **Credenciais**:
  - Banco de Dados: `mydatabase`
  - Senha: `1234567`
- **Volume**: `./.data/postgresql/data` (persistência de dados)

### pgAdmin

- **Imagem**: `dpage/pgadmin4`
- **Nome do Contêiner**: `dev-pgadmin`
- **Porta**: `5050` (localhost) mapeada para `80` (contêiner)
- **Credenciais**:
  - E-mail: `me@example.com`
  - Senha: `1234567`
- **Volume**: `./.data/pgadmin` (persistência de dados)

### Rede

- **Nome da Rede**: `dev-network`
- **Driver**: `bridge`

## Como Usar

1. **Iniciar os contêineres**:
   No terminal, navegue até a pasta do projeto e execute:

   ```bash
   docker-compose up -d

<h2>✍️ Autor</h2>

<a href="https://github.com/Felps3296">
  <img loading="lazy" src="https://avatars.githubusercontent.com/u/64935845?v=4" width="115" alt="Felipe Viana Reis">
</a>
<br>
<sub><b>Felipe Viana Reis</b></sub>
<br>

