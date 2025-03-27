# SQL-indieGo
banco de bagos do indieGo

### Usuário ###

```sql
CREATE TABLE Usuario (
  ID_U int PRIMARY KEY,
  Nome_U varchar(100),
  Data_Nasc varchar(8),
  Data_CriaU varchar(8)
)
```
falta login contato e dados_bank
-------------------------------------------------
### Comunidade

```sql
CREATE TABLE Comunidade (
  ID_C int PRIMARY KEY,
  Nome_C varchar(100),
  Desc_C varchar(999),
  Data_CriaC varchar(8)
)
```
