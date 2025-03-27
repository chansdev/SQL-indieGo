# SQL-indieGo
banco de bagos do indieGo <br>
https://www.programiz.com/sql/online-compiler

## Usuário 
```sql
CREATE TABLE Usuario (
  ID_U int PRIMARY KEY,
  Nome_U varchar(100),
  Data_Nasc varchar(8),
  Data_CriaU varchar(8)
)
```
_Falta login contato e dados_bank_
## Comunidade

```sql
CREATE TABLE Comunidade (
  ID_C int PRIMARY KEY,
  Nome_C varchar(100),
  Desc_C varchar(999),
  Data_CriaC varchar(8)
)
```
## Kickstarter
```sql
create table Kickstarter(
  ID_K			int,
  Nome_K		varchar(100),
  Desk_K		varchar(100),
  Data_CriaK	varchar(10),
  Fundos		float,
  Meta			float
)
```
_Falta recompensas_
## Projeto
```sql
create table Projeto(
  ID_P			int,
  Nome_P		varchar(100),
  Desc_P		varchar(999),
  Data_CriaP	varchar(10)
)
```
