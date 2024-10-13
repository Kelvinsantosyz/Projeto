# Projeto OneLife Advogados

## Descrição

Este projeto é um sistema de gerenciamento de usuários e chamados para a OneLife Advogados, focado em maximizar a captação de clientes e divulgar os serviços oferecidos. O sistema inclui funcionalidades para autenticação, registro de usuários, e gerenciamento de chamados.

## Tecnologias Utilizadas

- **Backend**: Node.js, Express
- **Banco de Dados**: MySQL
- **Frontend**: HTML, CSS, JavaScript, Bootstrap
- **Dependências**:
  - `bcrypt`: Para hashing de senhas.
  - `express-session`: Para gerenciamento de sessões.
  - `mysql2`: Para interação com o banco de dados MySQL.
  - Outros conforme listado em `package.json`.

## Estrutura do Banco de Dados

O banco de dados consiste nas seguintes tabelas:

### Tabela `usuarios`

| Coluna    | Tipo           | Descrição                          |
|-----------|----------------|------------------------------------|
| id        | INT            | Identificador único do usuário (chave primária). |
| nome      | VARCHAR(255)   | Nome do usuário (obrigatório).    |
| sobrenome | VARCHAR(255)   | Sobrenome do usuário (obrigatório). |
| email     | VARCHAR(255)   | E-mail único do usuário (obrigatório e deve ser único). |
| senha     | VARCHAR(255)   | Senha do usuário (obrigatório).   |

### Tabela `chamados`

| Coluna        | Tipo           | Descrição                                     |
|---------------|----------------|-----------------------------------------------|
| id            | INT            | Identificador único do chamado (chave primária). |
| nome          | VARCHAR(255)   | Nome da pessoa que faz o chamado (obrigatório). |
| sobrenome     | VARCHAR(255)   | Sobrenome da pessoa (obrigatório).          |
| email         | VARCHAR(255)   | E-mail da pessoa (obrigatório).             |
| telefone      | VARCHAR(255)   | Número de telefone (obrigatório).           |
| ramo          | VARCHAR(255)   | Ramo do direito relacionado ao chamado (obrigatório). |
| descricao     | TEXT           | Descrição detalhada do chamado (obrigatório). |
| status        | VARCHAR(255)   | Status do chamado, inicia como 'Aberto'.    |
| data_criacao  | TIMESTAMP      | Data e hora em que o chamado foi criado.    |

### Tabela `sessions`

| Coluna      | Tipo           | Descrição                           |
|-------------|----------------|-------------------------------------|
| session_id  | VARCHAR(128)   | Identificador único da sessão (chave primária). |
| expires     | INT UNSIGNED    | Tempo de expiração da sessão (em segundos). |
| data        | MEDIUMTEXT     | Dados da sessão.                   |

## Instalação

Para instalar as dependências do projeto, execute o seguinte comando:

```bash
npm install
