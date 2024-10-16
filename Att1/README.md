

# Projeto: Aplicação Bancária - Mobile e API

Este projeto consiste em uma aplicação bancária simples, desenvolvida com Flutter no front-end mobile e `json-server` para simular uma API REST no back-end. O objetivo é permitir a criação, edição, listagem e exclusão de transações financeiras, integrando uma interface móvel a uma API.

## Objetivo do Projeto

Muitas aplicações modernas exigem integração com APIs para processar, validar e armazenar dados em serviços externos ou bancos de dados. Neste projeto, utilizamos Flutter para realizar requisições HTTP e conectar a aplicação mobile a uma API construída com `json-server`.

### Funcionalidades Implementadas:

1. **Formulário de Transações**:
   - Tela com um formulário que contém dois campos:
     - **Campo de texto**: Para o nome da transação.
     - **Campo numérico**: Para o valor da transação.

2. **Lista de Transações**:
   - Tela que exibe uma lista das transações cadastradas via formulário.
   - A lista permite:
     - **Criação** de novas transações.
     - **Edição** de transações existentes.
     - **Exclusão** de transações.
   - Todas as operações de **CRUD** (criar, ler, atualizar, deletar) são realizadas via API.
   - Para manter o código organizado, foi usada uma **classe abstrata** que contém os principais métodos do CRUD, permitindo a reutilização em outras partes da aplicação.

### Tema da Aplicação

A aplicação é uma **Aplicação Bancária**, onde o usuário pode gerenciar transações financeiras, simulando funcionalidades básicas de um sistema bancário.

---

## Instruções de Instalação

### Back-end (API)

1. Navegue até a pasta `backend`.
2. No terminal, execute o seguinte comando para iniciar o servidor:
   
   ```bash
   json-server --watch db.json
   ```

3. Se o `json-server` não estiver instalado, você precisará instalá-lo globalmente no seu computador. Para isso, execute:

   ```bash
   npm install -g json-server
   ```

### Front-end (Mobile)

1. Navegue até a pasta `mobile`.
2. No terminal, instale a dependência HTTP necessária para fazer requisições no Flutter:

   ```bash
   flutter pub add http
   ```

3. Para rodar o aplicativo Flutter, execute o seguinte comando:

   ```bash
   flutter run
   ```

---

## Estrutura do Projeto

- **Backend**:
  - Simulado com `json-server`, onde os dados são persistidos no arquivo `db.json`.

- **Mobile**:
  - Desenvolvido com Flutter.
  - O app realiza operações de CRUD ao se conectar com a API via requisições HTTP.

---

## Fluxo da Aplicação

### 1. Iniciar o servidor API:

Execute o comando `json-server --watch db.json` na pasta `backend` para iniciar a API, que atuará como o backend simulando o banco de dados.

### 2. Interagir com o aplicativo mobile:

No app Flutter, o usuário pode:
- **Cadastrar novas transações** por meio de um formulário.
- **Visualizar a lista de transações** cadastradas.
- **Editar ou excluir transações existentes** diretamente na lista.

### 3. Persistência de dados:

Todas as transações realizadas pelo usuário são salvas no arquivo `db.json` via API, garantindo que os dados sejam armazenados de forma persistente e possam ser recuperados quando necessário.

---

## Tecnologias Utilizadas

- **Flutter**: Para o desenvolvimento da interface mobile.
- **Dart**: Linguagem de programação usada no Flutter.
- **json-server**: Para simular a API RESTful.
- **HTTP**: Para realizar as requisições entre o app Flutter e a API.

