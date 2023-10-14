<h1 align="center">Todolist Java</h1>

Projeto Maven, feito utilizando Springboot, consiste em uma API de cadastro com lista de tarefas.

### Sumário
- [Como começar](#como-começar)
- [Features](#features)
- [Tecnologias utilizadas](#tecnologias-utilizadas)

## Como começar

* Utilize uma plataforma para fazer requisições, como o [Postman](https://www.postman.com) ou [APIDog](https://apidog.com/?utm_source=google_search&utm_medium=g&utm_campaign=18544428894&utm_content=153517438552&utm_term=apidog&gad=1&gclid=CjwKCAjw-KipBhBtEiwAWjgwrDGW3LOJOzo7sHEut6kaW9wXcKOh_U_DZoSVMImBJoHvZkzunzeC2xoCvN4QAvD_BwE).
* A URL padrão é: https://todolist-java-3cy9.onrender.com
* Faça um cadastro no formato `JSON` e método `POST`, utlizando a rota `/users/`. E insira as credenciais
```
{
    "name": "your_name"
    "username": "your_username",
    "password": "your_password",
}
```
* Envie a requisição e será retornado os dados do cadastro. Com `ID`, `username`, `name`, `password` (criptografada) e `data de criação`.

Desta forma:
```
{
    "id": "de24f6b2-a419-4113-a27a-02751cb77fb7",
    "username": "your_username",
    "name": "your_name",
    "password": "$2a$12$mQxj5EZBfFmqux50w8GvLuN6iuCmIbbNC92b0t.ICEEmB3pydwTxC",
    "createdAt": "2023-10-14T16:17:02.487742"
}
```
* Após feito o cadastro, utilize a rota `/tasks/`. Vá na aba `Auth` da sua plataforma de API, e insira em `username` e `password`.
  
* E crie sua tarefa no formato `JSON`, passando os seguintes parâmetros: description; title; priority; startAt; endAt; userId.
 
Não se esqueça de inserir o seu token de usuário em `userId`:
```
{
    "description": "description",
    "title": "title",
    "priority": "priority",
    "startAt": "2023-11-12T00:00:00",
    "endAt": "2023-11-12T10:10:10",
    "userId": "de24f6b2-a419-4113-a27a-02751cb77fb7"
}
```
* Para atualizar uma tarefa, apenas faça o mesmo que foi feito para criar a tarefa, e mude a credencial de sua escolha.

## Features

* Validação via token, e criptografia
* Atualizar tasks existentes

## Tecnologias utilizadas

* Java
* Springboot
* H2 database

Nota: este é um projeto demonstrativo, portanto é utilizado um domínio gratuito e um banco de dados que apenas armazena em memória.