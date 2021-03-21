# Desafio 01 Rocketseat Ignite Trilha NodeJS - Módulo 01 Fundamentos do NodeJS

Desafio realizado durante o treinamento Ignite da Rocketseat na trilha de NodeJS.

## Como rodar o projeto

``` bash
  git clone https://github.com/leolimcav/ignite-nodejs-desafio1.git
  cd ignite-nodejs-desafio1

  yarn install # ou somente yarn para instalar os pacotes
  yarn dev # executa o servidor node

  ### Verificar se os testes estão passando ###
  yarn test
```

## Rotas

- ### /users
  - Método: POST
  - Request Body(JSON): username(string), name(string)
  - Retorna: Objeto do tipo User com os campos id(uuid), name(string), username(string), todos(array)
  - Status Code: 201, 400

- ### /todos
  - Métodos: GET
  - Headers: Username - String com o username de um usuário para validação
  - Request Body(JSON): username(string), name(string)
  - Retorna: Lista de Todos de um Usuário
  - Status Code: 200, 404
  
- ### /todos
  - Método: POST
  - Headers: Username - String com o username de um usuário para validação
  - Request Body(JSON): title(string), deadline(string no formato ANO-MES-DIA)
  - Retorna: Objeto do tipo Todo com os campos id(uuid), title(string), deadline(date), done(boolean), created_at(date)
  - Status Code: 201, 404
  
- ### /todos/:id
  - Método: PUT
  - Headers: Username - String com o username de um usuário para validação
  - Request Body(JSON): title(string), deadline(string no formato ANO-MES-DIA)
  - Retorna: Objeto do tipo Todo com os campos id(uuid), title(string), deadline(date), done(boolean), created_at(date)
  - Status Code: 200, 404

- ### /todos/:id/done
  - Método: PATCH
  - Headers: Username - String com o username de um usuário para validação
  - Retorna: Objeto do tipo Todo com os campos id(uuid), title(string), deadline(date), done(boolean), created_at(date)
  - Status Code: 200, 404
  
- ### /todos/:id
  - Método: DELETE
  - Headers: Username - String com o username de um usuário para validação
  - Request Body(JSON): title(string), deadline(string no formato ANO-MES-DIA)
  - Retorna: Nada
  - Status Code: 204, 404