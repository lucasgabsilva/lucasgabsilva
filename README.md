# API de Games

Esta API utilizada para X

## Endpints
### GET/games
Esse endpoint retorna a listagem de todos os games cadastrados no banco de dados.
#### Parâmetros
Nenhum
#### Respostas
##### OK! 200
Caso essa resposta aconteça, envia a listagem de todos os games
Exemplo de resposta bem sucedida 
```
[
    {
        "id": 23,
        "title": "Call of duty MW",
        "year": 2019,
        "price": 200
    },
    {
        "id": 12,
        "title": "Fifa 21",
        "year": 2021,
        "price": 300
    },
    {
        "id": 3,
        "title": "GTA V",
        "year": 2015,
        "price": 400
    },
    {
        "id": 33,
        "title": "Euro Truck Simulator 2",
        "year": 2010,
        "price": 70
    }
]
```
##### Falha na autenticação

Exemplo de resposta
```
{
    "err": "Token de autenticação inválido"
}
```
Caso aconteça, indica alguma falha ocorrida durante o processo de autenticação da requisição, como o token inválido ou expirado

### POST/auth
Esse endpoint é responsável por realizar o login do usuário 
#### Parâmetros
Email: recebe os dados do email cadastrado pelo usuário
Senha: recebe a senha cadastrada que está relacionada ao email

Exemplo:
```
{
    "email" : "Lucas@gmail.com",
    "password" : "123456"
}
```
##### Falha na autenticação. 401
Caso aconteça, indica que houve uma falha na autenticação do usuário, podendo ser causada pelo email e/ou senha digitados incorretamente.

Exemplo: 
```
{err: "Credenciais incorretas"}
```

#### Respostas
##### ok. 200
Caso essa resposta aconteça, recebemos o token de autenticação criptografado com JWT

Por exemplo:
```
{
    "token": "eyJhbGciOiJIUzI1NiIsInR5cCI6IkpXVCJ9.eyJpZCI6MSwiZW1haWwiOiJMdWNhc0BnbWFpbC5jb20iLCJpYXQiOjE3MDQ3MTYwODQsImV4cCI6MTcwNDcxOTY4NH0.xCBPdm5zFNaN6A5phXnvQlc-Qpjru-I5g2PTqfLZN7s"
}
```


