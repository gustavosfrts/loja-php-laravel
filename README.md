# Comandos necessários de serem rodados para iniciar o projeto
php composer i
\
php artisan migrate --seed
\
php artisan key:generate

### Dados do banco

```
database: loja
username: root
password:
```

#### URI e JSON Body de cada rota
## Cliente
* GET - *api.show.one.cliente*
    * URI - /api/cliente/listar/{id}
    * *Não possui JSON.*

<hr>

* POST - *api.show.all.cliente*
    * URI - /api/cliente/listar
```json
{
    "filtro": null,
    "order": "asc",
    "orderCampo": null,
    "quantPagina": 20
}
```

<hr>

* POST - *api.create.cliente*
    * URI - /api/cliente/cadastro
```json
{
    "nome": "Gustavo Freitas",
    "cpf": "12345678910",
    "email": null
}
```
<hr>

* PUT - *api.update.cliente*
    * URI - /api/cliente/atualizar/{id}
```json
{
    "nome": "Gustavo Freitas",
    "cpf": "12345678910",
    "email": null
}
```
<hr>

* DELETE - *api.delete.cliente*
    * URI - /api/cliente/deletar/{id}
    * *Não possui JSON.*

## Produto
* GET - *api.show.one.produto*
    * URI - /api/produto/listar/{id}
    * *Não possui JSON.*

<hr>

* POST - *api.show.all.produto*
    * URI - /api/produto/listar
```json
{
    "filtro": null,
    "order": "asc",
    "orderCampo": null,
    "quantPagina": 20
}
```

<hr>

* POST - *api.create.produto*
    * URI - /api/produto/cadastro
```json
{
    "quantidade": 5,
    "valorUnitario": 9800,
    "nomeProduto": "PC Gamer"
}
```
<hr>

* PUT - *api.update.produto*
    * URI - /api/produto/atualizar/{id}
```json
{
    "quantidade": 5,
    "valorUnitario": 9800,
    "nomeProduto": "PC Gamer"
}
```
<hr>

* DELETE - *api.delete.produto*
    * URI - /api/produto/deletar/{id}
    * *Não possui JSON.*


## Pedido
* GET - *api.show.one.pedido*
    * URI - /api/pedido/listar/{id}
    * *Não possui JSON.*

<hr>

* POST - *api.show.all.pedido*
    * URI - /api/pedido/listar
```json
{
    "filtro": null,
    "order": "asc",
    "orderCampo": null,
    "quantPagina": 20
}
```

<hr>

* POST - *api.create.pedido*
    * URI - /api/pedido/cadastro
```json
{
    "status": 1,
    "idCliente": 1,
    "produtos": [
        {
            "idProduto": 1,
            "quantidade": 2
        },
        {
            "idProduto": 2,
            "quantidade": 1
        }
    ]
}
```
<hr>

* PUT - *api.update.pedido*
    * URI - /api/pedido/atualizar/{id}
```json
{
    "status": 3,
    "produtosExcluir": [1],
    "produtosCadastro": [
        {
            "idProduto": 3,
            "quantidade": 3
        },
        {
            "idProduto": 4,
            "quantidade": 1
        }
    ]
}
```
<hr>

* PUT - *api.pay.pedido*
    * URI - /api/pedido/pagar/{id}
    * *Não possui JSON.*

<hr>

* PUT - *api.cancel.pedido*
    * URI - /api/pedido/cancelar/{id}
    * *Não possui JSON.*

<hr>

* DELETE - *api.delete.pedido*
    * URI - /api/pedido/deletar/{id}
    * *Não possui JSON.*
