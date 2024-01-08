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
Caso aconteça, indica alguma falha ocorrida durante o processo de autenticação da requisição, como o token inválido ou expirado
