# Comandos SQL - Referenças 
<!--____________________________________________-->
## Modelagem física

###Criar banco de dados

```sql


CREATE DATABASE vendas CHARACTER SET utf8mb4;

```
<!--____________________________________________-->
## Modelagem física

###Criar  tabela fabricantes

```sql

CREATE TABLE fabricantes(
    id INT NOT NULL PRIMARY KEY AUTO_INCREMENT,
    nome VARCHAR(45) NOT NULL
)

```
###Criar a tabele produtos
```sql

CREATE TABLE produtos (
    id INT NOT NULL PRIMARY KEY AUTO_INCREMENT,
    nome VARCHAR(45) NOT NULL,
    descricao TEXT(1000) NOT NULL,
    preco DECIMAL(6,2) NOT NULL,
    quantidade TINYINT(4) NOT NULL
)

```
<!--______________________________________________-->

### Adicinar campo/coluna em uma tabela
```sql

ALTER TABLE produtos ADD fabricantes_id INT NOT NULL
AFTER quantidade;


```
<!--______________________________________________-->

### Criação da chave estrangeira (relacionamento entre tabela)

```sql

 ALTER TABLE produtos
    # CONSTRAINT é uma restriçao definida no relacionamento 
    ADD CONSTRAINT fk_produtos_fabricantes

    # A chave estrangeira deve fazer referencia a chave primeira 
 FOREIGN KEY (fabricante_id) REFERENCES fabricantes(id)


```



