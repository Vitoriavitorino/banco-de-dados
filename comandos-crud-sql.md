# Comandos SQL - Para CRUD (Referencias)

## resumo 
c-> Create (Insere dados)
R-> Read (ler dados)
u-Update (Atualizar dados) 
D-> Deleta (Deletar dados)

<!--_____________________________________________-->

## Insert 
## Fabricantes

```sql

INSERT INTO fabricantes (nome) VALUES ('Asus');
INSERT INTO fabricantes (nome) VALUES ('Dell');
INSERT INTO fabricantes (nome) 
VALUES ('Apple'),('LG'),('Samsung'),('Brastemp');

```
<!--_________________________________________-->

## Insert
## Produtos

```sql
INSERT INTO produtos (nome,descricao,preco,quantidade,fabricante_id) VALUES(
    'Ultrabook',
    'Ultrabook Asus Intel Core i9',
    6500.99,
    7,
    1
)
```
