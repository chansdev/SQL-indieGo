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
_Falta login e contato_

#### Dados Bancários
```sql
CREATE TABLE dados_bank (
  Cpf_U		int(11) PRIMARY KEY,
  BID_U			int,
  Nome_Titular	varchar(50),
  Numero_Agenc	int(4),
  Numero_Cartao	int(16),
  Validade		varchar(5),
  FOREIGN KEY (BID_U) REFERENCES Usuario(ID_U)
)
```

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
#### Recompensas
```sql
CREATE TABLE Recompensas(
  ID_R		int PRIMARY KEY,
  RID_K		int,
  Titulo	varchar(50),
  Descricao	varchar(500),
  Valor		float,
  FOREIGN KEY (RID_K) REFERENCES Usuario(ID_K)
)
```

## Projeto
```sql
create table Projeto(
  ID_P			int,
  Nome_P		varchar(100),
  Desc_P		varchar(999),
  Data_CriaP	varchar(10)
)
```

## Doa
```sql
create table Doa (
  ID_D			int PRIMARY KEY,
  DID_U			int,
  DID_P			int,
  Data_Doa  date,
  FOREIGN KEY (DID_U) REFERENCES Usuario(ID_U),
  FOREIGN KEY (DID_P) REFERENCES Projeto(ID_P)
);
```
_Falta Dados_Bank_

## Posta
```sql
create table Posta (
  ID_Po			int  PRIMARY KEY,
  PID_U			int,
  PID_P			int,
  Data_Pos		date,
  FOREIGN KEY (PID_U) REFERENCES Usuario(ID_U),
  FOREIGN KEY (PID_P) REFERENCES Projeto(ID_P)
);
```
